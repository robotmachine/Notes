# GNU PG
# 
# Create foo.pgp:
gpg -c foo
#
# Decrypt foo.pgp to foo
gpg -o foo -d foo.pgp
#
# Create $@.pgp loop using passphrase in ~/foo (the first line of the file is used as the passphrase)
for i in *.*; do pgp --passphrase-file ~/foo "$i"; done
