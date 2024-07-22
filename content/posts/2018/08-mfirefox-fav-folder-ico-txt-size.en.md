---
title: "How to change font size and bookmark folder icon in Mozilla Firefox"
date: 2018-08-14T18:00:00+02:00
url: /firefox-txt-size-folder-ico/
# image: images/2024-thumbs/08-mfirefox-fav-folder-ico-txt-size.jpg
categories: 
  - how to
tags: 
  - Windows
  - Mozilla Firefox
showtoc: true  # Table of content: Hide (false) or show (true)
draft: false  # Draft: Show (false) or hide (true) on page
language: "English"
---

Let's set Firefox font size and change bookmarks folder icons. **Before** you do this be sure that:
- inside `about:config` and set the `toolkit.legacyUserProfileCustomizations.stylesheets` (quick left mouse button double-click) to `true`, quick tutorial you can find here: [Fix Mozilla Firefox ignoring userChrome.css](https://www.youtube.com/watch?v=3F_wSkMin8Q&list=PLbvZxzmdNckxgR98xK9iSVsO4bySit-q2 "Click/tap to visit the guide!"),
- inside your file explorer you can see the file extensions like `.exe`, `.txt`, `.msi`, `.docx`, ... like for example `file.exe` and not just the file name like `file`. You can see how to do it in the [walkthrough video at time 01:59](https://youtu.be/wWs_UwVntFU?si=jACAf5M_ZNkZE4MJ&t=119 "Click/tap to jump on that video section!")

## Open Firefox profile folder

1. Left mouse button click on the menu button ![](/images/Mozilla-Firefox/mfirefox_menu_button.jpeg) and then Left mouse button click `Help`.
   
   ![test](/images/Mozilla-Firefox/mfirefox_menu_help.en.jpeg)

2. Left mouse button click on `Troubleshooting Information`.
   
   ![](/images/Mozilla-Firefox/mfirefox_menu_troubleshooting_info.en.jpeg)

3. Left mouse button click on the button `Open Folder` in the same line of the `Profile Folder`.
   
   ![](/images/Mozilla-Firefox/mfirefox_troubleshooting_info.en.jpeg)

You can also open your file explorer and go to browsers profile folder similar to this:

    C:\Users\WINDOWS_PROFILE\AppData\Roaming\Mozilla\Firefox\Profiles\FIREFOX_PROFILE_NAME.default

Replace `WINDOWS_PROFILE` with your Windows profile name and replace `FIREFOX_PROFILE_NAME` with Firefox profile name.

## Create the necesarry file and prepare it

Before you do anthing be sure that file extensions are showed in your file explorer, check the [walkthrough video at time 01:36](https://youtu.be/wWs_UwVntFU?si=jACAf5M_ZNkZE4MJ&t=96 "Click/tap to jump on that video section!"). Folder and a file needs to be **EXACTLY** the same as written in steps bellow.

1. In the Firefox profile folder create a folder named `chrome` and open it.
2. Create regular text file and rename it to `userChrome.css`.
3. Now open the newly created file `userChrome.css` with prefered text editor.
4. At the very beggining make sure you type in or copy and paste exactly like this: 
   
       @namespace url(http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul);

5. Save the changes you've made. Not all programs have same way of saving the file but usually you can do that by left mouse button click on `File` in the top main menu and left mouse button click on `Save`, keyboard shortcut to save is `CTRL + S` (click `CTRL` and while pressing it click `S` and then release both buttons).

## Doing the changes to userChrome.css

Inside `userChrome.css` should be like:

    @namespace url(http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul);
    
    /* Changing all bookmarks folder icons */
    .bookmark-item[container] {
        list-style-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAjklEQVR42mNkAIIfx2xbgVQWAwHw//9/hh9cVgxX7ny5aBs6zQEkxgg1YD2QCiBkAAgwCdowXH0u8cHQKV9w1ICBNODaC4kvH24vUHVIO/+CLANuvhJnUGVdu4PD6rAnJQYcABrgOMIN2A00wI3MaBT/+vHOQl371PP3YQYQn505rRgu3/180S50ugNIDACEZogRw/LarAAAAABJRU5ErkJggg==') !important;
    }

    /* Global UI font size */
    * { font-size: 12pt !important; }

After you make the changes **ALWAYS** save the changes to a file othervise Firefox will not see them. Whatever is between `/*` and `*/` is the comment and firefox will ignore that text. 

Let's deconstruct above code bellow... . 

### First part: to select the bookmarks folders icon

    /* Changing all bookmarks folder icons */
    .bookmark-item[container] {
        list-style-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAjklEQVR42mNkAIIfx2xbgVQWAwHw//9/hh9cVgxX7ny5aBs6zQEkxgg1YD2QCiBkAAgwCdowXH0u8cHQKV9w1ICBNODaC4kvH24vUHVIO/+CLANuvhJnUGVdu4PD6rAnJQYcABrgOMIN2A00wI3MaBT/+vHOQl371PP3YQYQn505rRgu3/180S50ugNIDACEZogRw/LarAAAAABJRU5ErkJggg==') !important;
    }

You put your icon in between apostrofies in `url` like for example `icon.png` where the actual icon file is in the `chrome` folder we created earlier, example:

    list-style-image: url('icon.png') !important;

You can use `base64`, `svg`, `png`, `jpg`, `jpeg`, `bmp`, ... depends on your need.

This code sets one icon for all of the folders but in case you want to change individual folder icon you need to change `.bookmark-item[container]` to `.bookmark-item[container][label="Folder name"]` where `Folder name` is the title of your folder in the browser bookmarks. For the next folder just duplicate `.bookmark-item[containe...}` and change `Folder name` with the icon, here is an example:

    /* Changing first folder bookmark icon */
    .bookmark-item[container][label="Folder name"] {
        list-style-image: url('First_folder_icon.png') !important;
    }

    /* Changing second folder bookmark icon */
    .bookmark-item[container][label="Second folder name"] {
        list-style-image: url('Second_folder_icon.png') !important;
    }

### Second part: to set the global Firefox text size

    /* Global UI font */
    * { font-size: 12pt !important; }

Change the number `12pt` to whatever size you want like for example `16pt` and save the changes to a file. Change just the number, `pt` stays always there.

## Guide in other languages

- [Slovenski (Slovenian)](https://www.youtube.com/watch?v=U-uOC7PB4uE&list=PLbvZxzmdNckyeHQYbvDKF3GK58peTHdnl "Kliknite/tapnite da odprete! Click/tap to open!")
- [Srbski (Serbian)](https://www.youtube.com/watch?v=qgD5EVDq4uo&list=PLbvZxzmdNckxgR98xK9iSVsO4bySit-q2 "Kliknite/tapnite da otvorite! Click/tap to open!")

## Walkthrough Video

{{< youtube "wWs_UwVntFU" >}}