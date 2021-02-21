---
layout: page
title: Video Formats
parent: Usage
permalink: /usage/video-formats/
---

FreeTube is able to provide a handful of different formats from YouTube to serve content to you. The main ones are DASH, Legacy, and Audio.

You can select your preferred format in settings. Alternatively, you can change the format for a specific video by clicking on the button below the like bar with the file icon.

## DASH

[DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP) is the default video format and is the one that YouTube uses. It is designed to allow quality levels to dynamically change along with syncing up the video with a separated audio file. A majority of files returned by YouTube have the video and audio separated in order to be used via DASH. Since YouTube is mostly designed around this, DASH is the suggested format for most users.

A current limitation is that videos will max out at 1080p. This is not a limitation of DASH but rather a limitation of the video player FreeTube uses. Most videos from YouTube provide a combination of MP4 and WebM files. Almost all qualities higher than 1080p use WebM and the video player that we use doesn't fully support WebM. Because of this, most videos will max out at 1080p. Rarely you may find some videos that allow for higher qualities.

## Legacy

Legacy formats are more of a term coined specifically for FreeTube. YouTube provides a small number of video streams that are traditional MP4 files with the video and audio combined and do not take advantage of DASH. These videos are labeled as "Legacy" videos within FreeTube.

The main limitation of Legacy formats is that a legacy video will never have a quality above 720p.

One benefit of the Legacy formats is that they are easier to play compared to DASH. Legacy formats use less resources and less bandwidth which makes them preferred for low spec devices like a Raspberry Pi.

When [downloading a video](/usage/downloading-videos/), you'll likely want to download a legacy video file since it already has the video and audio combined.

## Audio

The Audio format takes advantage of the separated video and audio used for DASH and only streams the audio portion to the player. This format may be preferred if you are playing a video where there is little activity going on in a video such as when you are listening to music or a podcast.
