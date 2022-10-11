---
layout: page
title: CI / Nightly Builds
parent: Development
permalink: /development/nightly-builds
---

The FreeTube repository is currently setup to create binaries automatically every time a change is made to our development branch. With this setup, you can try out new changes right away instead of having to wait for a full release. This is doable thanks to [GitHub Actions](https://github.com/features/actions).

## Downloading Nightly Builds

In the main FreeTube repository, head over to the `Actions` tab. Alternatively, you can also click on [this link](https://github.com/FreeTubeApp/FreeTube/actions).

Once there, you will see some workflows over on the left side of the page. Click on the `build` workflow to only show builds.

In the main list, you will now see commit messages that explain the change that was made to the repository. Find the latest message with a green checkmark and click on the title. You will be brought to a detailed builds page.

Towards the bottom of the page, you will see a section labeled `Artifacts`. Here you can download the build for your operating system of choice. Click on a build to start your download.

**NOTE:** If you are unable to click on a build and download it, it's because you are required to sign in to GitHub in order to access these download links. Unfortunately there is nothing we can do about to change this.
