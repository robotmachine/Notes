# ID3 Notes
## Ideas
* Dump genre to .genre.txt per artist
* Dump year to .year.txt per album
* Investigate applying cover.jpg to id3 tags
## Script Snippets 
### Get genre of MP3s in current folder and write to .genre.txt in artist folder  
``y=$(id3v2 -l 01* | sed -n '/^TCON/s/^.*: //p' | sed 's/ (.*//') ; echo "$y" > ../.genre.txt``  
