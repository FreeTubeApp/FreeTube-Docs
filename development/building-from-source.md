---
layout: page
title: Building From Source
parent: Development
permalink: /development/building-from-source
---

This article assumes that your development environment is setup. For instructions on how to do so, please see the [Getting Started](/development/getting-started) page.

## Note for Linux Users

By default, FreeTube is configured to build a large variety of binaries. There is a very high chance that at least one of these binaries are unable to be built on your system. In order for FreeTube to successfully build on your system, you will need to edit the build script to remove the problematic binaries before building.

Open `_scripts/build.js` in your favorite text editor and edit [line 39](https://github.com/FreeTubeApp/FreeTube/blob/development/_scripts/build.js#L39). Remove the options that you will not be able to create on your system and save the file afterwards. Once done, you can follow the instructions as normal.

## Building for Your Native System

Open up your terminal in the root of the project and run the following command:

```
npm run build
```

Once the command has finished, a new `build/` folder will be created in the project. This folder will contain any and every binary that the command has created. It will only create binaries for the OS you are running (ex: Windows can only create Windows binaries).

## ARM64 (Linux Only)

If you are running a 64 bit Linux OS, you will also be able to create ARM64 binaries. To do so, run the following command:

```
npm run build:arm
```

Binaries will be located in the same location as the other command.
