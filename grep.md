# grep

##Search in multiple files for a string
`grep --include=\*.ext -rnw 'directory' -e "pattern"`
###Example:  
Search in .log and .txt files within current directory and subfolders for the text CocoaThread.  
`grep --include=\*.{txt,log} -rnw './' -e "CocoaThread"`
