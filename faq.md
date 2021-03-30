---
layout: page
title: FAQ
permalink: /faq/
---

## What makes FreeTube "private"?
Check out the [Privacy Section](/usage/privacy) to learn more about privacy with FreeTube.

## Will you consider adding support for services outside of YouTube? (Twitch, Soundcloud, PeerTube, etc.)
There are currently no plans to support services outside of YouTube. We are committed to creating a complete YouTube experience while also being as private as possible. There are many things that need to be done to accomplish this and more services will distract us from getting this done. When FreeTube has become feature complete, which may be a long ways from now, then I can consider new services.  For now, do not expect it any time soon.

## Do you plan on porting FreeTube to other platforms? (Android, iOS, etc.)
I have zero plans to port FreeTube to platforms that are not already supported. "Porting" would be more of an entire rewrite with a separate code base where I have to develop each feature multiple times for each platform. For iOS, any effort towards an app would just get it removed from the App Store anyways, which would make it a waste of time. Android is also a waste of time because you should be using NewPipe if you'd like a similar experience. I don't see a reason to make an Android app when NewPipe is a very nice equivalent to what I would make anyways.

We _can_ consider support for the Pinephone however, since it is also a Linux device. This will be later in the future however.

## Can I import my YouTube subscriptions over to FreeTube?
Yes! You can head over to the [importing your YouTube subscriptions](/usage/importing-subscriptions) page to learn more.

## Could You Please Implement X/Y/Z Feature?

Probably. As long as it isn't to added new services or port to new platforms, we can consider adding a new feature (See above questions). Keep in mind that just because a feature is suggested doesn't mean it'll get worked on right away. We try to plan what we'll be working on well ahead of time to keep ourselves organized. If you'd like to see a certain feature prioritized, consider submitting a pull request.

## I Found an Issue!

If you've found a problem with FreeTube, please look through the [common issues](/usage/common-issues) first. If the issue is outside of those, consider [creating an issue](community/creating-an-issue) on GitHub.

## How Can I Help Contribute to the Project?

We are open to accepting help from anyone regardless of your skill set. The simplest way you can help is by [creating an issue](/community/creating-an-issue) or by helping add more documentation. If you know more than one language, we would love it if you helped with [translating to your native language](/community/translations).

If you're a developer and would like to contribute code, please see our [Getting Started](/development/getting-started) guide to learn more. If you want to get some inspiration on what is currently available, check our [bugs](https://github.com/FreeTubeApp/FreeTube/projects/8) and [feature](https://github.com/FreeTubeApp/FreeTube/projects/8) project boards with all available issues.  


## Electron is bad, please use something else.
I understand the frustration that some of you have.  Electron has become overused and over relied on for a lot of projects.  This results in many projects being very resource heavy even for simple tasks.  I personally agree that more projects should put the effort into more native solutions.  I'll try to give my reasoning as to why I use Electron versus something else.

I believe that privacy should be accessible to as many people as possible, regardless of where they are at in the privacy spectrum. In order to accomplish this with FreeTube, this means that it needs to be cross platform.  I work on FreeTube in my free time, and I'm mostly the only person that works on this.  For this project, Electron is the only realistic solution in order for a one man show to cater to as many people as possible.

Looking at the amount of people that download FreeTube, this proves to me that I've made the right choice.  Windows users account for roughly 50% of all FreeTube downloads.  I can easily say that a native solution would end up being Linux only and I would end up dropping support for half of my users.

Despite this, it's still something I want to look into someday.  If FreeTube gets to a point where we only have to do small amounts of maintenance and if we're looking for new projects then I can consider looking into this.  Something like this would be extremely time consuming and is not being planned anytime soon.

## My Virus protection gave a warning when I tried to run FreeTube.  Is FreeTube a malicious application?
No it is not.  Windows and Mac requires that an application is signed by a verified publisher for most applications.  This gives the user a piece of mind that they downloaded the correct program and didn't install anything malicious.  Any good virus protection software will notice if an application isn't signed and will immediately warn the user of such a file.  FreeTube will most likely be scanned during first installation but your virus protection shouldn't find anything.  FreeTube is not currently signed because the licenses to sign applications for Windows are expensive and I'd like to avoid putting a lot of money into the project.  This may change in the future as progress is made but do not be alarmed by any notices from your virus protection.

Those that are concerned with this are welcome to view the source code and build their own packages for installation.
