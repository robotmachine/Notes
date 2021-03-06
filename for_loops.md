# for Loops
  
Prepend 's1e' to the beginning of all .avi files in the current directory.  
``for i in *.avi; do mv "$i" "s1e$i"; done``  
  
In the current working directory replace all instances of "Bacon" with "Turnip" in files ending .avi.  
``for i in *.avi; do j=`echo $i | sed 's/Bacon/Turnip/g'`; mv "$i" "$j"; done``  
  
In the current working directory remove the text "Horch" in files ending in .txt
``for i in *.txt; do j=`echo $i | sed 's/Horch//g'`; mv "$i" "$j"; done``  
  
In the current working directory change the first 0 in a filename to a 1, but leave the following 0's (per file) alone.
``for i in *; do j=`echo $i | sed 's/0/1/'`; mv "$i" "$j"; done``  
    
in the current working directory change the first . to a -, but leave the following .'s (per file) alone.
``for i in *; do j=`echo $i | sed 's/\\./\\-/'`; mv "$i" "$j"; done``  
   
For each *.mp3 file, set the id3v2 Track number to be X/Z (Z is the total number)   
Old one:    
``x="1"; for y in *.mp3; do `id3v2 --TRCK "$x/10" "$y"`; x=$[$x+1]; done``  
New one:    
``x="1" && z="`ls -l * | wc -l`"; for y in *.mp3; do `id3v2 -2 --TRCK "$x/$z" "$y"`; x=$[$x+1]; done``   
   
For each *.mp3 file, cut off the first three characters and the .mp3 and set the rest as the TIT2 id3v2 tag.  
``for x in *.mp3; do y=`echo $x | sed 's/...\(.*\)/\1/' | sed 's/.mp3//ig'`; id3v2 --TIT2 "$y" "$x"; done``  
