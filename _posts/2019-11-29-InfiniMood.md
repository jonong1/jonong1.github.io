---
layout: post
title:  "InfiniMood"
date:   2019-11-29
excerpt: "A mobile mood tracking tool on Android, functioning similarly to Twitter."
image: "/images/infinimood/logo.png"
---
<hr />

## Overview
InfiniMood was based on the concept of the widely popular social networking service, [Twitter](https://twitter.com/). Essentially, our Android application lets us do most of the features Twitter can do, including logging into your unique account, posting said events, searching / requesting to follow other users, and even customizing your profile as you see fit! The main difference between ours and theirs is that instead of just posting anything, we specifically aimed for the current mood at the moment as we feel that it gives insight on a more personal level. 

Additionally, for those who are familiar with the [Snap Map](https://map.snapchat.com/) feature on [Snapchat](https://www.snapchat.com/), we, too, have similarly implemented our own as well. This allows users to check where other people (those of which you're following) are currently located when posting events, as well as giving pop-ups on their respective posts for further details. 
<hr />

## Features
We built this mobile mood tracking application using **Android Studio** and **Java**, while also utilizing **Firebase** to manage / store new and existing user data. As stated above, our real-time live-tracking map system was implemented with **Google API** for all users to interact with simultaneously. 

Below are some examples of a few prominent features for a more visual representation.
<div class="box alt">
		<div class="row 50% uniform">
			<div class="4u"><span class="image fit"><img src="{{ "/images/infinimood/login.png" | absolute_url }}" alt="" /><figcaption class="caption" style="text-align:center; display:table; max-width:60%; margin: 10px auto;"><sup>Sign Up / Login</sup></figcaption></span></div>
			<div class="4u"><span class="image fit"><img src="{{ "/images/infinimood/add.png" | absolute_url }}" alt="" /><figcaption class="caption" style="text-align:center; display:table; max-width:60%; margin: 10px auto;"><sup>Add / Edit Mood Event</sup></figcaption></span></div>
			<div class="4u$"><span class="image fit"><img src="/images/infinimood/history.png" alt="" /><figcaption class="caption" style="text-align:center; display:table; max-width:60%; margin: 10px auto;"><sup>View Past History</sup></figcaption></span></div>
			<!-- Break -->
			<div class="4u"><span class="image fit"><img src="{{ "/images/infinimood/follow.png" | absolute_url }}" alt="" /><figcaption class="caption" style="text-align:center; display:table; max-width:60%; margin: 10px auto;"><sup>Search / Follow Users</sup></figcaption></span></div>
			<div class="4u"><span class="image fit"><img src="{{ "/images/infinimood/map.png" | absolute_url }}" alt="" /><figcaption class="caption" style="text-align:center; display:table; max-width:60%; margin: 10px auto;"><sup>Geolocation</sup></figcaption></span></div>
			<div class="4u$"><span class="image fit"><img src="{{ "/images/infinimood/profile.png" | absolute_url }}" alt="" /><figcaption class="caption" style="text-align:center; display:table; max-width:60%; margin: 10px auto;"><sup>Customize Profile</sup></figcaption></span></div>
		</div>
</div>
<hr />

## References
- <https://github.com/CMPUT301F19T05/InfiniMood>