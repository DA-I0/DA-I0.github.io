---
layout: post
tags: prototype block_breaker
title: Blockade of Gopher Keep - Prototype 2 Released!
excerpt_separator: <!--more-->
---
![placeholder logo](/assets/images/block-breaker/logo_placeholder.png)

It's real. It's finally here! The second prototype of “Blockade of Gopher Keep” is out and ready to be played!

Time to dive into what's new, what changed and what stayed the same.
<!--more-->

## Trials and tribulations

Some of you might know about the drama around Unity from few months ago - company tried to push through some really shady changes to the license agreement with no prior warning or clear communication about how exactly they suppose to work.

While these changes wouldn't affect me personally, and were somehow reined in after the backlash, this attempt was the final straw after years of pretty lackluster support for the core engine, canceled projects and empty promises.

It was time to act. It was time to look for greener pastures.

## Godot: The Sequeling

I've already posted about trying out Godot before - my attempt was painful, full of crashes and corrupted files. While it wasn't a good start I didn't want to give up on this engine.<br>Not yet anyway.

That's were Godot 4 comes in.

After the release of version 4 and previously mentioned Unity problems I decided to give it another go. Porting of the first BoGK prototype went surprisingly smoothly - while some thing had to be rewritten, a lot of basic elements worked pretty much out of the box.<br>
I did have to get used to the new workflow but even that wasn't as painful or problematic as my first experience with the engine.
What's more, this switch pushed me to improve the original code in multiple ways I didn't anticipate and should allow me to create a much better game on a technical level.

It's not all perfect obviously.

While I did manage to port and expand on the project to a point of another public version, there are some growing pains I wasn't able to avoid. Non of the issues present in Prototype 2 are game breaking and I'll do my best to smooth them out in the future, but they are there so be ready for some occasional jank.

## Patch notes

**Added:**
- 13 new levels
- difficulty settings: 3 default presets + customization
- new paddles: armed, curved, roguelike, bounce control
- new pickups: bouncy paddle, freeze paddle, sticky paddle, reverse controls, slow ball
- new breakables: chairs, explosives, fences, graves, pumpkins, tables
- new decorations: benches, bookcase, candle stand, paintings, windows, wardrobes
- new tileset: garden
- new visual effects
- player skill: screen shake (use it to shake the screen which randomly changes ball rotation and freezes paddle for a short time)
- game over screen
- local leaderboard
- localization support, partial localization for German, Japanese and Polish languages
- new user settings

**Changed:**
- switched from Unity to Godot Engine
- ball collision improvements
- adjustments to original levels
- default tileset improvements
- UI layout and theming

**Fixed:**
- fullscreen toggle doesn't update to loaded state
- weird ball collisions

**Known issues:**
- stage music is fully randomized, might select the same song multiple times
- ball slides over paddle when colliding under very small angle
- some UI elements require mouse to navigate
- control settings partially obscured by category buttons when using German or Japanese language
- [Steam Deck] game is zoomed in, with about half of the window visible on screen
- continuous lack of gophers

**Important note:**
If you played the Unity version (Prototype 1) make sure to remove the "DA-I0" folder created by the game. You can find it at:
- Linux: ~/.config/unity3d/unity3d/DA-I0
- Windows: C:\Users\<user_name>\AppData\LocalLow\DA-I0

## Conclusion

It was a rough 3 months. Not because of the game but mostly IRL stuff that did have some effect on progress (or lack thereof at times). Despite this, the new public version is here and that's something I wasn't sure I'll be able to type.

It might be small, it might be incomplete but it's mine and I'm sure as hell proud of what I achieved so far.

The next public version will be a proper alpha (version wise).<br>My development plan for now is to stick with one update every three months while I work on the systems and switch to a monthly release schedule after we hit beta.<br>
I have no idea how this will pan out, but that's the plan. Wish me luck.

*"Blockade of Gopher Keep" can be downloaded for free on [itch.io](https://da-i0.itch.io/blockade-of-gopher-keep).*