---
title: ""
keywords: homepage
sidebar: sidebar
permalink: index.html
---

# Sansar Scripting Blog

This site is a collection of links from around the web of ways to create and have fun with custom content in Sansar. Inside you 
will find examples, samples, tutorials and more that have been produced by the Sansar community.

All are encouraged to follow Sansar in Discord
[Sansar Official Discord!](http://discord.gg/sansarofficial)

# How to share your content here


## Editing existing content

If you see content on this site that could use an edit, maybe you found a typo or perhaps you're the creator of the content that is linked and you would like to add more links, images or copy to an existing page, you can do all of that through GitHub web interface. All you need is a GitHub account a web browser and a little bit of [Markdown](https://guides.github.com/features/mastering-markdown/) formatting.

<iframe width="560" height="315" src="https://www.youtube.com/embed/4Lt0BeZ8uIw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Adding your own page

You may also add new pages using the GitHub web interface. 

Pages require a block of metadata, called "frontmatter" to be added at the top of the file and looks like the example below. 

    ---
    title:  "Your Page Title"
    summary: "Summary of the content on this page."
    category: blogs
    sidebar: sidebar
    tags: [ examples ]
    permalink: your-page-link.html
    author: Your Name
    last_updated: January 25, 2020
    ---

*if you're ever in doubt just copy an exisiting page and update with your information.*

## Categories and Tags

Pages are organized under a predefined category and can have up to three tags of your own choosing.

If you feel that your work cannot be defined under an existing category you may propose a new category be added.

You may add any new tags you wish by updating the  `/data/tags.yml` file as well as add a template in the `/pages/tags` directory.

Tags with more than one word should be separated by underscores and not exceed three words. e.g. `marvelous_designer`

The content of your page can be in any format that is supported by [Markdown on GitHub](https://guides.github.com/features/mastering-markdown/) and conforms to [content guidelines](#content-guidelines) below.

## Youtube

Youtube embeds work with the `iframe` syntax provided by YouTube's "Share" feature.

![Image of YouTuve embed](/images/youtube-embed.png)

## Building the blog

If you'd like to contribute to the blog templates and functionality you can do so by forking the GitHub code and submitting your code changes through a [Pull Request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests).

The [github official forking documentation](https://guides.github.com/activities/forking/) has everything you need to know about how to fork a repository, make additions or changes and submit a pull request.

This site is created with [Jekyll](https://jekyllrb.com/) using the [Jekyll Documentation Theme](https://idratherbewriting.com/documentation-theme-jekyll/). 

Jekyll is best run on a Unix-like system system, if you are on a Windows [WSL](https://docs.microsoft.com/en-us/windows/wsl/install-win10) is suggested for installing and running this site in development mode, although it is not required that you run and build this application to submit content to the site through GitHub.



## Content Guidelines

All content must conform to [Sansar Content Guidelines](https://help.sansar.com/hc/en-us/articles/115004563063-Content-Guidelines) and our community [Code Of Conduct](/code_of_conduct.html).

