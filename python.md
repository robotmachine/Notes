# Python Notes

## Files  

Asks for a filename and assigns it to the variable 'file'.   
`file = raw_input("> ")` 

Assigns the variable 'txt' to open the variable 'file'
`txt = open(file)`  

Prints 'txt' using the command read() which will print the contents of the file.   
`print txt.read()`  

## Importing Modules  

Imports the function os  
`import os` 

Prints the current working directory.  
`print os.getcwd()`  

Changes directory  
`os.chdir("/path/to/change/to")`  
Without first importing os, none of the above will work.   
