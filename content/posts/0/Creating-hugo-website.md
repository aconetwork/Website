---
title: "Creating Hugo Website"
date: 2024-07-02T09:38:11+02:00
url: /Creating-hugo-website/
# image: images/2024-thumbs/Creating-hugo-website.jpg
categories: 
  - how to
tags: 
  - Windows
  - Linux
  - Ubuntu
showtoc: false  # Table of content to hide (false) or show (true).
draft: true  # Show (false) or hide (true) on page.
---

Hugo is one of the most popular open-source static site generators and it is simple to use.
[Official quick start guide](https://gohugo.io/getting-started/quick-start/ "Click/tap to visit gohugo!")

## Install HUGO and GIT on Linux

[Installation guide](https://gohugo.io/installation/linux/ "Click/tap to visit website Hugo!") on HUGO website. GIT is optional if you need it. All commands can be run with the Terminal.

*With snap*:

    sudo snap install hugo

*Debian-based*:

    sudo apt install hugo
    sudo apt install git-all

*Arch-based*:

    yay -S hugo

*To check if installed correctly and you have installed Hugo v0.112.0 or later*:

    hugo version

*Fedora-based*:

    sudo dnf install hugo
    sudo dnf install git-all

## Install HUGO and GIT on Windows

You can install GIT over Winget or manually download and install from [HERE](https://git-scm.com/download/win "Click/tap to visit git-scm!").

*With Chocolatey (free and open-source package manager for Windows)*:

    choco install hugo-extended

*Scoop (free and open-source package manager for Windows)*:

    scoop install hugo-extended

*Winget (Microsoft’s official free and open-source package manager for Windows)*:

    winget install Hugo.Hugo.Extended
    winget install --id Git.Git -e --source winget

You can also download and install GUI version [GitHub Deskop](https://desktop.github.com/download/ "Click/tap to visit GitHub download site!") for Windows.

## Create new site

You can create your own website theme but it is available alot of themes alerady available to use on [themes.gohugo.io](https://themes.gohugo.io/ "Click/tap to visit HUGO themes site!").

    hugo new site my-new-site --format yaml
    cd my-new-site
    git init
    git clone https://github.com/adityatelange/hugo-PaperMod themes/PaperMod --depth=1

For more methods to install and more information about Papermod theme visit the site [Install / Update PaperMod](https://adityatelange.github.io/hugo-PaperMod/posts/papermod/papermod-installation/ "Click/tap to visit PaperMod!").

    hugo --buildDrafts    # or -D
    hugo --buildExpired   # or -E
    hugo --buildFuture    # or -F

hugo server

Deploy the site

Hugo

https://www.markdownguide.org/

## Verify

## Guide in other languages

- [Slovenski (Slovenian)](// "Kliknite/tapnite da odprete! Click/tap to open!")
- [Srbski (Serbian)](// "Kliknite/tapnite da otvorite! Click/tap to open!")

## Walkthrough Video

<!-- {{< youtube "" >}} -->