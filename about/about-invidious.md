---
layout: default
title: Invidious
parent: About
permalink: /about/invidious
---

# What is Invidious?

Invidious is an Open Source web project for browsing YouTube. The goals of Invidious are similar to FreeTube, however Invidious has taken a different approach to solving the same issue.

With this approach, Invidious allows multiple users to login and use one instance of Invidious. This allows users to mix their usage together while Invidious fetches the desired information, increasing the privacy of the individual since it's more difficult to identify that one person.

Invidious also provides their own extractor, which includes a public [API](/usage/invidious-api/) that is open to other applications.

## Relationship with FreeTube

FreeTube and Invidious were developed and released at around the same time. In the beginning, FreeTube was using the official YouTube API. When Invidious released, FreeTube transitioned to the Invidious API and has continued to have Invidious as an option for extracting data.

## Major Differences

- Invidious is a website, where FreeTube is a desktop application (However FreeTube is also developed using web technologies)
- Invidious uses a minimal UI, where FreeTube uses a design similar to YouTube
- FreeTube (with it's [Local API](/usage/local-api/)) directly connects to YouTube, where Invidious acts as a middle man between YouTube and the user
- Invidious user data is stored on the Invidious server, where FreeTube stores user data on the user's machine

## Useful Links

- [Invidious GitHub](https://github.com/iv-org/invidious)
- [Invidious Instance List](https://api.invidious.io/)
- [Invidious Documents Site](https://docs.invidious.io/)
