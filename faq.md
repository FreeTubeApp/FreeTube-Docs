---
layout: page
title: FAQ
permalink: /faq/
---

## What makes FreeTube "private"?

Check out the [Privacy Section](/usage/privacy) to learn more about privacy with FreeTube.

## Will you consider adding support for services outside of YouTube? (Twitch, Soundcloud, PeerTube, etc.)

There are currently no plans to support services outside of YouTube. We are committed to creating a complete YouTube experience while also being as private as possible. There are many things that need to be done to accomplish this and more services will distract us from getting this done. When FreeTube has become feature complete, which may be a long ways from now, then we can consider new services. For now, do not expect it any time soon.

## Do you plan on porting FreeTube to other platforms? (Android, iOS, etc.)

We have zero plans to port FreeTube to platforms that are not already supported. "Porting" would be more of an entire rewrite with a separate code base where we have to develop each feature multiple times for each platform. For iOS, any effort towards an app would just get it removed from the App Store anyways, which would make it a waste of time.

There is no official port of FreeTube to Android and there are no plans to provide an official port. There is however an _unofficial_ fork that ports FreeTube to Android: [FreeTubeAndroid](https://github.com/MarmadileManteater/FreeTubeAndroid).

## Can I import my YouTube subscriptions over to FreeTube?

Yes! You can head over to the [importing your YouTube subscriptions](/usage/importing-subscriptions) page to learn more.

## Could You Please Implement X/Y/Z Feature?

Probably. As long as it's not to add new services or port to new platforms, we can consider adding a new feature (See above questions). Keep in mind that just because a feature is suggested doesn't mean it'll get worked on right away. We try to plan what we'll be working on well ahead of time to keep ourselves organized. If you'd like to see a certain feature prioritized, consider submitting a pull request.

## I Found an Issue!

If you've found a problem with FreeTube, please look through the [common issues](/usage/common-issues) first. If the issue is outside of those, consider [creating an issue](/community/creating-an-issue) on GitHub.

## How Can I Help Contribute to the Project?

We are open to accepting help from anyone regardless of your skill set. The simplest way you can help is by [creating an issue](/community/creating-an-issue) or by helping add more documentation. If you know more than one language, we would love it if you helped with [translating to your native language](/community/translations).

If you're a developer and would like to contribute code, please see our [Getting Started](/development/getting-started) guide to learn more. If you want to get some inspiration on what is currently available, check our [bugs](https://github.com/FreeTubeApp/FreeTube/projects/8) and [feature](https://github.com/FreeTubeApp/FreeTube/projects/7) project boards with all available issues.

## Electron is bad, please use something else.

We understand the frustration that some of you have. Electron has become overused and over relied on for a lot of projects. This results in many projects being very resource heavy even for simple tasks. We personally agree that more projects should put the effort into more native solutions. We'll try to give our reasoning as to why we use Electron versus something else.

We believe that privacy should be accessible to as many people as possible, regardless of where they are at in the privacy spectrum. In order to accomplish this with FreeTube, this means that it needs to be cross platform. We work on FreeTube in our free time, and we are mostly the only people that work on this. For this project, Electron is the only realistic solution in order for a team existing of a few developers to cater to as many people as possible.

Despite this, it's still something we want to look into someday. If FreeTube gets to a point where we only have to do small amounts of maintenance and if we're looking for new projects then we can consider looking into this. Something like this would be extremely time consuming and is not being planned anytime soon.

## My Virus protection gave a warning when I tried to run FreeTube. Is FreeTube a malicious application?

No it is not. Windows and Mac requires that an application is signed by a verified publisher for most applications. This gives the user a piece of mind that they downloaded the correct program and didn't install anything malicious. Any good virus protection software will notice if an application isn't signed and will immediately warn the user of such a file. FreeTube will most likely be scanned during first installation but your virus protection shouldn't find anything. FreeTube is not currently signed because the licenses to sign applications for Windows are expensive and we'd like to avoid putting a lot of money into the project. This may change in the future as progress is made but do not be alarmed by any notices from your virus protection.

Those that are concerned with this are welcome to view the source code and build their own packages for installation.

## MacOS "FreeTube" is damaged and can't be opened. You should move it to the Trash.

No it is not. As mentioned in the previous section, FreeTube is not codesigned (please read that section for more details) and on ARM Macs Apple has chosen a lot more aggressive, inaccurate messaging.

You can easily fix this by running the following command in the Terminal app. You will need to run the command again each time you update or reinstall FreeTube.

```
xattr -d com.apple.quarantine /Applications/FreeTube.app
```

## FreeTube trying to access my webcam and/or microphone

FreeTube does not use your webcam or microphone for any features or functionality. If you see a prompt claiming the application is requesting access, it's a false positive. The application itself does not interact with your camera or microphone. Additionally, even if there were an attempt to access them, FreeTube automatically blocks any such requests to protect your privacy.
