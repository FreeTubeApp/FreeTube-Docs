---
layout: page
title: Privacy
parent: Usage
permalink: /usage/privacy/
---

FreeTube allows you to browse YouTube more privately, but how private is it? We'll be going more into detail here and hopefully answer some questions about the privacy that you're given when you use FreeTube.

## Data

Your data is stored on your machine and isn't used to track your habits when you use YouTube / FreeTube. You can find where your [data is located](/usage/data-location) to confirm this. Alternatively, you can export your data from the settings page.

## Requests To YouTube

When you use the [local API](/usage/local-api) within FreeTube, FreeTube will be required to make a request to YouTube in order to get the data that you're wanting. This means that your IP Address will be sent over to YouTube along with the minimum required information that may be needed in that request (ex: if you request a channel page, that channel's ID will be sent along with the request).

When you use the [Invidious API](/usage/invidious-api) within FreeTube, FreeTube will be required to make a request to your set Invidious instance in order to get the data that you're wanting. This means that your IP Address will be sent over your Invidious instance along with the minimum required information that may be needed in that request (ex: if you request a channel page, that channel's ID will be sent along with the request). The Invidious instance will then send it's IP address to YouTube to fetch the data on your behalf.

Out of the two, using the Invidious API has greater privacy due to it being able to act as a proxy between you and YouTube.

Regardless of which API you use, you should use a VPN alongside FreeTube for even greater privacy.

## Requests To Other Places

FreeTube will make a few requests to places outside of YouTube. All of these requests can be either disabled or avoided. The requests made are as follows:

- [https://github.com](https://github.com) - Used to check for updates and provide changelog notes, can be disabled in settings
- [https://blog.freetubeapp.io](https://blog.freetubeapp.io) - Used to check for new blog posts, can be disabled in settings
- Your set [Invidious Instance](/about/about-invidious) - Used to check for "Most Popular", can be hidden in settings. Only requested when the user navigates to the page. The request is done regardless of your API settings

## Tracking

YouTube does not count any views made through FreeTube. It also cannot see your watching habits when your viewing a video within FreeTube. This is because YouTube's video tracking is done through their video player and not the video file itself. Since FreeTube is using it's own player and only grabbing the video file, YouTube cannot track your watch habits. This is regardless of your API choice.

When you make a request to YouTube (regardless of your API choice), it is unknown what YouTube may do behind the scenes with that request. YouTube could possibly have some tracking measures done within the requests we make, but there is no way to know for sure. Even if it does, it would be much more difficult for YouTube to track you individually since you are not logged in and because there is much less information to use to identify you.

This is why a VPN is very important. Even if YouTube happens to do any tracking with your IP Address, having a VPN makes it much more difficult to identify you since you're likely sharing that VPN with hundreds if not thousands of other users.

Using the [Invidious API](/usage/invidious-api) or [Tor / Socks5 proxy](/usage/tor) can also help, to add another layer between you and YouTube.

## Analytics

FreeTube itself does not have any analytics built into the app. FreeTube also does not require any sign up or account in order to use it.
