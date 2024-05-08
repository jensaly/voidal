# Voidal
Release builds for Voidal, an Aurora 4x clone written in C++.

Current version is 0.4.0. 

Discussion and future updates on Reddit: https://www.reddit.com/r/voidal/

# Setup instructions

## Windows

Ensure your OpenGL drivers are version 3.0 or newer (if you update your graphics drivers with the semblance of regularity, this should be sorted). You should set your window scaling to 100% ("make everything bigger"), as otherwise the GUI elements will look too large and blurry (still playable).

## Linux

The distributed version is built on Ubuntu 20.04 with Glibc 2.31, and tested on that version of Ubuntu as well as Arch. You will likely need to download SDL2 with your package manager.

## Getting started

The inital screen you are presented with will allow you to set up basic parameters of the game and the galactic topology. The most important option here is the "Debug start". Keeping this unchecked will start the game at the very beginning, with no technology beyond the basics researched, no ships, and only a starting set of installations. Checking this box will research all technology and start the game with a handful of ships fulfilling different purposes. As the name suggests, this allows playing around with larger-scale mechanics.

Voidal draws inspiration from Aurora, so familiarity with Aurora's UI and mechanics is presupposed. Coming QoL changes will address the learning curve with the UI without sacrificing complexity.

The QRH (quick reference handbook) functions as a small, built-in wiki.

# Screenshots

(The below is taken from v0.1.0, the previous public release. New material will be added shortly.)

[Demo video](https://www.youtube.com/watch?v=fUWFZTmYYIg)

![mainwindow](https://user-images.githubusercontent.com/91413827/188991877-6aac5c2c-ab55-4b83-ae8b-573801a6d618.PNG)
![fleetsinmotion](https://user-images.githubusercontent.com/91413827/188991879-46beae76-0100-46fe-8767-9a00561618f8.PNG)
![ship design](https://user-images.githubusercontent.com/91413827/188991882-a1627990-81e5-416e-aa57-a094a631d83a.PNG)
![missiles](https://user-images.githubusercontent.com/91413827/188991884-020b6db3-c65c-4c88-b4b7-2e907bd98130.PNG)
![combat](https://user-images.githubusercontent.com/91413827/188991887-1c7ce512-340f-4ded-a938-a8a9a0b19c84.PNG)

# Brief release notes

## Galaxy generation

The galaxy is generated in a manner determined by the seed provided at the start of the game. It consists of hundreds to thousands of star systems, naturally connected to one another by jump points. Depending on the generation settings, the entire galaxy may be connected by jump points such that any path can be taken between them, or the galaxy could be generated in "clusters" of stars.

## Interstellar travel

Interstellar travel comes in three forms:
 - Jump drives: Move instantaneously between pairs of connected jump points, but only between these jump points.
 - Warp drives: Can travel anywhere without considerations of the jump points, but at a fixed speed.
 - Portals: Artificial jump points that can be installed anywhere, but which have to be moved into place normally before being used.

## Weapons & Turrets

Two first forms of hitscan weapons:
 - Coilguns: Coilguns are rapid-fire kinetic weapons. They fire rapidly and with a low base accuracy, and their damage does not scale rapidly with technology level. They make up for it by being lightweight and having a rate-of-fire that scales quickly, pumping out projectiles.
 - Pulse lasers: Pulse lasers charge up capacitors from a reactor and releases it in a blast of energy. The damage drops off quickly by the inverse square law, so they shine when up close and personal.

 The accuracy of these weapons is decided primarily by the range to their target and the relative speed between the attacker and the defender. A raw hitscan weapon is therefore best mounted on a fast ship. However, hitscan weapons can be mounted on turrets, replacing the speed of the attacker with a built-in tracking speed.

## Stability fixes

Many behind-the-scenes reworks to improve stability, and an uncountable number of bug fixes.

# Known issues

- The UI is not DPI aware. It is therefore recommended that the size of apps is kept to 100% and not above.
- Certain parts of the UI are a little rough.
- The UI is currently not flexible and built to be serviceable on 1920x1080p monitors. Larger resolutions should have no issue, however smaller resolutions may have to move windows around a lot. All of these will be addressed in a future update.
- The player has access to the portal debug crosshair in normal game. This is an oversight.
- Text for explosions and impacts will overlap with other hostile ships if they orbit the same body.
- The Swarm AI is placeholder, and a better AI will be implemented in a future update.
- Armor is not yet fully implemented, and as a result the screens are left purposefully empty.
- GUs cannot be trained. You are given a set on start.
- "Damage release switch" for missile launchers does nothing, and "Partial loading" does not yet have its drawback implemented.
- For enough modifiers and long enough names, the displayed names of components will go beyond the windows they are displayed in
- Planets and bodies do not overlap their orbital tracks/orbital tracks are cosmetic and do not match when zoomed in far enough.
- There's a hard cap on the game at 10000 years.
