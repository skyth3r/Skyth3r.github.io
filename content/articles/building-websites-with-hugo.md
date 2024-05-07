---
title: Building websites with Hugo
date: 2023-01-20T08:00:00
lastmod: 2024-05-07T18:05:00
images: 
- /img/setting-up-hugo/setting-up-hugo-header.png
description: A guide on building your own website for free using Hugo and Github Pages.
tags: ['web-dev', 'hugo', 'guide']
---

In the last few months, there has been a flurry of activity around [personal blogs](https://www.theverge.com/23513418/bring-back-personal-blogging) and [owning your own data](https://www.brycewray.com/posts/2022/11/own-your-stuff/), since [Musk took the reins of Twitter](https://www.theverge.com/23551060/elon-musk-twitter-takeover-layoffs-workplace-salute-emoji).

With that, a lot of people have been wondering how they can start their own websites. Since re-launching my website, I've had people ask me how they can make their own website in the last few weeks. To avoid repeating myself, I've put together a guide on how you can build a website using Hugo and GitHub Pages.

[Other guides exist](https://kinsta.com/blog/hugo-static-site/), but this one covers how I've set up my website in a simple and easy-to-follow guide.

For this demo, I'm going to be using the [Hugo Bear Blog theme](https://github.com/janraasch/hugo-bearblog) as it's a nice minimalist theme to start with. My website uses a theme called [Digital Garden](https://github.com/apvarun/digital-garden-hugo-theme). The [installation steps](https://digital-garden-hugo-theme.vercel.app/articles/installation/) for this theme are slightly more complicated. This guide will focus on using a simpler theme to demonstrate the basics of building websites with Hugo. There are many other [free Hugo themes](https://themes.gohugo.io/) you can choose from as well on the official Hugo website. 

**One minor note**

While it's not needed, I would recommend spending some money and buying a domain name. Usually, most people want a domain in the format of firstNameLastName[dot]com, but you can pick anything you like. For example, Sophie's domain is [localghost.dev](https://localghost.dev/), a fun play on words for localhost. 

A domain name shouldn't cost too much and you can buy one from several domain name registrars. I bought my domain name, akashgoswami.com via [Google Domains](https://domains.google/) and pay £10 a year for it (that's less than £1 a month!).

## What is Hugo?
[Hugo](https://gohugo.io/) is a fast static site generator tool written in [Go](https://go.dev/). It uses templates and markdown files to generate webpages in seconds. The final result is a set of HTML files that you can deploy as a website using a hosting provider such as [GitHub Pages](https://pages.github.com/).

Let's use an analogy. Let's pretend that we're making a sandwich, instead of building a website 🥪

We prepare our sandwich by laying out all the ingredients that we want to include in our sandwich. Once that's done, you simply run the 'make sandwich' command to create a sandwich within seconds.

Now imagine we want to swap out some of those ingredients, add new ones or remove some we don't like. We can run the 'make sandwich' command again and have a new sandwich created with these changes.

That's how Hugo works, but instead of making a sandwich, it generates the files needed to make a website.

## Prerequisites

Before we start building our website, there are a few things you'll need beforehand.

### A text editor

You'll need something to edit your code in. I like using [Visual Studio Code](https://code.visualstudio.com/).There are some [handy Hugo extensions](https://gohugo.io/tools/editors/#visual-studio-code) that you can install within Visual Studio Code as well.

### Familiarity with using a command line app

You'll need to navigate around files and run some Hugo commands using the command line interface. On macOS, the built-in command line tool is called 'Terminal' (but I prefer using [iTerm2](https://iterm2.com/)) and on Windows it's Powershell. 

### A Package Manager

Hugo can be installed as a [prebuilt binary](https://gohugo.io/installation/) but I prefer using a package manager. For macOS, you'll want to use Homebrew. For Windows, it's Chocolatey. The installation guides for both of these package managers is well documented so I'll leave the links to official installation instructions below.

macOS - [Installation instructions for Homebrew](https://brew.sh/)

Windows - [Installation instructions for Chocolatey](https://chocolatey.org/install)

Linux - If you use a Linux-based OS then you can find the [correct installation steps for your Linux distro here](https://gohugo.io/installation/linux/)

### GitHub (and Git)

To host the website, we're going to use GitHub Pages, so you'll need a [GitHub](https://github.com/) account. Create an account (please also enable 2-factor authentication) and then install [GitHub Desktop](https://desktop.github.com/).

You'll also need to install Git via your package manager if it's not already on your machine:

macOS

```
brew install git
```

Windows

```
choco install git.install
```

## Setting up our website

First up, open the command line and navigate to where you want to create your website project file. I choose to create mine in Users/Akash (the default directory when you open Terminal on macOS). 

Then, run the following command (but replace username with your GitHub username):

```
hugo new site username.github.io
```

This creates a new folder under the same name that contains some starter files for your Hugo website.

Then run the following two commands to navigate into this newly created folder and create a git repository:

```
cd username.github.io
git init
```

After that, we want to add our Hugo theme and set it as well by using the following two commands

```
git submodule add https://github.com/janraasch/hugo-bearblog themes/hugo-bearblog
echo "theme = 'hugo-bearblog'" >> hugo.toml
```

### Modifying the site

Now that the website is set up, you can add your own content to it. 

It's best to refer to a theme's recommended instructions. For [hugo-bearblog theme](https://github.com/janraasch/hugo-bearblog/), it's best to refer to the [exampleSite folder](https://github.com/janraasch/hugo-bearblog/tree/master/exampleSite) with the theme.

### Testing and building the site

Once that's done you can spin up the website by running `hugo server` and then visiting http://localhost:1313/

To stop the web server, just enter the command mentioned in your command line application (for macOS its Ctrl+C).

Once you've made your changes, you can build your website by running the `hugo` command. This will update the files within your public folder, which you can then deploy to a hosting service.

## Uploading the website to GitHub

Now that we're happy with our website, we'll want to upload it to GitHub. Open the GitHub Desktop application and then go to File > Open Local Repository. 

Make sure you tick all the files and then enter a commit message. It doesn't have to be too fancy, 'first commit' works well. Once you've done that, click 'Commit to main' and then the 'Publish repository' button. A popup will appear asking you to name your new repository. Name it 'username.github.io' and set it to be public before you click the 'Publish Repository' button.

### GitHub Actions

To deploy your website, open the new repository via GitHub on a web browser, and then head to Settings > Pages. 

From here you can switch the source to 'GitHub Actions' and the default Hugo action should be suggested. Click configure button and then commit the code to your main branch.

If you now head back to the Actions tab you can see a workflow running to build your website.

#### Setting your domain name (Optional)

If you have a custom domain, you can set your website's name from the Custom Domain section of the Pages settings page. You'll also need to set your DNS records from your domain registrar to point to GitHub. 

## Wrapping up

Once your website has been built, you can view it by entering either username.github.io or your custom domain name from your web browser!

That's it! You've built your own website 🎉

Now that you know the basics, feel free to edit anything you like; switch themes, write new posts, the choice is yours. You can now host your own website, and push new content to it by syncing your changes from your machine to GitHub via GitHub Desktop. Just remember to also run the `hugo` command to rebuild the website after making any changes.

If you found this guide helpful at all or want to suggest an improvement, feel free to reach out to me and let me know.