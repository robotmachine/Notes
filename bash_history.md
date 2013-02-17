# Bash History
  
Run the last command that matches foo (starting at the beginning of the line).  
`!foo`  
  
Run the last command that matches foo (anywhere in the line).  
`!?foo`
  
Press `<ctrl>+r` to enter a reverse incremental history search. Enter executes the command when you find it. `<ctrl>+j` will bring it to the command line for editing.
  
Return a numbered list of everything in history.
`history`  
  
Search with grep (-i for case insensitive).  
`history | grep -i "foo"`  
  
The above will return a numbered list.  
Use the history expression command and the number to execute the desired command.  
`!<number>`  
