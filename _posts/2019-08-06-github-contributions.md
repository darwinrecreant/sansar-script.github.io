---
layout: post
author: Binah
title:  "Github contributions"
date:   2019-08-06 00:00:00 -0700
categories: github
---

If you're looking for ways to share your code with the Sansar scripting community through the sansar-script github repositories, [https://github.com/lindenlab/sansar-script](https://github.com/lindenlab/sansar-script), [https://github.com/lindenlab/sansar-script.github.io](https://github.com/lindenlab/sansar-script.github.io), there are a few ways that you can do that. 

If git is new to you or you need a refresher the article, "[An introduction to Git: what it is, and how to use it](https://www.freecodecamp.org/news/what-is-git-and-how-to-use-it-c341b049ae61/)", by FreeCodeCamp is a nice to the point overview of the most important concepts you should know about. 

If you're not sure what or how you can contribute check out this [open source guide](https://opensource.guide/how-to-contribute/) to get some ideas.

## Pull requests

Github collaboration has  a specific workflow that is centered around pull requests. A pull request is a request that you make to Linden Lab asking that your code be merged into the `master` branch and made publicly available. Because Linden Lab are the owners of sansar-script repositories it is a read only repository when you clone it, you will not have push access and will not be allowed to create branches directly from a clone. Instead you must create a fork of sansar-script repository that will be a copy of the sansar-scripts on your github namespace which you own. 

Rather than document the steps to create a pull request in this post, the [github official forking documentation](https://guides.github.com/activities/forking/) has everything you need to know about how to fork a repository, make additions or changes and submit a pull request.

## Submodules

For those of you that maintain a personal repository of sansar scripts and or tutorials on github there is an option to include your repository in the `sansar-script/Users` directory via git submodules. A submodule is at its core a repository embedded in a directory of another repository, github has a nice clear post ["Working with submodules"](https://github.blog/2016-02-01-working-with-submodules/) that calls out the most important things to know about what they are and how they are used.

If you are interested in contributing to sansar-scripts via submodules please [open an issue](https://github.com/lindenlab/sansar-script/issues/new/choose) using the Submodule request issue template.

## Code of Conduct

All contributions and collaborators to the sansar-script library are expected to be respectful and to agree to conduct themselves within the bounds of the repository's [code of conduct](https://github.com/lindenlab/sansar-script/blob/master/CODE_OF_CONDUCT.md) which can be found in the root of the project.