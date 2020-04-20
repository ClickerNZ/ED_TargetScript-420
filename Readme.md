
Version 4.2.0

HISTORY: 
This script started with Aussiedoids' most excellent and extremely comprehensive ED script version 3.1.0
and was modified to mimic my old Saitek X-55 basic configuration. I have since decided to use the advanced
abilities of TARGET Script to create a "smart" configuration and have studied and lifted ideas and methods
from Aussiedroid and others including CMDRs Touille and Darkcyde.

PHILOSOPHY: 
This script does not set out to use every single button and switch on the WARTHOG HOTAS, nor provide 
every single bind available in ED. Whilst convenient, I tend not to use the HOTAS for non-HOTAS functions
(eg I do not currently issue chat macros or fighter instructions etc).
I've written or modified the functions to suit my preferences, my play style and my hardware. Therefore, I've
stripped a lot of features which exist in Aussiedroid's script, modified or rewritten others and created some
new stuff.

My HARDWARE:
This script and supporting files are written and maintained to work with my current hardware setup.
This includes a Thrustmaster Warthog HOTAS, Thrustmaster TWCS Pedals and an EDTracker Pro (wireless).
Keyboard and mouse usage is very limited but still required for certain functions

COMPATIBILITY: 
Be aware that this script uses some localised state tracking where possible/desired, which cannot currently
synchronise with states changed using a second tool to issue concurrent commands via keystroke such as 
AutoHotKey or Voice Attack/HCS Voicepacks. UPDATE: If the second tool causes changes in status.json, this script now handles those.

CAUTION: 
If you intend to edit this software, be careful changing the printf formatting as output from this script
displays differently in the TARGET Editor versus the TARGET GUI Console due to font differences between the two.
The formatting used herein suits the GUI console and not the editor.
 
UPDATE:
- Versions 331 and later now include the ability to read/process any of the key/value pairs within the
status.json file that Elite Dangerous writes to the journal folder. 
- Version 410 and 410a uses an external C++ based exe file (thanks to CMDR Touille) which resides and runs in the ED Journal file location. This program monitors status.json and sends the Flags key value via a TCP socket to TARGET.
Together, these enable the script to align all of the state tracking I need.
- Version 410b no longer uses the external C++ file. I've replaced this with an REXEC statement to run fnsReadStatusJson() every 500 ms.
- Version 420 contains changes required for ED 3.7 - Fleet Carriers

PACKAGE CONTENTS: 
When publishing or sharing this script the following should be included in the zipped package;
- This readme file
- The license file
- ED_Main.tmc, ED_Functions.tmh, ED_Macros.ttm, ED_Toggles.tmh,  
- ED_StateTracker.tmh, ED_KeyMap.tmh, ED_GlobalVars.tmh, ED_UserSettings.tmh 
- ED_TCPCallback.exe (+ ED_TCPCallback.cpp) - no longer required 
- Voice.exe (users can find this on github and check out the source if they wish)
- sounder.exe (users can find this on github via the same author as voice.exe)
- target_enhanced.tmh As of version 4.0.0, I use a modified target.tmh file which itself was modified by Sedenion
(whenever Thrustmaster update their TARGET software, I will update it and provide a new version here)
- Windows batch file (SAMPLE_Launcher.cmd) to use to launch Elite Dangerous, my TARGET script and supporting apps)
- The Elite Dangerous .bind file created to support this script
- The image files created to summarise the Joystick and Throttle button assignments
- The image files created to summarise keyboard key utilisation
- The change log for this version

INSTALLATION:
1) Copy the .bind file in the package's 'Bindings' folder to your Elite Dangerous bind file folder.
This is usually at "c:\users\%username%\AppData\Local\Frontier Developments\Elite Dangerous\Options\Bindings"
As 'AppData' can usually be hidden you may need to unhide it via the folder view options in Windows if navigating
via the windows explorer. Or, you should be able to cut/paste the path above into a run box or address bar.

2) Unzip the script files anywhere on your disk that you can easily find/get to.
Example c:\Thrustmaster\ED_TargetScript 

3) Copy voice.exe and sounder to c:\Thrustmaster\ED_TargetScript\ and set correct path in the ED_UserSettings.tmh file for
both VoicePath and VoiceCMD variables

3a) Copy Sounds folder to c:\Thrustmaster\ED_TargetScript\ and set correct path in ED_UserSettings file 

4) - THIS IS NO LONGER REQUIRED - Copy ED_TCPCallback.exe to wherever ED writes its status.json files.
This is usually %userprofile%\saved games\frontier developments\elite dangerous\
Then, create a shortcut to this exe on your desktop and run it when you run the game.
Or, ideally, include a 'start' statement in the windows batch file launcher program included in this package.
If you are adventurous (and know how), you can hard code the status.json file path into ED_TCPCallback.cpp and recompile.
This will allow you to copy and run ED_TCPCallback.exe from anywhere you want (eg. c:\Thrustmaster\ED_TargetScript\ED_TCPCallback\)

5) Print out and/or study the image files within the 'Maps' folder.

6) The Preferred method of running the script is via a Windows batch file.
No longer applicable - (This is required as the script now writes the location and string length of the status.json file.)
No longer applicable - (The scripts also uses a timeout command line modifier for TargetGUI.exe)

ED_Launcher.cmd batch file is included in this package and is best copied to wherever you copied the scripts to in "step 2" above.
I recommend you create a shortcut to this batch file on your desktop and run it as administrator.
Please read the comments in this batch file for more information

USER SETTINGS:
All user configurable settings are in the ED_UserSettings.tmh file.
Avoid changing anything in ED_GlobalVars or ED_KeyMap files unless you know what you are doing.

USAGE and SHARING: 
If you have obtained a copy of this script, feel free to use the ideas and methods for your own use and I 
encourage you to share these with other like minded players.
This software uses the MIT license which can be found at the root of this package/repository.

CREDITS:
Original script by Aussiedroid.
Contribution and ideas lifted from Touille and Darkcyde.
Modified target.tmh was sourced from Sedenion.

DISCLAIMER:
This software is a work in progress. 
No warranties are stated or implied and no responsibility will be accepted for any damage this software may
cause to your hardware, sanity or marital status.
By downloading, installing and using this software, you agree to use this at your own risk.

Fly Dangerous Commanders ... o7

CMDR Clicker
