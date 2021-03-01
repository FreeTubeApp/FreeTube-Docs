---
layout: page
title: Creating A Pull Request
parent: Development
permalink: /development/creating-a-pull-request
---

You've created a fix / feature for FreeTube and you're ready to submit your pull request. We'll assume you already know how to do this.

There are a few things to follow when you submit a pull request to the FreeTube project:

- You agree that your code will be published under the [GNU Affero General Public License](https://www.gnu.org/licenses/agpl-3.0.html)
- Your pull request **MUST** be configured to be merged into our `development` branch
- Your pull request must not cause any merge conflicts. You are responsible for solving these before your PR is merged
- Your pull request must pass our [linter rules](http://127.0.0.1:4000/development/getting-started/#linting)
- Your code must follow [ES6 Standards](http://es6-features.org/) and follow the same structure as the rest of our code
- Your pull request should not introduce any proprietary or non-free software / services / modules

Once your pull request meets the above conditions, feel free to create your pull request. When creating your pull request, you'll be presented with a template containing some questions. Please answer the questions as best as you can before submitting your pull request.

Once your pull request has been submitted, someone from the team will review your code. Please be prepared to make changes if requests. Once approved your code will be merged and will immediately be included in our next [nightly build](/development/nightly-builds)
