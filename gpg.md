# GNU PG
  
Create foo.txt.gpg from foo.txt and encrypt with a passphrase.  
`gpg -c foo.txt`  
 
Create bar.gpg from foo.txt and encrypt with a passphrase.  
`gpg -o bar.gpg -c foo.txt`  
  
Decrypt foo.pgp to foo.txt  
`gpg -o foo.txt -d foo.pgp`  
   
Encrypt bar.gpg from foo.txt using a key with UUID Robert.  
`gpg -o foo.pgp -r "Robert" -e foo.txt`  
  
Create $@.pgp loop using passphrase in ~/foo (the first line of the file is used as the passphrase).  
`for i in *.*; do pgp --passphrase-file ~/foo "$i"; done`  
