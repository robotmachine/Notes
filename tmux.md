# tmux

## Command Line Options

`$> tmux new-session` New empty session using the current terminal.  
`$> tmux new-session -d 'command -w options'` Create a new session with a command in the first window.  
`$> tmux new-session -s NAME` Create a new session with the name NAME.  
`$> tmux list-sessions` List the current sessions. The result will be something like:  
`main: 3 windows (created Wed Mar 13 12:01:27 2013) [123x36] (attached)`
`2: 1 windows (created Wed Mar 13 14:24:28 2013) [80x23]`  
`3: 1 windows (created Wed Mar 13 14:24:30 2013) [80x23]`  
`4: 1 windows (created Wed Mar 13 14:24:33 2013) [80x23]`  
`$> tmux attach-session -t N` Attach session number N. Or, if you gave the session a name you can use the name.  

## Interactive  
Use CTRL-a (^a) to get screen's attention and then issue the command.  
(e.g., to go to the next screen hold CTRL and then press a. Release and then press n)  
  
### Common  
  
### Regions  
  
### Others  
  
## Commands  
^a, then `:`, then the command.  
  
