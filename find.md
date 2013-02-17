# Find Notes  
  
`find` will look in all directories below the one specified. find / will search everything on the computer.  
  
In current directory search for files containing zebra and print them on the screen.  
`find . -type f -name "*zebra*" -exec echo {} \;`  
  
Move all .txt files from current dir and subdirs to ~/doc.    
`find . -name "*.txt" -exec mv {} ~/doc \;`  
  
Move all .avi files that do not have sample in the title from current dir and subdirs to ~/vid.  
`find . -iname "*.avi" ! -iname "*sample*" -exec mv {} ~/vid \;`  
The -name flag is case sensitive while the -iname flag is not.  
  
In home directory find mp3 files. Use rsync to copy them to a remote server.  
`find . -type f -iname "*.mp3" -print0 | xargs -0 -I {} rsync -aP {} -e ssh 10.10.1.40:~/Desktop/`  
The -print0 flag will prevent files with spaces or newline characters from ruining things.  
Piping to xargs -0 continues the trend.  
The -I flag assigns {} as whatever find finds so it can be used by xargs.  
