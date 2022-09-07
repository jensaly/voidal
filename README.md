# Voidal
Release builds for Voidal, an Aurora 4x clone written in C++.


# Setup instructions

## Windows

Ensure your OpenGL drivers are version 3.0 or newer (if you update your graphics drivers with the semblance of regularity, this should be sorted). Ensure that saves and lists are in the correct place. You should set your window scaling to 100% ("make everything bigger"), as otherwise the GUI elements will look wrong.

## Linux

The distributed version is built on Ubuntu 20.04 with Glibc 2.31. Your system must be compatible with that. voidal.txt provides a command to dynamically link to the runtime SDL library provided, and then run the game (this will be sorted in future).

# Known issues
- The UI is not DPI aware
- The UI is, at times, misaligned by a few pixels and may have buttons slightly outside the windows
- The circles indicating assignment in the missile launcher assignment window may sometimes stick after closing, unless the window is moved
- Engines use raw He-3. This is placeholder
- Table borders are occasionally too small or to large for their content
- Text for explosions and impacts will overlap with other hostile ships if they orbit the same body
- The Swarm AI doesn't do anything but acquire resources
- The GU window in the ship designer redirects to the armor window (GU-functionality in the design phase is not yet implemented)
- The Armor window is very unfinished
- Citizen information and map overview does nothing (these are part of an advanced population system that is currently on hold)
- GU training has no content (GUs are not fully implemented)
- The QRH is incomplete
- Mining is very unbalanced, and the ratio of mined minerals to construction consumption is out of line
- Certain events come in clusters and others come as individuals. This is in the process of being reworked. I would like feedback on what is preferable, Aurora's style or this style.
- "Damage release switch" for missile launchers does nothing, and "Partial loading" does not yet have its drawback implemented
- Missile agility not implemented
- Missiles always hit. This is for debug purposes.
- For enough modifiers and long enough names, the displayed names of components will go beyond the windows they are displayed in
- Planets and bodies do not overlap their orbital tracks/orbital tracks are cosmetic and do not match when zoomed in far enough. This is to save performance, a workaround will come in the future.
- There are too many significant digits in many numbers
- Portals and Debug Window have been reported to crash the game on a minority of computers
And there will inevitably be crashes.