# Bash Snippets

`for x in * ; do if [ -f "$x"/.genre.txt ] ; then y=$(cat "$x"/.genre.txt) ; if [[ $y == *Hip-Hop* ]] ; then echo "$x" ; fi ; fi ; done | less`  
