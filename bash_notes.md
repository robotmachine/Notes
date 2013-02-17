# General bash/unix notes  
  
## find

Move all .txt files from current dir and subdirs to ~/doc.    
`find . -name "*.txt" -exec mv {} ~/doc \;`  
  
Move all .avi files that do not have sample in the title from current dir and subdirs to ~/vid.  
`find . -iname "*.avi" ! -iname "*sample*" -exec mv {} ~/vid \;`  
  
The -name flag is case sensitive while the -iname flag is not.  
  
## rsync  
Copy all *.avi files in /home/user/vid/ to ./ via SSH.  
`rsync -aP '-e ssh -p 2112' user@192.168.1.10:"/home/user/vid/*.avi" ./`  
  
## other  
  
Count files in current directory.  
`ls -l . | egrep -c '^-'`  
  
Prepend Q to *.mp3.  
`for i in *.mp3; do mv "$i" "Q$i"; done`  
