# mtgcaptainit
 The Official Website for the Captain Format

## Instructions on how to update website on web server

### 1) Login as root on web server and run these commands

cd /var/www/

git clone https://github.com/mtgCaptainIT/mtgCaptainIT.github.io

cd mtgcaptain.cards

mv -v -f /var/www/mtgCaptainIT.github.io/* /var/www/mtgcaptain.cards

### 2) Verify the files exist

cd /var/www/mtgcaptain.cards

ls

### 3) If the files do exist with a correct timestamp it is time to cleanup

cd /var/www/

rm -r mtgCaptainIT.github.io

### 4) Verify you can access the website on your own PC and the new changes are reflected
