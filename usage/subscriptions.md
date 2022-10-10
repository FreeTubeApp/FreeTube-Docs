---
layout: page
title: Subscriptions
parent: Usage
permalink: /usage/subscriptions/
---

One major feature about FreeTube is the ability to subscribe to your favorite YouTube creators.
There are no limits to how many subscriptions you can have, however there are some limits when you have a lot of subscriptions, more on this later.

## Subscribing to a Channel

Subscribing to a channel is no different to how you would subscribe to a channel on YouTube. Browse to a channel's page and you will see a big subscribe button. Clicking on that will add that subscription to your current [profile](/usage/profiles). Clicking the button again will remove the subscription.

## Viewing Your Subscription Feed

Going to your subscriptions page will allow you to view a feed of the latest videos of every channel you're subscribed to. Because of the limitations of FreeTube (We can't tell YouTube to get your feed in a traditional sense, we have to manually grab every channel), this feed must be manually refreshed. Refreshing your subscription list can take a while and is expensive to do, so try not to refresh too often.

## Methods of Generating Your Feed

FreeTube has 2 different methods to obtain your subscription feed (It's 4 if you count using the [Local API](/usage/local-api) and the [Invidious API](/usage/invidious-api) as an extra toggle). There's what we'll call the traditional method and then there's the RSS method.

The traditional method grabs the first page from that channel's page and sorts them into a list by upload date. This is the method you're using by default.

The RSS method uses that channel's RSS feed to generate your subscription feed. This method is faster than the traditional method, however the RSS feeds do not provide certain information to FreeTube. The information not included are things such as the video duration and the status of a video (ie: If the video is live / a premiere / etc.). The RSS method also has a benefit of not contributing to your daily request limit.

When using the Invidious API and using the RSS method, FreeTube will grab a proxied version of the channel's RSS feed from Invidious, preventing that call to YouTube.

## Limitations

YouTube has a limit on how many requests per day an IP address is allowed to make. If you exceed this limit, you will be greeted with a 429 error and will not be allowed to browse using FreeTube any more. This limit can be reached much faster if you have a large amount of subscriptions. As mentioned above, using RSS does not count towards this limit and can be safely used even when you have a large amount of subscriptions.

As a safety precaution, FreeTube will automatically force the RSS method whenever you have more than 125 subscriptions in a profile. This will happen regardless of your settings and there is no way to disable this. Creating a new [profile](/usage/profiles/#creating-a-new-profile) with less than 125 subscriptions will bypass this however.

For more information, check out the [Common Issues](/usage/common-issues) page about 429 errors.

## Fallback

When your default method of obtaining your subscription feed fails, FreeTube will automatically fall back to your non-preferred method in an attempt to still show you a feed. For example, if the traditional method returns an error while attempting to fetch your feed, FreeTube will automatically try again using the RSS method. FreeTube can fallback even further if you have the API fallback option enabled.
