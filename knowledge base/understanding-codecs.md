---
layout: page
title: Understanding video codec selection
parent: Knowledge base
permalink: /knowledge-base/understanding-codecs/
---

FreeTube doesn't provide any user facing options to do that no (forcing specific codecs is a bad idea because of bullet point 2).

FreeTube uses the [Web MediaCapabilities API](https://developer.mozilla.org/en-US/docs/Web/API/MediaCapabilities/decodingInfo) to determine which streams are likely to play smoothly (no stutters or frame drops) and power efficiently (generally checks whether that stream can use hardware accelerated decoding) to try to provide a decent playback experience for most people out of the box.

So if you think that FreeTube is not picking AV1 or VP9, there are a few things you can check:

1. Check that your theory is correct by right clicking on the player and enabling the stats overlay, that will tell you which streams FreeTube is currently playing.
2. It is possible that the video itself doesn't have AV1 and VP9 streams e.g. live streams only have h264/avc1 in FreeTube, with VR videos FreeTube will ignore the VP9 streams as they cause playback errors (so only AV1 or h264), recently finished live streams and recently published videos may be missing some codecs and resolutions as YouTube is still processing the video, old videos will be missing the newer codecs and finally this is purely anecdotal but videos with low view counts on channels with generally low view counts tend to be missing codecs and resolutions (possibly because YouTube considers them lower priority to fully process).
3. Check the GPU Internals page to see if FreeTube/Electron/Chromium can actually use hardware decoding on your machine and what codecs, resolutions and framerates it can do that at.
    1. In the app menu (press Alt on Windows and Linux to make it show up) go to "View" and then "GPU Internals (chrome://gpu)"
    2. In the "Graphics Feature Status" section (at the top of the page), check that the Video Decode bullet point says "Hardware accelerated"
    3. In the "Video Acceleration Information" section (near the bottom of the page), in the "Decoding" subsection check that it lists " Decode av1" and "Decode vp9" at the resolutions that you are trying to play in FreeTube
4. If the information on the GPU internals page doesn't match what you expect for your hardware and driver combination. Check that your GPU drivers are up-to-date.
5. On Linux things get complicated and hardware accelerated video decoding aka VA-API support may not be enabled by default (Chromium considers VA-API on Linux support to be community maintained, so they don't enable it by default) so you will likely need to launch FreeTube with specific flags to enable it if it is supported by your hardware and drivers (so not NVIDIA). As those flags differ by GPU manufacturer, GPU drivers, Electron/Chromium version, you'll need to figure out the correct ones for your specific combination with a bit of internet research. The [Chromium VA-API on Linux](https://chromium.googlesource.com/chromium/src/+/refs/heads/main/docs/gpu/vaapi.md#vaapi-on-linux) documentation and ArchLinux wiki are good places to start your research (for the ArchLinux wiki keep in mind that you need to pass the flags directly to FreeTube, FreeTube does not read non-standard distro specific electron/chromium config files that they suggest).
6. If your GPU and drivers do not support AV1 and/or VP9 or you are unable to get hardware acceleration to work, you can use some more dirty tricks, we will not provide support for any issues you encounter while doing these, so do these at your own risk:
    1. There are Chromium flags that can force disable support for specific codecs or decoding backends, those flags differ by OS, GPU drivers, Electron/Chromium version, you'll need to figure out the correct ones for your specific combination with a bit of internet research.
    2. Alternatively you can also create a custom build of FreeTube for yourself with added filtering in the code, you will need to make sure that you do not end up in a situation where you have filtered out all streams and break playback (see bullet point 2 for an incomplete list about the many situations and edge cases where not all streams are available)
