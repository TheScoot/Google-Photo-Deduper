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

You need to create a client_secret by following Step 1 of the instructions located here: 
https://developers.google.com/drive/v3/web/quickstart/python
Save file as 'client_secret.json' in same directory as photodeduper.py

If you do not have httplib2 installed then use:
pip install httplib2

To get the Google API client use:
pip install --upgrade google-api-python-client

If the Package six is giving you an exception, install the latest version by doing:
sudo pip install --ignore-installed six

The reason I wrote this, is the iOS Google Photos App keeps creating duplicate photos if I edit any of them with the 
iOS Photos app since the checksum will no longer be the same and it thinks it is a new photo.

