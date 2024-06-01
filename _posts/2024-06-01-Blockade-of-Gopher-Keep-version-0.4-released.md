---
layout: post
tags: block_breaker release
title: Blockade of Gopher Keep - Version 0.4.0 Released
excerpt_separator: <!--more-->
---
![placeholder logo](/assets/images/block-breaker/logo_placeholder.png)

I'm back with another release of ["Blockade of Gopher Keep"](https://da-i0.itch.io/blockade-of-gopher-keep)!

Check inside for all the meaty details about the new additions.
<!--more-->

## Overview

As some of you may remember, Blockade of Gopher Keep was initially developed on Unity - an engine I was very familiar and comfortable with. My move to Godot was planned as a future thing which suddenly change to "now" bringing a host of surprises I wasn't entirely prepared for.<br>While not completely different, switching to Godot required some changes to my workflow and approach to the code - both of those things are a net positive overall but transition period wasn't something I cold avoid.

Because of that, my work until now contained a lot of mistakes, some code related, some having to do with how I set up stuff in the editor. Long story short, I had quite a bit to fix for this release.

I also did some design and preliminary work on a secondary game mode which may or may not make it into the next version. That said, this isn't a completely technical patch - there are some neat additions and improvements visible from player's perspective.

## Technical stuff

As already mentioned, I spent quite a bit of time reworking the code. There's some optimization, bug fixes and rewriting of parts that didn't work great or just had to be changed to allow for more flexibility. These changes should take care of most of the frame spikes present in the previous versions of the game and make some of the gameplay features more robust. I also found and fixed a few more bugs that made it into 0.3 release cycle - none of them were game breaking which is why I didn't bother with hotfixes beyond patch .2 but I tried to catch as many as possible for this version.

Besides that, I remade some of the editor related object setup. These changes are mostly for my own benefit as they allow me to simplify and automate some of the work I have to do for each new addition.


## Content

Enought tech generalities, it's time for player-facing content!

![Enemies!](/assets/images/block-breaker/v-0-4/enemy_presentation.webp)
> Current enemy types: basic, defender, deflector.

The main new addition this time is the introduction of enemies. They are pretty simple, all things considered, but should provide a bit more dynamism and variety to the gameplay.
There are three types of foes:
- Basic - pretty much a walking target
- Defenders - they'll block your balls using their big shield, can't be hurt from the front
- Deflectors - similar to defenders with the addition of countering your attacks, ball hitting them from the front will be returned with a small temporary speed boost

Enemies use placeholder sprites as I'm still thinking on what kind of design I'd like them to take, they do however have all the necessary animations and actions planned for these variants.

![New tileset](/assets/images/block-breaker/v-0-4/03.png)
> New tileset!

Next on the list are the new graphical elements. There's a new tileset (room), 6 new (and 3 old) stages to show it off as well as new props (barrel, various potted plants and small organ - the musical kind).

On UI side, I changed the stage clear panel activation - instead of triggering when the exit timer runs out it'll wait until ball reaches the exit door. This was done to unify the gameplay with how it works when this panel is turned off - it allows players to disregard the timer to clear the rest of the level in search of pickups.

## Bonus features

On a less... "contenty" side I brought another gameplay addition: session modifiers.<br>
These things allow you to do stuff like set session length, randomize stage order, disable pickups and turn on the disappearing balls (the closer one is to the paddle the more transparent it becomes). The latter two increase the score multiplier and might help when hunting for a new high score.

![Color palettes](/assets/images/block-breaker/v-0-4/palettes.webp)
> Color palette comparison.

Another new inclusion is the color palette support.<br>
I realize that some color combinations might be a bit rough for people with color blindness so I wanted to add even more options to make the game playable for them. Well, that and some players might simply like the new colors more than the original ones.<br>
This addition brings two new video settings - separate palette choice for stage backgrounds and interactable elements (blocks, breakable objects, teleport doors, etc.).<br>As always, I want people to be able to customize the experience to their needs.

Besides that there's also an optional CRT filter - it's more of a novelty addition but why not? Might need some additional tweaking in the future.

## Patch notes

**Added:**
- 6 new stages.
- Enemies (basic, defender, deflector).
- Play session customization: session length, randomize stage order, disable pickups, disappearing ball.
- Bonus score for completing play session and killing all enemies.
- New tileset.
- New props.
- Support for palette swaps with 2 new color palettes (Autumn, Muted), separate settings for stage and interactables.
- Optional CRT filter.
- New localization entries.

**Changed:**
- Updated target framework from .Net 6.0 to 7.0.
- Increased max multiplier for "Advancing Speed" from x1.5 to x2.
- Add instead of replacing the temporary boost value of balls caught in an explosion.
- Removed max score multiplier limit.
- Replaced English language names with localized versions.
- Stage background brightness to use color instead of transparency.
- Made "Shake" skill debris use "Effect Transparency" setting.
- Various visual and layout adjustments for all stages.
- Switched few stage backgrounds to the new tileset.
- Various art adjustments.
- Various theme improvements.
- Menu navigation improvements.
- Slightly reworked the leaderboard screen.
- Trigger the stage clear panel on reaching the exit door instead of after exit timer runs out.
- Minor adjustments to default game settings.

**Fixed:**
- General code improvements and optimization.
- Lots of game object setup and implementations.
- Random frame spikes.
- "Advancing Speed" not triggering properly after death or ball reset.
- Cloned balls don't copy all of the speed multiplier values.
- Exit timer doesn't stop on return to menu.
- Ball bounce animation appears frozen when triggered too often.
- Ball keeps animating when using "Ball Control" skill.
- Ball speed trail isn't cleared when teleporting.
- Incorrect ball animation speed on release.
- Incorrect water tiles in stage 28.
- Some map details aren't affected by background brightness setting.
- Exit prompt doesn't update its keybind to current active controller type.
- Pause menu retriggering when canceling out with a keybind.
- Player name field on game over/win panel doesn't reset between sessions.
- Couple translation errors.

**Known issues:**
- Some UI layout issues when using OpenDyslexic font.
- No on-screen keyboard for text boxes when using a controller.
- CRT filter doesn't affect dropdown lists in the settings menu.
- Continuous lack of gophers.

### Conclusion

While I'd like to say that BoGK is ready to fully switch into the content creation mode there's still a lot of technical work waiting to be done.

The good news is that I have a pretty complete vision on what features and how much content I'd like to have before releasing the 1.0 version and won't have to scramble in panic thinking what to do next. All that's left is implementing all of it. Yay?

That's all for now. Hope you all have fun with this release!

<iframe frameborder="0" src="https://itch.io/embed/2244493?bg_color=ab5675&amp;fg_color=ffe7d6&amp;border_color=73464c" width="552" height="167"><a href="https://da-i0.itch.io/blockade-of-gopher-keep">Blockade of Gopher Keep by .〇.</a></iframe>