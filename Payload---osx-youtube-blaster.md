>`REM Author: Cody Theodore`
`REM Title: OSX Youtube Blast`
`REM This payload will open terminal, crank up the Macs volume all the way, then open a youtube video of your` `choice by replacing the link. Remember to include the "watch_popup" part of the URL for full screen.`
`DELAY 1000`
`GUI SPACE`
`STRING terminal`
`DELAY 500`
`ENTER`
`DELAY 4000`
`STRING osascript -e 'set volume 7'`
`DELAY 500`
`ENTER`
`DELAY 500`
`STRING open http://www.youtube.com/watch_popup?v=dQw4w9WgXcQ`
`DELAY 500`
`ENTER`> 