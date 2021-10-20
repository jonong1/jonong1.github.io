---
layout: post
title:  "Mechanical Turk Framework"
date:   2021-04-15
excerpt: "A new system framework integrated with Amazon Mechanical Turk API."
image: "/images/mturk/logo.jpeg"
---
<hr />

## Overview
Mechanical Turk Framework is a software development project that integrates with [Amazon Mechanical Turk API](https://docs.aws.amazon.com/AWSMechTurk/latest/AWSMturkAPI/Welcome.html). Our goal was to provide our client with a simple yet effective framework for conducting / managing web-based experiments (also known as Human Intelligence Tasks - HITs), specifically around behavioural game theory, plus provide a functional dashboard for all that is required and more. My role was a **Full-Stack Developer / Project Manager**, essentially dealing with both front-end and back-end code.

Alternatively, existing software that contains some of the required functionality (i.e., [TurkServer](https://github.com/TurkServer/long-run-cooperation)) either didn't integrate well with Amazon Mechanical Turk, or was built upon a deprecated API. This concluded for our team to meet their needs and propose a system that would provide them with a tool which contains the core functionalities they require, as well as providing them with solid infrastructure that's secure and scalable in the future. 

Before we dive into some obstacles we had to tackle as a team and some core features of our web application, let us first define a few things. Users of our system falls into 2 main categories:
<dl>
	<dt>Administrators (also called Requesters)</dt>
	<dd>
		<li>Consist of researchers who are responsible for managing the application and creating these HITs</li>
	</dd>
	<dt>Turkers (also called Workers)</dt>
	<dd>
		<li>Consist of Amazon Mechanical Turk workers who are responsible in partaking these HITs (& get paid) </li>
	</dd>
</dl>
<hr />

## Obstacles
<span class="image right"><img src="{{ "/images//mturk/web.png" | absolute_url }}" alt="" /></span>
Not only was this a difficult project to finish in 4 months, the time crunch got even smaller as we also needed to implement *servers* where each server had 2 players playing a normal / extensive form game and have it be submitted to Amazon Mechanical Turk directly. This also meant that our databases had to sync with one another at all times, which made optimizing a crucial factor.

To make matters worse, our team consisted of 6 members in which many did not contribute much and so, we had to work overtime and compensate for the missing progress. In the end, I took leadership and delegated tasks to our team so we could meet the client's needs and finish on time. The project turned out to be amazing; code was fully scalable (as is the server / games) and most importantly, bug-free. 
<hr />
## Features
<p><span class="image left"><img src="{{ "/images//mturk/home.png" | absolute_url }}" alt="" /></span>Upon logging into your account, you are greeted to our Overview Page (shown on the left) where it displays your current available balance (in relation to your account on <a href="https://mturk.com">Amazon MTurk</a>). At the top shows the navigation bar, displaying the Experiments Page, HITTypes Page, HITs Page, Active / Completed Assignments Page, Qualifications Page and Workers Page.</p>
<p><span class="image right"><img src="{{ "/images/mturk/exp.png" | absolute_url }}" alt="" /></span>At the top right displays the current experiment (also called batch) which then filters everything related to that specific batch. The very first step an Admin should do is to either create a new experiment or choose an existing one (nothing is selected initially, meaning no data will be displayed). Additionally, most of the other pages show a very similar concept as this one; a simple table displaying the existing information details, and the choice of adding a new field. Moreover, the Qualifications Page can be altered to become active or inactive with just a click of a button. All of this was structured using our back-end <strong>PostgreSQL</strong> database while synchronously integrating it with Amazon MTurk itself - reducing traffic / load times by <strong>15%</strong>.</p>

<p>One of the core features of this whole project that our client requested was to develop servers / lobbies optimized for up to <strong>200</strong> users to play (scalable) normal and extensive form games simultaneously live. Images below show the sequence of how a simple 2-player game of TicTacToe would go about working, starting from our end to Amazons'. (<u><i>Note</i></u>: games are also shown as active assignments).</p>
<div class="box alt">
	<div class="row 50% uniform">
		<div class="4u"><span class="image fit"><img src="{{ "/images/mturk/wait.png" | absolute_url }}" alt="" /><figcaption class="caption" style="text-align:center; display:table; max-width:60%; margin: 10px auto;"><sup>Waiting for other party to join</sup></figcaption></span></div>
		<div class="4u"><span class="image fit"><img src="{{ "/images/mturk/game.png" | absolute_url }}" alt="" /><figcaption class="caption" style="text-align:center; display:table; max-width:60%; margin: 10px auto;"><sup>Playing a turn-based game live</sup></figcaption></span></div>
		<div class="4u$"><span class="image fit"><img src="/images/mturk/gj.png" alt="" /><figcaption class="caption" style="text-align:center; display:table; max-width:60%; margin: 10px auto;"><sup>Submit to Amazon directly</sup></figcaption></span></div>
	</div>
</div>
<p><span class="image right"><img src="{{ "/images//mturk/completed.png" | absolute_url }}" alt="" /></span>When completed, Admins can then approve / reject submitted assignments, or even pay bonuses to workers in bulk through a pop-up (specifically, using checkboxes on the left-hand side). For better security, we also designed our system so that it wouldn't allow Admins to pay bonuses to non-approved assignments or ones already paid. All in all, our user-friendly interface was designed using <strong>HTML / CSS</strong> that allowed users to manage tasks with ease, improving overall time / efficiency.</p>
<hr />

## References
- <https://docs.aws.amazon.com/cli/latest/reference/mturk/index.html>
- <https://channels.readthedocs.io/en/latest/>