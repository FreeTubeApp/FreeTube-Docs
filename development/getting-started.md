---
layout: page
title: Getting Started
parent: Development
permalink: /development/getting-started/
---

Getting a development environment setup for FreeTube is very simple. You must have [Git](https://git-scm.com), [Node.js](https://nodejs.org/en/) and [Yarn](https://yarnpkg.com) installed on your system in order to set up your environment.

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
yarn install
```

Run the application:

```
npm run dev
```

And you're done! After a couple of seconds, FreeTube will open up and you are ready to make changes to the project.

## Hot Reload

With this development environment of FreeTube, hot reload is enabled. This means that changes you make to the code will be reflected immediately within the app window.

## Linting

To keep your code up to par with the rest of the application, we enforce a linter that must pass before we will accept your pull request. This is done automatically when you create your pull request, however you can test this before your pull request is made.

In the root of your directory, run the following command:

```
npm run lint
```

This command will then display all of the errors that the linter found in your project. If nothing is displayed after you run the command, then no errors were found.

In some cases, the issues that the linter finds are simple enough that they may be able to be fixed automatically. If this happens, you can run the following command to fix them:

```
npm run lint-fix
```

This command will also show any errors that the linter still finds and cannot fix.

## Adding New Strings For Localization

If you are adding a new string of text that needs to be available for translation, you will need to add it into the `/static/locales/en-US.yaml` file within the project. Please follow the same structure already established when adding new strings. Alternatively, add your string to a location that seems appropriate.

You **DO NOT** need to add your strings to the other locale files. Our translation software will handle that for you.

## Adding New External Players

If you are adding a new external player, you will need to add a flag mapping to `/static/external-player-map.json`.
Please try to add all mappings possible to the player to allow the maximum number of features used. Please follow the schemata of mpv.

You **DO NOT** need to add anything to any source code files.

## Useful Links and Information

FreeTube is built using Electron and Vue.js, so knowing how these technologies work is beneficial to creating code. These links may be helpful to learning more about these.

 - [https://www.electronjs.org/docs](https://www.electronjs.org/docs)
 - [https://vuejs.org/v2/guide/](https://vuejs.org/v2/guide/)
 - [https://vuejs.org/v2/guide/components-registration.html](https://vuejs.org/v2/guide/components-registration.html)
 - [https://vuejs.org/v2/guide/components-props.html](https://vuejs.org/v2/guide/components-props.html)
 - [https://vuejs.org/v2/guide/routing.html](https://vuejs.org/v2/guide/routing.html)
 - [https://vuex.vuejs.org/](https://vuex.vuejs.org/)

 If you have any more questions about development, feel free to ask us in our [Matrix Channel](/community/matrix).

 Once you've made your code changes, it's time to send a [pull request](/development/creating-a-pull-request).
