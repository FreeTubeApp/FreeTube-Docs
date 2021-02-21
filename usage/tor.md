---
layout: page
title: Tor
parent: Usage
permalink: /usage/tor/
---

FreeTube allows you to use the Tor network as a proxy to make API calls to YouTube.  This can be enabled through the settings page on FreeTube.  You must have a Tor client up and running in order to use this feature.

For all systems, make sure that your Tor session is running on default settings using `127.0.0.1` for the IP and `9050` for the port.

### Windows:

Go to the Tor Project's [download](https://www.torproject.org/download/download.html.en) page and download the expert bundle for Windows.  Extract the Tor folder and move it to your desktop (this is important so FreeTube can find the folder).  Open up `Tor.exe` as an administrator and a Tor session should be created.

### Mac

Run the following command to install Tor. (Requires Homebrew)

`brew install tor`

Once installed, start a Tor session with the `tor` command.

### Linux

Install `tor` through your preferred package manager.  For example, on Debian or Ubuntu, you will input this command.

`sudo apt install tor`

A Tor session should start automatically upon installation.  If it does not, you can start a Tor session with this command.

`/usr/bin/tor --RunAsDaemon 1`
