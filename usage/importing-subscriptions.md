---
layout: page
title: Importing your Subscriptions
parent: Usage
permalink: /usage/importing-subscriptions/
---

FreeTube has the ability to import your subscriptions from a variety of services. Here you will find instructions on how to import from each service.

## From YouTube

1. Login to your YouTube account
2. Click on your profile picture in the top right corner of the web page
3. Click on "Your data in YouTube" in the displayed drop down
4. Click on "More" in the "Your YouTube dashboard" card
5. Click on "Download YouTube data"
6. Under "Create a New Export", make sure "YouTube and YouTube Music" is selected
7. Click on "All YouTube data included" and deselect everything except for "Subscriptions"
8. Click "Next step"
9. Select your preferred method of deliver (Email, Dropbox, etc.) and click on "Create Export" (Instructions from here on out will assume that you selected email)
10. Check your email and download the .zip file that is provided.
11. Extract the .zip file
12. The file you want will be in `Takeout/YouTube and YouTube Music/subscriptions/subscriptions.json`

Once you have this file, you can import this file into FreeTube by going to `Settings->Data Settings->Import Subscriptions->Import YouTube (.json)`

## From Invidious

While logged into your Invidious account, go to the settings page. Scroll down to the bottom of the page and look for the "Import/Export Data" link. On the new page, look at the bottom for "Import Subscriptions as OPML (for NewPipe and FreeTube)".

Once you have this file, you can import this file into FreeTube by going to `Settings->Data Settings->Import Subscriptions`

## From NewPipe

Go to your subscriptions page (Not your settings page!). On this page, click on the `Subscriptions` title to open up a drop down. In this drop down,click on the "Export to File" button. Transfer this file to your PC running FreeTube.

Once you have this file, you can import this file into FreeTube by going to `Settings->Data Settings->Import Subscriptions`

## From other FreeTube instances

Go to the settings page of the FreeTube app. Under "Subscription Settings", set your subscriptions export type to "FreeTube" and click on "Export Susbcriptions".

Once you have transferred this file to your new machine, you can import this file into FreeTube by going to `Settings->Data Settings->Import Subscriptions->Import FreeTube (.db)`

## From Somewhere Else

At this time, we do not support importing subscriptions from anywhere other than the above methods. Please ask the maintainer of your app if they would be open to supporting exporting their subscriptions into one of the above formats and then use that import function within FreeTube to import your subscriptions.

## Troubleshooting Issues

There might be situations where FreeTube does not properly import your subscriptions. Please try these troubleshooting steps to see if these can fix your issues.

- Try changing your API preference ([Local](/usage/local-api) / [Invidious](/usage/invidious-api)). Alternatively, try using a different [Invidious Instance](https://api.invidious.io/).
- Browse your exported file for any duplicate channels. FreeTube will show a message that not all channels were able to be imported in this situation, however if your file has duplicates, then this isn't a real issue. **YouTube includes duplicates in their export file more than you think.**
- Browse your exported file and check for any banned / removed channels. Exporting from YouTube will still include these channels in your exported file, however FreeTube will obviously be unable to import them.

If you are still having issues importing your subscription or if a channel didn't get included in the import (And you know that it's in your export file), consider [creating an issue](/community/creating-an-issue). You may need to include a link to your exported file in order for us to further investigate the issue.
