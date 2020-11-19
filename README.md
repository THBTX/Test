



# DU-Orbital-Hud
## A general purpose HUD for Dual Universe
#### Cockpits are *NOT* supported.
###### For assistance, see our [Discord](https://discord.gg/sRaqzmS)

# Table of Contents
| |
|------|
| [Features List](#features-list) |
| [Change Log](./ChangeLog.md) |
|[Warnings](#warnings)
|[Installation](#installation)|
|[Usage / Hotkey Reference](#Usage)
| [Credits](#credits) |

# Features List

| HUD (Heads-Up) | Autopilot | Brakes|
| --- | --- | --- |
Artificial horizon | Automatic braking | Brake-hold
Altimeter | Autopilot to saved locations | Brake landings (brake force > construct mass)
Pitch | Inter-planetary transit routes |Coast landings (brake force < construct mass)
Roll | Orbital insertion | 
Yaw | Transit-to-orbit | 
Vertical speed indicator |   | 


| Additional Features | 
| --- |
|Parachute Re-Entry or Glide Re-Entry|
|Trip odometers and information display.|
|Fuel level displays for all types of fuel tanks. Ability to unslot fuel tanks to save slots.|
|Altitude hold, pitch hold, auto-landing and takeoff functionality.|
|Orbital alignment and maneuver assistants.|
|Radar and periscope for situational awareness.|
|Emergency Warp if target too close or has lock on you.|
|Ability to hide the built-in display windows to keep your flight aesthetic clean and focused.|
|Free-look mode.|
|User Parameters for customizing to your HUD and your flight preference to your ship capabilities.|
|Save parameters between HUD version updates (requires databank).|

[Return to Table of Contents](#table-of-contents)

# Warnings

##### DISCLAIMER: We do not accept any responsibility for incorrect use of the autopilot, which may result in fiery reentry, mountain impacts or undesired entrance into PvP. Read and heed the warnings below!

##### :warning: Auto-Land - Use with supervision. Will only engage if brakes > mass. Uses brakes and hovers / vertical engines to lower you to a safe landing. 
##### :warning: Autopilot - Not suitable for trips less than 2SU. Ensure you have LOS (line of sight) to the target body before engaging as autopilot is direct flight and does not detect bodies (will fly into a planet / body if in between starting position and destination).
##### :warning: Autopilot to Saved Location - Accurate withing roughly 15m of saved and selected location assuming a brake landing is available. If Coast Landing is displayed, you will need to resume control upon arrival at your destination.
##### :warning: Auto-Rentry - Not suitable for bodies without atmosphere. Not suitable for bodies with high altitudes (Thades, etc.). Know the altitude of the surface before using. Alt+Space and/or Alt-C may be used to adjust hover altitude as needed.

[Return to Table of Contents](#table-of-contents)

# Installation

##### Pre-installation Notes:

##### :black_small_square: Button - If manually connected to the seat, will be pressed when you enter (sit), and open / extend when you exit (stand).
##### :black_small_square: Databank - Although not required, we recommend a databank be used.  This allows the HUD to save your user preferences and some long-term variables.  In addition, flight status is saved if you leave and return to the seat.
##### :black_small_square: Doors / Forcefields - If manually connected to the seat, will close / retract when you enter (sit), and open / extend when you exit (stand). Ensure they are closed / retracted before connecting to the seat.
##### :black_small_square: Fuel tanks - If _not_ manually connected provide a rough estimate of fuel levels. If manually connected, more accurate readings are provided and a non-HUD widget is updated.

## On the right side of this page, locate and click on "Releases" or select the "Release" listed as the latest.  Detailed installation instructions are located there.

[Return to Table of Contents](#table-of-contents)

# Usage
#### The HUD makes use of on-screen buttons and keyboard controls. An overview followed by more detailed destriptions is below:

| Item | Key(s) | Brief Description|
| --- | --- | --- |
|UI Overlay|Hold SHIFT|Displays the UI overlay with mouseover buttons. Mouse over a button and let go of SHIFT to select it.|
|Toggle autopilot targets |Hold SHIFT, press R/T (speedup/speeddown)|Cycles through between autopilot targets.|
|Free Look|ALT|Toggles free-look. Please note that your view does not auto center when exiting Free Look.  Free Look must be enabled to zoom in 3rd person mode.|
|Autopilot Destination|Option 1 and Option 2, ALT-1 and ALT-2 or SHIFT-R and SHIFT-T)|Cycles through autopilot destinations (planets / bodies / saved waypoints).|
|Toggle HUD|Option 3, or ALT-3|Toggles the primary hud display HUD on/off.|
|Autopilot|Option 4, or ALT-4|Engages the autopilot if a destination is set. :warning: Ensure you have LOS (line of sight) before autopiloting to another planet / body.

[Return to Table of Contents](#table-of-contents)

AUTOPILOT DESTINATION (Option 1 and Option 2, ALT-1 and ALT-2) - Cycle between destination planets for the autopilot. You may also use SHIFT-R and SHIFT-T, as described above.
TOGGLE HUD (Option 3, ALT-3) - Toggles the primary hud display HUD on/off
AUTOPILOT (Option 4, ALT-4) - Engages the autopilot if a destination is set and you are in space.
TURN & BURN (Option 5, ALT-5) - Will use the main engines in addition to retro-rockets to perform braking when necessary.
ALTITUDE HOLD (Option 6, ALT-6) - Toggle the altitude hold functionality. Set hold height with LALT-C (down) and LALT-SPACE (up). Disable
SAVE/CLEAR SETTINGS (Option 7, ALT-7) - Save or clear the currently saved configuration settings.
FOLLOW MODE (Option 8, ALT-8) - Engage follow mode if you are using Remote Control
ANTIGRAVITY GENERATOR - Engaged either by button or ALT-G (unless remapped). Once engaged, hold ALT+C to lower target height or ALT+Space to raise target height.



Blah blah blah





### Credits

Rezoix and his HUD - https://github.com/Rezoix/DU-hud

JayleBreak and his orbital maths/atlas - https://gitlab.com/JayleBreak/dualuniverse/-/tree/master/DUflightfiles/autoconf/custom

Archeageo and his work on the HUD

[Return to Table of Contents](#table-of-contents)

