---
layout: post
tags: prototype block_breaker
excerpt_separator: <!--more-->
---
![placeholder logo](/assets/images/block-breaker/logo_placeholder.png)

I'm still alive and kicking so it's time for another post!

Last time I mentioned taking a break from Godot and doing some work on my older prototypes - the latter is exactly what I want to write about today.

Let's talk about my block breaker prototype, also known as "Blockade of Gopher Keep".
<!--more-->
> ### Quick navigation:
[Intro](#so-block-breaker-games-eh) | [Prototype](#prototype) | [Gameplay](#gameplay) | [Levels](#levels) | [Pickups](#pickups) | [Level "hazards"](#level-hazards) | [Conclusion](#conclusion)

## So... block breaker games, eh?

Back in the old days of 1980s... Nah just kidding. This isn't a news website where I need to worry about CEO and stuff. That said, let's just add some clarification - block breaker games are those fun little titles where you control a paddle and use it to bounce a ball around the map, trying to clear all the blocks (think Arkanoid or Wizorb).

I'm not going to pretend I'm some huge fan of the genre, one who knows everything there is to know about it and wants to use that knowledge to create something completely new. Not at all.

While I do enjoy playing these games from time to time, the idea to actually make one myself came from watching [Bob Ross's video about Death's Hangover](https://youtu.be/aTxuQVIc-Z0) and thinking "this can't be THAT difficult to make, right?". Well... yesn't.

## Prototype

As the title suggests, this is just a prototype. I didn't have a full picture of what I want to make when I started working on it (truth be told, I still don't).
I **did** manage to finish a working and, more importantly, public version of the project which is already a win - one which hasn't happened in a long time.

The first released version of this project contains:
- 10 levels
- 7 pickups
- 4 level "hazards"/interactable elements

Just enough for a prototype or proof of concept release and to keep things semi-interesting throughout. I hope.

Funnily enough, while the project itself is few years old, vast majority of the work (not just polishing) happened in the last 2-3 months. It was a time when I decided to pause everything else I did and spend (almost) all of my free time pushing to finish **something** that can be presented in a playable state rather than endlessly tweaking things that never end up "good enough" for release.

Game is available for Linux and Window machines, and can be downloaded [here](https://da-i0.itch.io/blockade-of-gopher-keep).

## Gameplay

This one is simple - destroy all the blocks present on the map, reach the exit to advance to the next level.

![gameplay screenshot](/assets/images/block-breaker/bogk_02.png)

There's a little bit of variety here to keep gameplay from being completely basic. We have normal and sturdy *blocks* (require multiple hits to break). We have two types of *barriers* - indestructible and sturdy, the latter doesn't count towards completing the level but can spawn pickups unavailable in blocks (like extra lives).

*Scoring system* started as a basic "break thing, get points" kind of thing but that quickly evolved into a bit more fun creation. Right now it's based on a score multiplier which changes based on two factors: *combo* and *pickups*.<br>
Each destroyed element increases your combo counter and each 10 steps increase score multiplier (up to x5). Combo resets after losing the last ball currently at play.<br>
*Pickups multiplier* is suppose to push players towards more difficult approach - each difficulty increasing pickup (shorter paddle, faster or smaller ball) can increase the multiplier independently from your combo (currently up to x4).
Both multipliers are added together before using them to calculating the score.

Finally there's the *exit timer* - after destroying all the blocks available on each map, level exit opens and race against time begins. The faster you reach exit the more points you get as any remaining time is added to the score (with standard multiplier treatment of course). On the other hand, there might be some destructible elements left that can provide you with pickups and additional combo/score. It's up to the player to decide which to prioritize - well, that and the whims of ball(s).

## Levels

![gameplay screenshot](/assets/images/block-breaker/bogk_10.png)

While level count isn't huge at the moment there's just enough of them to present players with all the game elements without throwing everything at them at once. That's good enough for now but there's no space between introduction of each one of the elements to spread out those introductions and give more practice to people slower on the uptake.<br>
That's one of the main things I'd like to change with the next release, I'd like there to be 2-3 levels between each new element.

Another limitation of current version is the fact there's only one tileset, with all variety coming from block positioning and map decorations.
It works well enough with limited map pool available right now but it's something that will have to be addressed in the future.<br>
I actually have a partially finished second tileset but I wasn't able to finish it in time for this release (I have a general idea, still trying to figure out decent looking implementation).

I'm also planning to increase the amount of map decorations to improve on visual blandness of current maps - there're literally two of them at the moment: wall sign and column, three if you include alternative floor tiles representing carpet.

## Pickups

Pretty important part of gameplay, aren't they?<br>
Pickups not only provide variety to each play session but also allow for dynamic difficulty changes based on player decision.

![pickups](/assets/images/block-breaker/pickups.png)

Current collection of pickups consists of a rather standard set. We have:
- smaller ball
- faster ball
- extra balls (spawns 2 additional balls from each existing one)
- safety net (spawns emergency blocks right below the paddle)
- shorter/longer paddle
- extra life

I'm trying to come up with some more interesting additions for the next version but what makes it in remains to be seen.

## Level "hazards"

It's not **really** a good name for what I'm about to write about. Only one of these elements is an actual danger to the player, other ones only affect ball direction/position - this can make for some clutch moments but more as a side effect than anything else.

So what do we have?

![bollard](/assets/images/block-breaker/bollard.png){: class="img-transparent-left" }

There's *bollard* - a vertical post that pops up and down based on a timer. It's pretty much a toggleable collider which changes paths available to the ball.

<br>
![whirpool](/assets/images/block-breaker/whirpool.png){: class="img-transparent-left" }
Next is *whirpool* - a circular void that sucks the ball in and releases it at a random angle. Temporarily deactivated after each use.
<br><br><br><br><br><br>
![teleport door](/assets/images/block-breaker/teleport_door.png){: class="img-transparent-left" }
On the third place we have *teleport door* - pair of doors which transports the ball between each other. Now we're thinking with portals!

<br><br><br><br>
![coffin](/assets/images/block-breaker/coffin.png){: class="img-transparent-left" }
Last but not least, there's *coffin* - the only real hazard at the moment. It's a breakable element that releases a ghost which travels towards the bottom of the screen. Touching it costs a life so be careful!

## Conclusion

Here it is, my very first public release.

This project was always meant to be a side thing and while I do have a bunch of ideas for at least one more version I don't have any specific plans to expand it into a full game or anything like that.

Originally I was planning to publish (and possibly update) this thing then go back to my main project.

Will that happen? I don't know.

I might end up switching my priorities and making this my main time sink. I might decide to go with a similar treatment to another shelved prototype.<br>
Whatever it is, I'll try to be more open on what and how is going on. Hopefully it won't take me another six months for that to happen.