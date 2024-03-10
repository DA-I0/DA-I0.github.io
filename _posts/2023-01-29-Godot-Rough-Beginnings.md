---
layout: post
title: Godot - Rough Beginnings
tags: godot
excerpt_separator: <!--more-->
---
Throughout the years I used various tools and engines - some more, other less complicated.<br>
The one I stuck with for the longest time would be Unity. It's been around 10 years now, I think?<br>
I'm used to how it works and how to interact with it to create what I want. The process to set up a basic prototype up and running became a second nature and something I can easily do in my sleep. 

Now, it's time to throw out (almost) all of it and start from scratch. It is **hard**.
<!--more-->

On the first glance Godot looks similar enough to Unity so it wasn't particularly difficult to get the basic gist of what's what and what's where. It actually gave me a false sense of familiarity and expectations that this project will go much smoother than it turned out to be.

Not to say Unity is perfect cause, let's be honest, it's not even close, but years of doing things certain way aren't exactly easy to brush off.

Now lets see what I got myself into.

> Before we start I'd like to mention I'm using the stable version of Godot, which at the time of writing would be 3.5.1. I know that version 4 is right around the corner (well, in software development time) but it's still work in progress with lots of fixes and improvements on the way. For the sake of learning with the least amount of outside issues and for a relatively simple project I felt it like going with stable was simply the best solution.

## The Bad

While it's not particularly complicated, attempting to do some things in Godot feels much clunkier than what I'm used to. None of this stuff is enough to turn me away from the engine but it is definitely noticeable.

One of the main things I always go for in Unity is creating a single controller object responsible for housing all the setup scripts and general data holders. Godot objects having only one script slot causes what feels like unnecessary clutter of useless nodes. It probably doesn't have much effect on the technical side but it's a pain from the organizational standpoint.

Another thing is working with signals compared to Unity's *Send/BroadcastMessage* methods. Having to register listeners is simple, sure, but it's an additional step one needs to think about. Am I just lazy?

Prefabs being separate scenes rather than objects isn't **that** different from how you work with them in Unity these days but not being able to modify them from the scene you're working on could definitely be improved. This one is more of a small annoyance than anything but I feel like it's worth mentioning anyway.<br>
Instanced prefabs also don't seem to update when their source scene is modified for some reason - might be a bug or how it works. Need to test this a bit more.

Working with physics and physic layers can be a bit of a pain as well. The lack of typical layer matrix and having to set those interactions on an object level might give you more freedom on how to do it but it's also more cumbersome and, again, requires additional work.

Apparently you also can't disable object elements (children)? I'm going to be honest, this might be me not doing enough research but so far I wasn't able to figure or find out how to do something as simple as disabling a hitbox for a specific object.<br>
You can delete it (my current solution) or change physics masks but I wasn't able to do something that Unity provides with a single method.
And no, using *SetPhysicsProcess(false)* did not help with that.

Then, there's crashing.

![godot crash logs](/assets/images/godot/godot_crash_logs.png){: class="img-transparent-left" }

Oh boy the crashing.

I'm using Linux, specifically Pop_os!<br>
For some reason Godot's editor crashes **a lot** - usually after about 2 to 5 attempts to playtest my changes.
No idea what's going on with that but it can be a real pain considering I tend to try things out pretty often.

> Pictured here is the result of about 2 hours of a **very** casual dev session.

It's not a huge deal since my changes are already saved and restarting the editor takes maybe 10 seconds but it's not a great look for the engine.

I could understand if this was caused by my code triggering a memory leak or breaking stuff in any other way but that's not the case - crashes seem to be absolutely random and happen whether there are any problems with the project or not.

Last but not least - script creation. For whatever reason I can only create new script files inside the editor. It's fine to work with them in VSCodium after that but the creation itself **has** to be done from the UI, otherwise Godot won't treat them as "proper" nor execute anything contained within.

Again, not a huge deal but it does require some additional clicking for no real reason.

## The Good

As mentioned before, Godot's UI felt pretty familiar right out the gate and after using it for a little bit I can confidently say it's quite easy to figure out without any additional help. This is important as I'm someone who likes to play around with new things and tries to find their own way around before RTFM.
This approach isn't perfect but it's fun and rarely gets to a point of annoyance - I'm happy to report that Godot managed to pass this test.

![godot editor](/assets/images/godot/godot_editor.png)

I also appreciate how customizable it is. While I'm not planning to spend hours on tweaking it to perfection (at least not yet), few changes here and there were enough to make my work with the editor smoother and slightly faster.

Monitoring tools are also a plus - I haven't used them extensively yet but playing around with them gave me a rather positive impression on what's available.

Leaving UI and moving to more general things, I found the overall workflow to be relatively easy to grasp. Most of my problems so far come from inexperience rather than steps required being convoluted or difficult.
Various types of nodes and objects are clearly defined which is great for understanding things and can make searching through your scene hierarchy quicker.

I mentioned working with physics as a negative before but there is one thing I do like about Godot - being able to set monitoring/being monitored separately for each layer. It's something I already found to be useful for some of my game elements and I can't wait to see what interesting things can be done with that.

I would also like to give a warm shout-out to the [documentation](https://docs.godotengine.org/en/stable/). It's been really helpful so far and allowed me to create a basic prototype quickly and without too much trouble (outside issues caused by myself). I don't know how extensive it is when it comes to more advanced topics but so far I'm quite happy with what I saw.

## Conclusion

There it is, my first impressions of Godot.

It might seem like I'm being rather negative towards the engine but that's mainly due to unfamiliarity with it and constant (mostly unintended) comparisons with Unity. I simply haven't used it enough to find all the neat stuff available here.

It's not perfect by any means but that's not exactly a damning conclusion. Starting with it was definitely a bit rougher than anticipated but it didn't end with complete bouncing off like my short stint with UE3 and this on its own is promising.

There's a lot I don't know. There's a lot I'm mistaken about. There's a lot to simply get used to.<br>
I'm sure with time my thoughts on this engine will morph and adjust accordingly. I'm certainly willing to push through and see what else it has in store for me.

Let's hope it pays off.