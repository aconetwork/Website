---
title: "Hide Spotlight shortcut from desktop"
date: 2025-04-14T00:00:00+02:00
# publishDate: 2025-04-14T00:00:00+02:00
url: /mspotlight-shortcut-hide-en/
# image: images/2024-thumbs/spotlight-reset.jpg
categories: 
  - how to
tags: 
  - Windows
showtoc: true  # Table of content: Hide (false) or show (true)
draft: true  # Draft: Show (false) or hide (true)
language: "English"
---

Microsoft Spotlight is a tool that changes your Windows desktop background image by downloading the images from the internet. In this tutorial I will teach you to hide the Spotlight desktop shortcut `Learn about this picture` but keep Spotlight pictures in 2 methods.

## Hide `Learn about this picture` desktop icon with prepared registry file (easyer method)

To ONLY remove the desktop shortcut `Learn about this picture` you need to add/modify registry key in a Windows Registry. First way is just to download a reg file I prepared for you and apply it. Let's do it:

(Click on the individual step title or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Download the registry file" openByDefault=true >}}

 To hide the shortcut use [spotlight-desktop-icon-hide.reg](/scripts/spotlight-desktop-icon-hide.reg "Click/tap to download the file!") and to show hidden shortcut use [spotlight-desktop-icon-show.reg](/scripts/spotlight-desktop-icon-show.reg "Click/tap to download the file!").

 1. To download it the right mouse button click on the file link and left mouse button click `Save link as`.

    

 2. Open the desired folder where you want to save it and left mouse button click on the `Save` button.



{{< /collapse >}}

{{< collapse summary="**Step 2:** Open the folder where you downloaded the file and open the file with left mouse button click" openByDefault=true >}}

  If `User Account Control` or any other security window opens up left mouse button click on the `Yes` button to confirm you allow to open it.

{{< /collapse >}}

{{< collapse summary="**Step 3:** Left mouse button click the `Yes` button in the `Registry Editor` window" openByDefault=true >}}



{{< /collapse >}}

{{< collapse summary="**Step 4:** When registry file is succesfully imported left mouse button click on the `Ok` button" openByDefault=true >}}

  

{{< /collapse >}}

{{< collapse summary="**Step 5:** Refresh the desktop to apply the change." openByDefault=true >}}

  In to je to.

{{< /collapse >}}

## Hide `Learn about this picture` desktop icon manually in Windows Registry

(Click on the individual step title or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Left mouse button click on the Start menu button" openByDefault=true >}}



{{< /collapse >}}

{{< collapse summary="**Step 2:** Start typing on the keyboard `Registry Editor` and open it with the left mouse button click on the `Registry Editor`" openByDefault=true >}}

  If `User Account Control` or any other security window opens up left mouse button click on the `Yes` button to confirm you allow to open it.

{{< /collapse >}}

{{< collapse summary="**Step 3:** Left mouse button click the `Yes` button in the `Registry Editor` window" openByDefault=true >}}

  If `User Account Control` or any other security window opens up left mouse button click on the `Yes` button to confirm you allow to open it.

{{< /collapse >}}

{{< collapse summary="**Step 4:** Go to the `NewStartPanel` entry" openByDefault=true >}}

  Location: `Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\HideDesktopIcons\NewStartPanel`

  Eather copy/paste or write the location in top text input field and press `Enter` key on the keyboard OR just open the entryes untill you are inside `NewStartPanel`.

{{< /collapse >}}

{{< collapse summary="**Step 5:** Create `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` key but if it exists skip this step and go to the `Step 6`" openByDefault=true >}}

  1. Make sure you are inside `NewStartPanel` and right mouse button click in the empty area.
  2. Go over New and left mouse button click the `DWORD (32-bit) Value`.
  3. Type in `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` (or copy and paste it) and press Enter key on the keyboard.

{{< /collapse >}}

{{< collapse summary="**Step 6:** Right mouse button click `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` and then left mouse button click `Modify`" openByDefault=true >}}

 

{{< /collapse >}}

{{< collapse summary="**Step 7:** Under the `Value data` make sure it is `1` and not `0` and left mouse button click on the `Ok` button" openByDefault=true >}}

  

{{< /collapse >}}

{{< collapse summary="**Step 8:** Refresh the desktop to apply the change." openByDefault=true >}}

  In to je to.

{{< /collapse >}}

## Video version
<!--
{{< youtube "" >}}
-->