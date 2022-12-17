---
layout: page
title: Local API
parent: Usage
permalink: /usage/local-api/
---

The Local API is an extractor built into FreeTube that's used to obtain data from YouTube. When you download FreeTube for the first time, this API is used by default. You can select your preferred API in settings. The Local API is a combination of modules and projects by several different developers and maintainers. When combined, they provide a complete YouTube experience. Some of these modules are also maintained by the FreeTube team.

Every module in the Local API uses some form of extracting data from the YouTube website. With this method, it is not rare for something to break within the app. When this happens, we will attempt to fix this as fast as possible. Depending on what broke, we may have to wait for the maintainer of that module to make a fix before the fix can make it's way into FreeTube.

The Local API is one method of obtaining data from YouTube. For another method of obtaining data supported with FreeTube, check out the [Invidious API](/usage/invidious-api).

## Advantages of the Local API

- It is able to make requests quicker compared to Invidious
- The Local API is less likely to fail due to IP blocks compared to the Invidious API
- The Local API is supported by a wide variety of developers due to us using existing modules. This means that more developers outside of the FreeTube team are maintaining and fixing issues when they show up.
- The Local API provides functionality that the Invidious API does not. Ex: Live Chat

## Disadvantages of the Local API

- Updates to the Local API requires the user to download a new version of FreeTube
- The Local API makes calls directly to YouTube, which can slightly hinder privacy
- Because the FreeTube team doesn't 100% maintain the Local API, updates to make fixes can potentially take longer due to a fix not yet being available by the maintainer of a certain part.

## Modules Used in the Local API

| Name                                                                                     | License | Functionality                         | Maintained By the FreeTube Team? |
| ---------------------------------------------------------------------------------------- | ------- | ------------------------------------- | -------------------------------- |
| [youtube-chat](https://github.com/FreeTubeApp/youtube-chat)                              | MIT     | Live Chat                             | Yes                              |
| [youtubei.js](https://github.com/LuanRT/YouTube.js)                                      | MIT     | Search Suggestions, Playlists         | No                               |
| [ytdl-core](https://github.com/fent/node-ytdl-core)                                      | MIT     | Obtain Video Information              | No                               |
| [node-ytsr](https://github.com/TimeForANinja/node-ytsr)                                  | MIT     | Search Functionality                  | No                               |
| [videojs-vtt-thumbnails-freetube](https://github.com/FreeTubeApp/videojs-vtt-thumbnails) | MIT     | Handle Video Thumbnails / Storyboards | Yes                              |
| [yt-channel-info](https://github.com/FreeTubeApp/yt-channel-info)                        | ISC     | Channel Info / Search                 | Yes                              |
| [yt-comment-scraper](https://github.com/FreeTubeApp/yt-comment-scraper)                  | GPL-3.0 | Comment Info / Sort                   | Yes                              |
| [yt-dash-manifest-generator](https://github.com/FreeTubeApp/yt-dash-manifest-generator)  | GPL-3.0 | Generate DASH Files                   | Yes                              |
| [yt-trending-scraper](https://github.com/FreeTubeApp/yt-trending-scraper)                | GPL-3.0 | Get Trending Information              | Yes                              |

## Fallback

If you have the [Invidious API](/usage/invidious-api) enabled as your default extractor, you can have FreeTube fallback to the Local API if the Invidious API fails by enabling fallback within your settings.
