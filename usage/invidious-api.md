---
layout: page
title: Invidious API
parent: Usage
permalink: /usage/invidious-api/
---

The Invidious API is an extractor built into the [Invidious](/about/invidious) project that's used to obtain data from YouTube. FreeTube can connect to an Invidious instance and have it obtain data on it's behalf. Invidious handles all extraction logic and therefore provides a full experience of browsing YouTube.

Invidious extracts data from YouTube and does not use any official API.

The Invidious API can be enabled by changing your preferred API in the settings page within FreeTube.

The Invidious API is one method of obtaining data from YouTube. For another method of obtaining data supported with FreeTube, check out the [Local API](/usage/local-api).

## Advantages of the Invidious API

- Invidious makes a request to YouTube on your behalf, preventing your IP from being sent to YouTube
- Since multiple users are using one instance, your requests are mixed together which makes it difficult for YouTube to identify one user
- Since Invidious is hosted on an external server, updates to their extractor can be done without needing to update FreeTube itself
- If an Invidious instance is IP blocked, it's easy to have FreeTube use another instance to continue watching content
- Invidious can proxy videos, images, and RSS feeds which prevents FreeTube from making any direct connections to YouTube

## Disadvantages of the Invidious API

- Because potentially many users are using Invidious, it's more likely for an instance to get blocked compared to the Local API. Some instances can bypass this however
- Because Invidious proxies a lot of data from YouTube, content and videos can potentially take longer to load, degrading the viewing experience
- Invidious doesn't provide functionality to some features that FreeTube provides, such as live chat

## Fallback

If you have the [Local API](/usage/local-api) enabled as your default extractor, you can have FreeTube fallback to the Invidious API if the Local API fails by enabling fallback within your settings.
