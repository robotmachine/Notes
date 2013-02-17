# [GNU screen](https://www.gnu.org/software/screen/)

## Command Line Options
Adapt all windows to the new display width & height.
`$> screen -A`  

Reattach session. If there are multiple it will list them.
`$> screen -r`  

Show list of current screens.
`$> screen -list`  
`	1248.pts-0.robot-mk-x	(Detached)`  
`	1241.pts-0.robot-mk-x	(Detached)`  
`	753.pts-0.robot-mk-x	(Detached)`  
`3 Sockets in /run/screens/S-brian.`  

Reattach to a specific session
`$ screen -r foo`

Reattach session if there is one, otherwise start a new one.
`$> screen -R`   

## Interactive
Use CTRL-a (^a) to get screen's attention and then issue the command.  
(e.g., to go to the next screen hold CTRL and then press a. Release and then press n)

### Common  
`"` List all windows and their titles.  
c - Create a new window.
k - Destroy the current window.
n - Next window.
p - Previous window.
d - Detach this screen.

~Regions:
S - Split in half vertically.
| - Split in half horizontally.
[tab] - Go to the next window.
Q - Kill all regions except the current.
X - Kill the current region.

~Others:
0-9 - Select the numbered window.
A - Set the title for the current window.
C - Clear the screen.
F - Resize window to match the current size.
l - Refresh the window (lowercase L)
M - Monitor window for activity.
_ - Monitor window for inactivity.
x - Lock terminal.
[ - Enter scrollback mode.
] - Write the contents of the paste buffer to stdin

~Commands:
All commands start with :
CTRL-A, then :, then type the command.

:sessionname foo - Rename the session with a friendly name.
