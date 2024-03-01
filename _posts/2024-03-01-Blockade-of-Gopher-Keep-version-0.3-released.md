---
layout: post
tags: block_breaker release
title: Blockade of Gopher Keep - Version 0.3.0 Released!
excerpt_separator: <!--more-->
---
![placeholder logo](/assets/images/block-breaker/logo_placeholder.png)

Welcome back!

It's time for another release of ["Blockade of Gopher Keep"](https://da-i0.itch.io/blockade-of-gopher-keep). There's plenty of new stuff, updates and bug fixes so let's get straight to it.
<!--more-->

## It's a game?!

First things first, we have a versioning change - BoGK is no longer a prototype!

I know this sounds like I'm making a big deal out of nothing but until this release, BoGK never really felt like a "real game".<br>First it was a prototype to try out an idea, then a prototype to try out a new engine - now it's another release leading us closer and closer to a full product.

It's more of a symbolic change than anything else but going forward I'll be switching to the [semantic versioning](https://semver.org/).

## How did it go?

The main focus for this release was on the technical aspects of the game.

I tried to make everything work and feel better as well as make implementing new content easier in the future. The biggest visible changes from player's perspective will most likely be the addition of new skills. I tried to keep them both varied enough and reasonably useful but wider testing is required if I were to come up with a proper conclusions on that.

Besides that I did a full menu pass to improve usability and allow for (near) full keyboard/controller navigation of all available screens.<br>Reworked game setup screen is also an important change as it allows for a simpler and faster jump into the game proper.<br>We also have some smaller quality of life changes, including (but not limited to): pagination status for paddle/skill/difficulty panels, text values for game settings with slider controls and info prompts when saving settings/changing stages.<br>
There are still some issues, like the lack of on-screen keyboard for gamepad users or some missing prompts and navigation tips but we're getting there.

I also spent some time working on more accessibility settings which brought addition of color customization for main brekable objects and an alternative font choice.<br>The latter will require additional work to polish and fix various theming issues, however I hope even its current implementation will be "good enough" for those that actually need it.

Non-english localizations are still only at a partial stage but were updated with new lines and improvements.

Last but not least, we've got quite a few bug fixes!

I managed to take care of ball "sliding" on paddles as well various UI issues that somehow slipped by last time, despite testing for them specifically.

All in all, things should be much better now.

## Patch notes

**Added:**
- 7 new levels
- 3 new skills: ball control, emergency net, power ball
- new paddle: split (experimental)
- new interactable: speed pad
- new difficulty: very hard
- new difficulty modifiers: pickup speed multiplier, advancing speed (each destroyed breakable increases ball speed)
- new UI & user settings
- new accessibility settings
- bonus points for clearing stages without losing a life
- stage clear panel with score bonus summary
- new map tile variants
- new visual effects
- new music tracks and playlist shuffle

**Changed:**
- updated Godot Engine to version 4.3 dev 3
- paddle collision improvements
- skill readiness from time delay to breakable destruction
- minor difficulty adjustments
- various level changes
- various UI improvements: new game setup screen, pagination status, layout changes and more
- improved keyboard/gamepad menu navigation
- localization improvements

**Fixed:**
- ball slides over paddle when colliding under very small angle
- language selection doesn't appear on first launch
- difficulty removal button not working
- control settings partially obscured by category buttons when using German or Japanese language
- exit prompt displays mouse controls regardless of used control method
- stage music is fully randomized, might select the same song multiple times
- [Steam Deck] game is zoomed in, with about half of the window visible on screen

**Known issues:**
- some UI layout issues when using OpenDyslexic font
- no on-screen keyboard for text boxes when using a controller
- ball bounce animation appears frozen when triggered too often
- [Steam Deck] random frame spikes
- continuous lack of gophers

## Conclusion

Despite my initial fears and some rough times along the way, project is moving forward surprisingly smoothly. There are some pretty big features planned in the future so stay tuned for that!

For now however, I hope you'll enjoy this release.

<iframe frameborder="0" src="https://itch.io/embed/2244493?bg_color=ab5675&amp;fg_color=ffe7d6&amp;border_color=73464c" width="552" height="167"><a href="https://da-i0.itch.io/blockade-of-gopher-keep">Blockade of Gopher Keep by .〇.</a></iframe>