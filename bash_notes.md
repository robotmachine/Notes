# General bash/unix notes  
  
  
## rsync  
Copy all *.avi files in /home/user/vid/ to ./ via SSH.  
`rsync -aP '-e ssh -p 2112' user@192.168.1.10:"/home/user/vid/*.avi" ./`  
  
## other  
  
Count files in current directory.  
`ls -l . | egrep -c '^-'`  
  
Prepend Q to *.mp3.  
`for i in *.mp3; do mv "$i" "Q$i"; done`  
