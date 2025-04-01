---
title: "Change Microsoft Spotlight"
date: 2025-03-08T16:21:55+01:00
# publishDate: 2025-03-08T16:21:55+01:00
url: /mspotlight-en/
# image: images/2024-thumbs/spotlight-reset.jpg
categories: 
  - how to
tags: 
  - Windows
showtoc: true  # Table of content: Hide (false) or show (true)
draft: true  # Draft: Show (false) or hide (true)
language: "English"
---

Microsoft spotlight is a tool that changes your background image by downloading the image from the internet. In this tutorial I will teach you to change to other background option or just to hide the desktop shortcut `Learn about this picture`.

## Define your own background image/animation

(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** In the empty area of Windows desktop right mouse button click and left mouse button click `Personalize`" openByDefault=true >}}

 

{{< /collapse >}}

{{< collapse summary="**Step 2:** Under the `Background` left mouse button click on the `Windows spotlight` to select what you want" openByDefault=true >}}

 You can confirm desired option `Picture`, `Solid color`, `Slideshow` or `Windows spotlight` by left mouse button click on it. Now just set your preferences and enjoy.

{{< /collapse >}}

## Hide `Learn about this picture` desktop icon with registry file

To ONLY remove the desktop shortcut `Learn about this picture` you need to add registry key into a Windows Registry. First way is just to download a reg file I prepared for you and apply it. Let's do it:

(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Download the file `spotlight-desktop-icon-hide.reg` (check the link bellow here)" openByDefault=true >}}

 To hide [spotlight-desktop-icon-hide.reg](/scripts/spotlight-desktop-icon-hide.reg "Click/tap to download the file!") and to show [spotlight-desktop-icon-hide.reg](/scripts/spotlight-desktop-icon-show.reg "Click/tap to download the file!").

 1. To download it the right mouse button click on the file link and left mouse button click `Save link as`.

    

 2. Open the desired folder where you want to save it and left mouse button click on the `Save` button.



{{< /collapse >}}

{{< collapse summary="**Step 2:** Open the folder where you downloaded the file and open the file with left mouse button click" openByDefault=true >}}

  If `User Account Control` window opens up, left mouse button click on the `Yes` button

{{< /collapse >}}

{{< collapse summary="**Step 3:** Left mouse button click the `Yes` button in the `Registry Editor` window" openByDefault=true >}}



{{< /collapse >}}

{{< collapse summary="**Step 4:** When registry file is succesfully imported left mouse button click on the `Ok` button" openByDefault=true >}}

  That is it.

{{< /collapse >}}

## Hide `Learn about this picture` desktop icon manually in Windows Registry

(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Click start menu button" openByDefault=true >}}



{{< /collapse >}}

{{< collapse summary="**Step 2:** Start typing `Registry Editor` and open it with the left mouse button click on the `Registry Editor`" openByDefault=true >}}

  If `User Account Control` window opens up, left mouse button click on the `Yes` button

{{< /collapse >}}

{{< collapse summary="**Step 3:** Left mouse button click the `Yes` button in the `Registry Editor` window." openByDefault=true >}}

  If `User Account Control` window opens up, left mouse button click on the `Yes` button

{{< /collapse >}}

{{< collapse summary="**Step 4:** Go to the `NewStartPanel` entry" openByDefault=true >}}

  Location: `Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\HideDesktopIcons\NewStartPanel`

  Eather copy/paste or write the location in top text input field and press `Enter` key on the keyboard OR just open the entryes untill you are inside `NewStartPanel`.

{{< /collapse >}}

{{< collapse summary="**Step 5:** Create `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` entry if it does not exist but if it exists skip to the `Step 6`" openByDefault=true >}}

  1. Make sure you are inside `NewStartPanel` and right mouse button click in the empty area.
  2. Go over New and left mouse button click the `DWORD (32-bit) Value`.
  3. Type in `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` and press Enter key on the keyboard.

{{< /collapse >}}

{{< collapse summary="**Step 6:** Right mouse button click `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` and left mouse button click `Modify` or just double left mouse button click" openByDefault=true >}}

 

{{< /collapse >}}

{{< collapse summary="**Step 7:** Under the `Value data` make sure it is `1` and not `0` and left mouse button click on the `Ok` button" openByDefault=true >}}

 And that is it.

{{< /collapse >}}


## Video version
<!--
{{< youtube "" >}}
-->