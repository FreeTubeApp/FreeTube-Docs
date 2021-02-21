---
layout: page
title: Getting Started
parent: Development
permalink: /development/getting-started/
---

Getting a development environment setup for FreeTube is very simple. You must have Git and Node.js installed on your system in order to set up your environment.

Once installed, open a Terminal in a folder that you'd like to store your repository. Then, clone the repository.

```
git clone https://github.com/FreeTubeApp/FreeTube.git
```

Change directory to the new folder:

```
cd FreeTube
```

Install Dependencies:

```
npm install
```

Run the application:

```
npm run dev
```

And you're done! After a couple of seconds, FreeTube will open up and you are ready to make changes to the project.

## Hot Reload

With this development environment of FreeTube, hot reload is enabled. This means that changes you make to the code will be reflected immediately within the app window.
