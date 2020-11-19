



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

##### Post-installation Note:
##### :black_small_square: This HUD uses on-screen buttons, and so needs to be able to use your mouse. The only way to keep DU from trying to use your mouse for input is to set the Control Scheme to Keyboard. You can then right click the seat, Advanced -> Edit LUA Parameters and find the checkboxes to choose which control scheme you would actually like to use.

[Return to Table of Contents](#table-of-contents)

# Usage
#### The HUD makes use of on-screen buttons and keyboard controls. An overview followed by more detailed destriptions is below:

| Item | Key(s) | Brief Description|
| --- | --- | --- |
|UI Overlay|Hold SHIFT|Displays the UI overlay with mouseover buttons. Mouse over a button and let go of SHIFT to select it.|
|Toggle autopilot targets |Hold SHIFT, press R/T (speedup/speeddown)|Cycles through between autopilot targets.|
|Free Look|ALT|Toggles free-look. Please note that your view does not auto center when exiting Free Look.  Free Look must be enabled to zoom in 3rd person mode.|
|Autopilot Destination|Option 1 and Option 2, <br/>ALT-1 and ALT-2 or <br/>SHIFT-R and SHIFT-T)|Cycles through autopilot destinations (planets / bodies / saved waypoints).|
|Toggle HUD|Option 3, or ALT-3|Toggles the primary hud display HUD on/off.|
|Autopilot|Option 4, or ALT-4|Engages the autopilot if a destination is set. :warning: Ensure you have LOS (line of sight) before autopiloting to another planet / body.
|Lock Pitch|Option 5, or ALT-5|Will lock your target pitch at current pitch and attempt to maintain that pitch (this is different from Altitude Hold) Most other AP features will cancel Lock Pitch.
|Altitude Hold|Option 6, or ALT-6|Toggle the altitude hold functionality. Set hold height with LALT-C (down) and LALT-SPACE (up).|
|Save / Clear Databank Settings|Option 7, or ALT-7|Save or clear the currently saved configuration settings.|
|Follow Me|Option 8, or ALT-8|Engage follow mode if you are using Remote Control.|
|Anti-gravity Generator|ALT-G (default mapping) or <br/>HUD button|Once engaged, hold ALT+C to lower target height or ALT+Space to raise target height.|

| Item | Detailed Description|
| --- | --- |
|UI Overlay|Hold SHIFT to show the UI overlay with buttons. Mouse over a button and let go of SHIFT to select it. While holding SHIFT, press R/T (speedup/speeddown) to cycle between autopilot targets.|
|Free Look|ALT is now a toggle for free-look. Because of the way we had to use Keyboard mode, it can't re-center when you lock it back, but that can be desirable in some situations|
|Radar|Radar indicates below minimap number of targets or if it is jammed (atmo in space or space in atmo). The radar widget only pops up if targets are detected. The periscope widget only pops up if you click a target and successfully identify it. All widgets close automagically.|
|Destination Select|ALT-1 and ALT-2 (Option1 and Option2) to scroll between target planets for Autopilot and display. This also works using SHIFT-R and SHIFT-T to scroll. This widget will not display if no planet is selected (ie you must press one of these hotkeys after entering the seat in order to show the widget)|
|HUD Toggle|ALT-3 toggles the HUD and other widgets off/on. Orbital display and autopilot information will still show if hud is off. There is a parameter you can set to have HUD and Widgets on at same time.|
|Autopilot|ALT-4 to engage Autopilot for interplanetary travel, if you are in space and have a planet targeted. Ensure you have a clear line of sight to the target. This will align to the target, realign slightly to point 200km to the side of the target, accelerate, cut engines when at max, start braking when appropriate, and hopefully achieve a stable orbit around the target. You can set your target orbit distance in parameters, default is 100km. Recommend do not go less then 35km.
|Lock Pitch|Option 5, or ALT-5 will lock your your target pitch at current pitch and attempt to maintain that pitch (this is different from Altitude Hold) Most other AP features will cancel Lock Pitch.|
|Altitude Hold - MaxPitch affects all of the below, autotake off, landing, and re-entry. Default value is 20 degrees.|ALT-6 to toggle Altitude Hold. If used while flying (with gear up), this will attempt to hold at the altitude you turned it on at and put you in cruise control at current speed. You can modify target height with LALT+C (down) and LALT+spacebar (up). Cruise speed is modifiied like normal. Hitting ALT-6 again or tapping brake will take stop Alt-Hold mode but leave you in cruise control. ALT-6 while landed (with gear down) to turn on Auto Takeoff - this is simply Altitude Hold that sets you to a paramater-defined distance above your starting position (default 1km). You must control your own thrust and release the brake to takeoff. G (Gear) is a very loaded key. While in atmosphere it will attempt to Brake Land if your brakes are strong enough (stop you and float to ground). If not it will attempt to coast land (angle down till slow enough and within hover/vbooster height then land). If in space it will initiate re-entry to a specific altitude (2500m by default) at a specific re-entry speed (1050km/hr default). You may modify the target values via Edit LUA Parameters, or use alt-C and alt-spacebar to lower and raise target height, and mousewheel to change target cruise speed.|
||Save/Clear Variables in Databank|ALT-7 to Wipe variables in a databank, you must press it a second time to confirm - Hitting ALT-7 2x will wipe all data except saved locations from databank. To wipe saved locations you must select them as a target and then use Clear button shown while holding shift. Or you can pick up the databank, remove dynamic properties, and then put it back down, this clears everything from it.|
|Follow Mode|ALT-8 will toggle Follow Mode when using a Remote Controller. This makes your craft lift off and try to follow you wherever you go. It will not go below ground unless you dig out a big enough hole that it would naturally go down while hovering.|
|Toggle Gyro|ALT-9 to engage Toggle Gyro. If a gyro is installed on your ship, this will change your ships perceived orientation from Core to Gyro. This is used to allow you to control flight based on gyro orientation and not core orientation.

Auto-Brake is not on the UI this version; it is unreliable because it is unable to align your trajectory, and tends to over-brake if it's not perfectly aligned.|
|Persistence|As mentioned briefly above, your custom variables are saved between reloading configurations if you attach a databank to the ship (and use Alt+7 to save them). However, all variables in the program are saved in the databank when you exit the seat. This means it will be exactly as you left it - if you were landed when you got out, it won't jump off the ground when you get it.

This also means that when using autopilot, you can relatively easily move between a seat and Remote Controller; it will be down for a short time while you swap, but everything is saved and it will pick up where it left off.|

[Return to Table of Contents](#table-of-contents)

Blah blah blah





### Credits

Rezoix and his HUD - https://github.com/Rezoix/DU-hud

JayleBreak and his orbital maths/atlas - https://gitlab.com/JayleBreak/dualuniverse/-/tree/master/DUflightfiles/autoconf/custom

Archeageo and his work on the HUD

[Return to Table of Contents](#table-of-contents)

