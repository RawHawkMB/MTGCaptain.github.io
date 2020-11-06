# mtgcaptainit
 The Official Website for the Captain Format

## Instructions on how to update website on web server

### 1) Login to the web server via SSH or web SUI & run these commands

cd /var/www/

./updatewebsite.sh

### 2) Verify you can access the website on your own PC and the new changes are reflected correctly


#### Script Contents:

Echo "...Starting Script"
Echo "Changing to website directory & cleaning up old Github temp files."
cd /var/www/
rm -r mtgCaptainIT.github.io

Echo "Downloading new GitHub data."
git clone https://github.com/mtgCaptainIT/mtgCaptainIT.github.io

Echo "Updating HTML and Picture data."
mv -v -f /var/www/mtgCaptainIT.github.io/* /var/www/mtgcaptain.cards
mv -v -f /var/www/mtgCaptainIT.github.io/img/* /var/www/mtgcaptain.cards/img

Echo "Please refresh the website and review changes."
Echo "Ending Script..."
