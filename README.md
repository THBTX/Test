



# DU-Orbital-Hud
## A general purpose HUD for Dual Universe
#### Cockpits are *NOT* supported.
###### For assistance, see our [Discord](https://discord.gg/sRaqzmS)

# Table of Contents
| |
|------|
| [Features List](#features-list) |
| [Change Log](./ChangeLog.md) |
| [Credits](#credits) |

# Features List

| HUD (Heads-Up) | Auto-Pilot | Brakes|
| --- | --- | --- |
Artificial horizon | Automatic braking | Brake-hold
Altimeter | Auto-pilot to saved locations | Brake landings (brake force > construct mass)
Pitch | Inter-planetary transit routes |Coast landings (brake force < construct mass)
Roll | Orbital insertion | 
Yaw | Transit-to-orbit | 
Vertical speed indicator |   | 


| Additional Features | 
| --- |
| Emergency Warp if target too close or has lock on you |
|Parachute Re-Entry or Glide Re-Entry|
|Trip odometers and information display.|
Fuel level displays for all types of fuel tanks. Ability to unslot fuel tanks to save slots.
altitude hold, auto-landing and takeoff functionality
Orbital alignment and maneuver assistants
Radar and periscope for situational awareness
Ability to hide the built-in display windows to keep your flight aesthetic clean and focused
Free-look mode
User Parameters for customizing to your HUD and your flight preference to your ship capabilities.
Save parameters between HUD version updates

[Table of Contents](#table-of-contents)


# Installation

### Note: Although not required, we recommend a databank be used.  This allows the HUD to save your user preferences and some long-term variables.  In addition, flight status is saved if you leave and return to the seat.

| Step |Details  |
| --- | --- |
| 1 |Scroll down the the Assets and click on ButtonHUD.conf, this should trigger a download for this file.|
| 2 |Save the file to %ProgramData%\Dual Universe\Game\data\lua\autoconf\custom (or equivalent directory if you did not do default install), the filename does not matter (as long as it's still .conf)|
| 3 |In-game, right click your seat and go to Advanced -> Update custom autoconf list - If you get a YAML error, you did not follow the above directions correctly.|
| 4 |Again, right click your seat and select Advanced -> Run Custom Autoconfigure -> ButtonsHud - Dimencia and Archaegeo|
| 5 |IMPORTANT: Right click the ship and set the user control scheme to Keyboard (Advanced -> Change Control Scheme -> Keyboard). This is necessary for the HUD to work, but you can change the actual control scheme in the next step - fear not virtual joystick aces!|
| 6 |Right click the seat, choose Advanced -> Edit LUA Parameters. Change the userControlScheme to the actual control scheme you wish to use (e.g. Virtual Joystick). You may mouse over the other parameters and set them as you wish - there are many, you should familiarize yourself with them. You may also change control scheme using a Button while seated.|
| 7 |If you have a Databank installed on your vehicle your parameters will save when you stand up. Saved parameters will be restored any time you upgrade the HUD to a new version. See Saving in the Readme for more information|

Blah blah blah





### Credits

Rezoix and his HUD - https://github.com/Rezoix/DU-hud

JayleBreak and his orbital maths/atlas - https://gitlab.com/JayleBreak/dualuniverse/-/tree/master/DUflightfiles/autoconf/custom

Archeageo and his work on the HUD

[Table of Contents](#table-of-contents)
