


<!--Intro information-->
# DU-Orbital-HUD
## A general purpose HUD for Dual Universe
#### Cockpits are *NOT* supported.
###### For assistance, see our [Discord](https://discord.gg/sRaqzmS)
###### Donations are accepted! We have a Donation Station in Sanctuary District 3 and more to come or you can always contact us and do a VR trade. We do not spend any time mining or building so our funds to test features are limited.
<!--TOC-->
# Table of Contents
| |
|------|
| [Features List](#features-list) |
| [Change Log](./ChangeLog.md) |
|[Warnings](#warnings)
|[Installation](#installation)|
|[Usage / Hotkey Reference](#Usage)
|[Variable Persistence](#variable-persistence)
|[Customization](#customization)
|[Examples and Tutorials](#examples-and-tutorials)
[No Autopilot Version](#no-autopilot-version)
| [Credits](#credits) |
<!--List of features both shorlist and expanded details-->
# Features List

| HUD (Heads-Up) | Autopilot | Brakes|
| --- | --- | --- |
Artificial horizon | Automatic braking | Brake-hold
Altimeter | Autopilot to saved locations | Brake landings (brake force > construct mass)
Pitch | Inter-planetary transit routes |Coast landings (brake force < construct mass)
Roll | Orbital insertion | 
Yaw | Transit-to-orbit | 
Vertical speed indicator |   | 


| Feature Detail / Additional Features | 
| --- |
|Brake indicator / toggle. Brake is now a toggle, and is on by default when entering the seat. There is an onscreen text indicator to show you when the brake is on. You can set brake to work like default with an Edit LUA Parameter setting.|
|Interplanetary Helper - Use __Alt-1__ and __Alt-2__ or __SHIFT-R__ / __SHIFT-T__ to cycle through target planets. Shows distance, travel time (including acceleration, travel, and braking - absolute total), brake time (current and max). Note that currently, Brake Time is inaccurate if you're inside atmosphere. Once you're in space, it will properly read the space brakes and give the correct values. Shows max mass for your ship on planet at sea level based on brakes. Note: If going to a planet with atmosphere, you must get the max mass reading while in atmosphere, and same if going to planet with no atmosphere.|
|Auto-Brake - Use __Alt-9__ when you have a target selected with the Interplanetary Helper, and it will toggle Auto-Brake. The script will automatically engage the brake when within the max braking distance for that planet. This does not guarantee that you will not hit the planet - even with Auto-Brake, do not aim directly at the planet. It targets an end speed of 0, though you will generally have a much higher end speed, so has some leeway. It will continue braking until stable orbit is achieved, if possible from the trajectory.|
|Dodgin's Don't Die Rocket Governor - Set your speed with cruise control and press __B__ to have your rocket engines fire up to that speed and no faster|
|Auto-Land on Gear Down - Putting down your landing gear sets your hover height to 0, raising it sets it to max. Entering a vehicle with gear down sets the height to 0, entering a vehicle with the gear up sets it to max|
|Door/Ramp Automation - Automatically closes doors/ramps when entering, and opens them when exiting. Requires you to link these to the seat once, and it will remember and relink them each time you configure it afterward. No renaming required.|
|(ButtonHUD) Buttons and custom controls - Custom implementations of virtual joystick and mouse controls, allowing you to use virtual joystick without that disgusting giant circle on your screen. Buttons to use many of the features.|
|Atmospheric Package - Auto-Takeoff, Auto-Land, Altitude Hold, and for Remote Controllers, Follow Mode|
|Fuel Tanks - These are no longer automatically slotted to seat. You still get fuel readouts under the minimap. If you want the standard fuel widget, you will need to link the fuel tank(s) to the seat one time and then run the autoconfig.|
|AutoPilot - Use __Alt-4__ when you have a target selected with the Interplanetary Helper, and you are in space with clear line of sight to the target. The script will align to the optimal vector to place you in a 1SU orbit from the target, accelerate, cut engines when appropriate, and brake until orbit is achieved.|
|Parachute Re-Entry or Glide Re-Entry|
|Trip odometers and information display.|
|Fuel level displays for all types of fuel tanks. Ability to unslot fuel tanks to save slots.|
|Altitude hold, pitch hold, auto-landing and takeoff functionality.|
|Orbital alignment and maneuver assistants and Orbital information widget which shows apoapsis, periapsis, apogee, perigee, eccentricity for the nearest planet, using these libraries: https://gitlab.com/JayleBreak/dualuniverse/-/tree/master/DUflightfiles/autoconf/custom |
|Radar and periscope for situational awareness.|
|Emergency Warp if target too close or has lock on you.|
|Ability to hide the built-in display windows to keep your flight aesthetic clean and focused.|
|Free-look mode.|
|User Parameters for customizing to your HUD and your flight preference to your ship capabilities.|
|Save parameters between HUD version updates (requires databank).|
|Manual Control HotKey|Pressing Stop engines (__Z__ by default) 2x within 1 second will clear ALL AP / special functions. You will be at 0 engine in throttle mode with brakes off. (normal __Z__ behavior) but all special features like altitude hold, or brake landing or anything else will turn off. (Give me manual control key) Pressing it just once is normal vanilla stop all engines. NOTE: This will NOT turn off antigrav or stop a warp in progress. It does turn off emergency warp active.|


[Return to Table of Contents](#table-of-contents)
<!--Warnings and disclaimers-->
# Warnings

##### DISCLAIMER: We do not accept any responsibility for incorrect use of the autopilot, which may result in fiery reentry, mountain impacts or undesired entrance into PvP. Read and heed the warnings below!

##### :warning: Auto-Land - Use with supervision. Will only engage if brakes > mass. Uses brakes and hovers / vertical engines to lower you to a safe landing. 
##### :warning: Autopilot (Space) - Not suitable for interplanetay trips less than 2SU. Ensure you have LOS (line of sight) to the target body before engaging as autopilot is direct flight and does not detect bodies (will fly into a planet / body if in between starting position and destination).
##### :warning: Autopilot to Saved Location - Accurate within roughly 15m of saved and selected location assuming a brake landing is available. If Coast Landing is displayed, you will need to resume control upon arrival at your destination.
##### :warning: Auto-Rentry - Not suitable for bodies without atmosphere. Not suitable for bodies with high altitudes (Thades, etc.). Know the altitude of the surface before using. __Alt-Space__ and/or __Alt-C__ may be used to adjust hover altitude as needed.

[Return to Table of Contents](#table-of-contents)
<!--Basic install instructions / point them towards real install instructions-->
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
<!--Table so user can quickly find keys to use-->
# Usage
#### The HUD makes use of on-screen buttons and keyboard controls. An overview followed by more detailed descriptions are below:

| Item | Key(s) | Brief Description|
| --- | --- | --- |
|UI Overlay|Hold __SHIFT__|Displays the UI overlay with mouseover buttons. Mouse over a button and let go of SHIFT to select it.|
|Toggle autopilot targets |Hold __SHIFT__, press __R__ or __T__ (speedup/speeddown)|Cycles through between autopilot targets.|
|Save Location|Hold __SHIFT__ then selecting the __Save Position__ mouseover| Will save the current location in the databank (if installed). This location may be selected by the autopilot option to automatically fly to the destination.  It will _not_ monitor for impeeding structures or ships. Monitor during use.|
|Free Look|ALT|Toggles free-look. Please note that your view does not auto center when exiting Free Look.  Free Look must be enabled to zoom in 3rd person mode.|
|Autopilot Destination / Destination Select|__Option 1__ and __Option 2__, <br/>__ALT-1__ and __ALT-2__ or <br/>__SHIFT-R__ and __SHIFT-T__)|Cycles through autopilot destinations (planets / bodies / saved waypoints).|
|Toggle HUD|__Option 3__, or __ALT-3__|Toggles the primary hud display HUD on/off.|
|Autopilot|__Option 4__, or __ALT-4__|Engages the autopilot if a destination is set. :warning: Ensure you have LOS (line of sight) before autopiloting to another planet / body.
|Lock Pitch|__Option 5__, or __ALT-5__|Will lock your target pitch at current pitch and attempt to maintain that pitch (this is different from Altitude Hold) Most other AP features will cancel Lock Pitch.
|Altitude Hold|__Option 6__, or __ALT-6__|Toggle the altitude hold functionality. Set hold height with LALT-C (down) and LALT-SPACE (up).|
|Save / Clear Databank Settings|__Option 7__, or __ALT-7__|Save or clear the currently saved configuration settings.|
|Follow Me|__Option 8__, or __ALT-8__|Engage follow mode if you are using Remote Control.|
|Anti-gravity Generator|__ALT-G__ (default mapping) or <br/>HUD button|Once engaged, hold __ALT-C__ to lower target height or __ALT-Space__ to raise target height.|
<!--Messy Messy details. This needs to be cleaned up.-->
| Item | Detailed Description|
| --- | --- |
|UI Overlay|Hold __SHIFT__ to show the UI overlay with buttons. Mouse over a button and let go of SHIFT to select it. While holding SHIFT, press R/T (speedup/speeddown) to cycle between autopilot targets.|
|Free Look|__ALT__ is now a toggle for free-look. Because of the way we had to use Keyboard mode, it can't re-center when you lock it back, but that can be desirable in some situations|
|Autopilot Destination / Destination Select|__ALT-1__ and __ALT-2__ (__Option1__ and __Option2__) to scroll between target planets for Autopilot and display. This also works using SHIFT-R and SHIFT-T to scroll. This widget will not display if no planet is selected (ie you must press one of these hotkeys after entering the seat in order to show the widget)|
|HUD Toggle|__ALT-3__ toggles the HUD and other widgets off/on. Orbital display and autopilot information will still show if HUD is off. There is a parameter you can set to have HUD and Widgets on at same time.|
|Autopilot|__ALT-4__ to engage Autopilot for interplanetary travel, if you are in space and have a planet targeted. Ensure you have a clear line of sight to the target. This will align to the target, realign slightly to point 200km to the side of the target, accelerate, cut engines when at max, start braking when appropriate, and hopefully achieve a stable orbit around the target. You can set your target orbit distance in parameters, default is 100km. Recommend do not go less then 35km.
|Lock Pitch|__ALT-5__ (__Option 5__) will lock your your target pitch at current pitch and attempt to maintain that pitch (this is different from Altitude Hold) Most other AP features will cancel Lock Pitch.|
|Altitude Hold - |__ALT-6__ to toggle Altitude Hold. If used while flying (with gear up), this will attempt to hold at the altitude you turned it on at and put you in cruise control at current speed. You can modify target height with LALT+C (down) and LALT+spacebar (up). Cruise speed is modified like normal. Hitting ALT-6 again or tapping brake will stop Alt-Hold mode but leave you in cruise control. ALT-6 while landed (with gear down) to turn on Auto Takeoff - this is simply Altitude Hold that sets you to a paramater-defined distance above your starting position (default 1km). You must control your own thrust and release the brake to takeoff. G (Gear) is a very loaded key. While in atmosphere it will attempt to Brake Land if your brakes are strong enough (stop you and float to ground). If not it will attempt to coast land (angle down till slow enough and within hover/vbooster height then land). If in space it will initiate re-entry to a specific altitude (2500m by default) at a specific re-entry speed (1050km/hr default). You may modify the target values via Edit LUA Parameters, or use alt-C and alt-spacebar to lower and raise target height, and mousewheel to change target cruise speed.|MaxPitch affects all of the below, autotake off, landing, and re-entry. Default value is 20 degrees.
|Save/Clear Variables in Databank|__ALT-7__ to Wipe variables in a databank, you must press it a second time to confirm - Hitting __ALT-7__ 2x will wipe all data except saved locations from databank. To wipe saved locations you must select them as a target and then use Clear button shown while holding shift. Or you can pick up the databank, remove dynamic properties, and then put it back down, this clears everything from it.|
|Follow Mode|__ALT-8__ will toggle Follow Mode when using a Remote Controller. This makes your craft lift off and try to follow you wherever you go. It will not go below ground unless you dig out a big enough hole that it would naturally go down while hovering.|
|Toggle Gyro|__ALT-9__ to engage Toggle Gyro. If a gyro is installed on your ship, this will change your ships perceived orientation from Core to Gyro. This is used to allow you to control flight based on gyro orientation and not core orientation. Auto-Brake is not on the UI this version; it is unreliable because it is unable to align your trajectory, and tends to over-brake if it's not perfectly aligned.|
|Radar|Radar indicates below minimap number of targets or if it is jammed (atmosphere in space or space in atmosphere). The radar widget only pops up if targets are detected. The periscope widget only pops up if you click a target and successfully identify it. All widgets close automagically.|

[Return to Table of Contents](#table-of-contents)
<!--This should go somewhere else, I'm not sure where yet.-->
## Variable Persistence
As mentioned briefly above, your custom variables are saved between reloading configurations if you attach a databank to the ship (and use Alt+7 to save them). However, all variables in the program are saved in the databank when you exit the seat. This means it will be exactly as you left it - if you were landed when you got out, it won't jump off the ground when you get it.

This also means that when using autopilot, you can relatively easily move between a seat and Remote Controller; it will be down for a short time while you swap, but everything is saved and it will pick up where it left off.|

[Return to Table of Contents](#table-of-contents)
<!--Does this really need to be in the readme, or some other file? Not sure how often a user would need this information.-->
# Customization
The following LUA parameters were added
Right click the seat and go to _Advanced_ -> _Edit Lua Parameters_ to see them all. Mouse over a name to see its purpose and potential settings.

    -- USER DEFINABLE GLOBAL AND LOCAL VARIABLES THAT SAVE
    useTheseSettings = false -- export: Toggle on to use the below preferences.  Toggle off to use saved preferences.  Preferences will save regardless when exiting seat. 
    freeLookToggle = true -- export: Set to false for vanilla DU free look behavior.
    BrakeToggleDefault = true -- export: Whether your brake toggle is on/off by default. Can be adjusted in the button menu.  Of is vanilla DU brakes.
    RemoteFreeze = false -- export: Whether or not to freeze you when using a remote controller.  Breaks some things, only freeze on surfboards
    RemoteHud = false -- export: Whether you want full HUD while in remote mode, experimental, might not look right.
    userControlScheme = "virtual joystick" -- export: Set to "virtual joystick", "mouse", or "keyboard"
    brightHud = false -- export: Enable to prevent hud dimming when in freelook.
    PrimaryR = 130 -- export: Primary HUD color
    PrimaryG = 224 -- export: Primary HUD color
    PrimaryB = 255 -- export: Primary HUD color
    centerX = 960 -- export: X postion of Artifical Horizon (KSP Navball), (use 1920x1080, it will scale) Default 960. Use centerX=700 and centerY=880 for lower left placement.
    centerY = 540 -- export: Y postion of Artifical Horizon (KSP Navball), (use 1920x1080, it will scale) Default 540. Use centerX=700 and centerY=880 for lower left placement. 
    throtPosX = 1300 -- export: X position of Throttle Indicator, default 1300 to put it to right of default AH centerX parameter.
    throtPosY = 540 -- export: Y position of Throttle indicator, default is 540 to place it centered on default AH centerY parameter.
    vSpdMeterX = 1525  -- export: X postion of Vertical Speed Meter.  Default 1525 (use 1920x1080, it will scale)
    vSpdMeterY = 250 -- export: Y postion of Vertical Speed Meter.  Default 250 (use 1920x1080, it will scale)
    altMeterX = 550  -- export: X postion of Altimeter.  Default 550 (use 1920x1080, it will scale)
    altMeterY = 540 -- export: Y postion of Altimeter.  Default 500 (use 1920x1080, it will scale)
    fuelX = 100 -- export: X position of fuel tanks, default is 100 for left side, set both fuelX and fuelY to 0 to hide fuel
    fuelY = 350 -- export: Y position of fuel tanks, default 350 for left side, set both fuelX and fuelY to 0 to hide fuel
    circleRad = 400 -- export: The size of the artifical horizon circle, recommended minimum 100, maximum 400.  Looks different > 200. Set to 0 to remove.
    DeadZone = 50 -- export: Number of pixels of deadzone at the center of the screen
    showHud = true -- export: Uncheck to hide the HUD and only use autopilot features via ALT+# keys.
    hideHudOnToggleWidgets = true -- export: Uncheck to keep showing HUD when you toggle on the widgets via ALT+3.
    ShiftShowsRemoteButtons = true -- export: Whether or not pressing Shift in remote controller mode shows you the buttons (otherwise no access to them)
    StallAngle = 35 --export: Determines how much Autopilot is allowed to make you yaw/pitch in atmosphere.  Also gives a stall warning when not autopilot.  (default 35, higher = more tolerance for yaw/pitch/roll)
    speedChangeLarge = 5 -- export: The speed change that occurs when you tap speed up/down, default is 5 (25% throttle change). 
    speedChangeSmall = 1 -- export: the speed change that occurs while you hold speed up/down, default is 1 (5% throttle change).
    brakeLandingRate = 30 -- export: Max loss of altitude speed in m/s when doing a brake landing, default 30.  This is to prevent "bouncing" as hover/boosters catch you.  Do not use negative number.
    MaxPitch = 30 -- export: Maximum allowed pitch during takeoff and altitude changes while in altitude hold.  Default is 20 deg.  You can set higher or lower depending on your ships capabilities.
    ReentrySpeed = 1050 -- export: Target re-entry speed once in atmosphere in m/s.  291 = 1050 km/hr, higher might cause reentry burn.
    ReentryAltitude = 2500 -- export: Target alititude when using re-entry.
    EmergencyWarpDistance = 320000 -- export: Set to distance as which an emergency warp will occur if radar target within that distance.  320000 is lock range for large radar on large ship no special skills.
    IgnoreEmergencyWarpDistance = 500 -- export: Any targets within this distance are ignored for emergency warp.
    RequireLock = false -- export: Set to true to require a target to lock onto you before starting an emergency warp.
    AutoTakeoffAltitude = 1000 -- export: How high above your ground starting position AutoTakeoff tries to put you
    TargetHoverHeight = 50 -- export: Hover height when retracting landing gear
    LandingGearGroundHeight = 0 --export: Set to hover height reported - 1 when you use alt-spacebar to just lift off ground from landed postion.  4 is M size landing gear,
    MaxGameVelocity = 8333.00 -- export: Max speed for your autopilot in m/s, do not go above 8333.055 (30000 km/hr), can be reduced to safe fuel, use 6944.4444 for 25000km/hr
    AutopilotTargetOrbit = 50000 -- export: How far you want the orbit to be from the planet in m.  200,000 = 1SU (Default 50000)
    AutopilotInterplanetaryThrottle = 1.0 -- export: How much throttle, 0.0 to 1.0, you want it to use when in autopilot to another planet to reach MaxGameVelocity
    warmup = 32 -- export: How long it takes your engines to warmup.  Basic Space Engines, from XS to XL: 0.25,1,4,16,32
    MouseYSensitivity = 0.003 --export:1 For virtual joystick only
    MouseXSensitivity = 0.003 -- export: For virtual joystick only
    autoRollPreference = false -- export: [Only in atmosphere]<br>When the pilot stops rolling,  flight model will try to get back to horizontal (no roll)
    autoRollFactor = 2 -- export: [Only in atmosphere]<br>When autoRoll is engaged, this factor will increase to strength of the roll back to 0<br>Valid values: Superior or equal to 0.01
    rollSpeedFactor = 1.5 -- export: This factor will increase/decrease the player input along the roll axis<br>(higher value may be unstable)<br>Valid values: Superior or equal to 0.01
    turnAssist = true -- export: [Only in atmosphere]<br>When the pilot is rolling, the flight model will try to add yaw and pitch to make the construct turn better<br>The flight model will start by adding more yaw the more horizontal the construct is and more pitch the more vertical it is
    turnAssistFactor = 2 -- export: [Only in atmosphere]<br>This factor will increase/decrease the turnAssist effect<br>(higher value may be unstable)<br>Valid values: Superior or equal to 0.01
    TrajectoryAlignmentStrength = 0.002 -- export: How strongly AP tries to align your velocity vector to the target when not in orbit, recommend 0.002
    pitchSpeedFactor = 0.8 -- export: For keyboard control
    yawSpeedFactor = 1 -- export: For keyboard control
    brakeSpeedFactor = 3 -- export: When braking, this factor will increase the brake force by brakeSpeedFactor * velocity<br>Valid values: Superior or equal to 0.01
    brakeFlatFactor = 1 -- export: When braking, this factor will increase the brake force by a flat brakeFlatFactor * velocity direction><br>(higher value may be unstable)<br>Valid values: Superior or equal to 0.01
    DampingMultiplier = 40 -- export: How strongly autopilot dampens when nearing the correct orientation
    fuelTankHandlingAtmo = 0 -- export: For accurate estimates, set this to the fuel tank handling level of the person who placed the element. Ignored for slotted tanks.
    fuelTankHandlingSpace = 0 -- export: For accurate estimates, set this to the fuel tank handling level of the person who placed the element. Ignored for slotted tanks.
    fuelTankHandlingRocket = 0 -- export: For accurate estimates, set this to the fuel tank handling level of the person who placed the element. Ignored for slotted tanks.
    apTickRate = 0.0166667 -- export: Set the Tick Rate for your HUD.  0.016667 is effectively 60 fps and the default value. 0.03333333 is 30 fps.  The bigger the number the less often the autopilot and hud updates but may help peformance on slower machings.
    
[Return to Table of Contents](#table-of-contents)

<!--These links do not work properly in my test environment.  Will need to be edited once it is "live".-->
# Examples and Tutorials
#### https://www.youtube.com/watch?v=jQSkI0OcATU&feature=emb_logo - Demonstration of Use and Features
https://github.com/Dimencia/DU-Orbital-Hud/blob/master/ButtonHUD_example_1.png
#### This HUD uses on-screen buttons, and so needs to be able to use your mouse. The only way to keep DU from trying to use your mouse for input is to set the Control Scheme to Keyboard. You can then right click the seat, Advanced -> Edit LUA Parameters and find the checkboxes to choose which control scheme you would actually like to use.
https://github.com/Dimencia/DU-Orbital-Hud/blob/master/ButtonHUD_example_2.png
#### The usual hotkeys apply, but it should be easier to use the new button system. We will be converting this to work with screens and a Remote Controller once the screen flicker bug is fixed. For now, many options are missing from the buttons since Remote Controllers must use the hotkeys

[Return to Table of Contents](#table-of-contents)

# No Autopilot Version
#### No Autopilot features version available at https://github.com/Archaegeo/DU-Orbital-HUD-NO-AP

[Return to Table of Contents](#table-of-contents)

### Credits

Rezoix and his HUD - https://github.com/Rezoix/DU-hud

JayleBreak and his orbital maths/atlas - https://gitlab.com/JayleBreak/dualuniverse/-/tree/master/DUflightfiles/autoconf/custom

Archeageo and his work on the HUD

[Return to Table of Contents](#table-of-contents)

