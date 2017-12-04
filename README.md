# Google-Photo-Deduper

Uses the Drive APIs to go through all your photos to look for photos with the same name and created date and:

With the -save flag:
Backs up all the duplicate photos with the one it will keep marked.  

With the -delete flag:
Keeps the last modified photo and deletes all the others.

Notes:
You must select the setting in Google Drive to "Automaticlly put your Google Photos into a folder in My Drive" 

If a file has a created date even a second off it will not be considered a duplicate.
PNGs are not working for some reason.  Feel free to try and fix, I tried a bunch of things, it just doesn't return them.

The reason I wrote this, is the iOS Google Photos App keeps creating duplicate photos if I edit any of them with the 
iOS Photos app since the checksum will no longer be the same and it thinks it is a new photo.

