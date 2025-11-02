---
layout: page
title: Importing your History
parent: Usage
permalink: /usage/importing-history/
---

FreeTube has the ability to import your history from a variety of services. Here you will find instructions on how to import from each service.

## From YouTube

1. Login to your YouTube account
2. Click on your profile picture in the top right corner of the web page
3. Click on "Your data in YouTube" in the displayed drop down
4. Click on "More" in the "Your YouTube dashboard" card
5. Click on "Download data"
6. Under "Create a New Export", make sure "YouTube and YouTube Music" is selected
7. Click on "Multiple formats"
8. Click on "OK"
9. Change the History file format to "JSON"
10. Click on "All YouTube data included" and deselect everything except for "History"
11. Click on "OK"
12. Click "Next step"
13. Select your preferred "Destination" method (Email, Dropbox, etc.)
14. Click on "Create Export" (Instructions from here on out will assume that you selected email)
15. Check your email and download the .zip file that is provided.
16. Extract the .zip file
17. The file you want will be in `Takeout/YouTube and YouTube Music/history/watch-history.json`

Once you have this file, you can import this file into FreeTube by going to `Settings->Data Settings->Import History`

## From other FreeTube instances

Go to the Settings page of the FreeTube app. Under "Data Settings", click on "Export History".

Once you have transferred this file to your new machine, you can import this file into FreeTube by going to `Settings->Data Settings->Import History`

## From Somewhere Else

At this time, we do not support importing history from anywhere other than the above methods. Please ask the maintainer of your app if they would be open to supporting exporting their history into one of the above formats and then use that import function within FreeTube to import your history.
