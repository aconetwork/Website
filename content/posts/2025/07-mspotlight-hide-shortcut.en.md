---
title: "Hide Spotlight shortcut from Windows desktop"
date: 2025-07-25T00:00:00+02:00
# publishDate: 2025-04-14T00:00:00+02:00
url: /mspotlight-shortcut-en/
# image: images/2024-thumbs/spotlight-reset.jpg
categories: 
  - how to
tags: 
  - Windows
showtoc: true  # Table of content: Hide (false) or show (true)
draft: false  # Draft: Show (false) or hide (true)
language: "English"
---

Microsoft Spotlight is a tool that changes your Windows desktop background image by downloading the images from the internet. In this tutorial you will learn how to hide (and show) the Spotlight desktop shortcut `Learn about this picture` but keeping Spotlight background pictures in 2 methods inside Windows Registry.

{{< figure align=center src="/images/other/Win10en_-_desktop_-_learn_about_this_pic.jpeg" >}}

## What to do if security notifications shows up when opening a file or program?

If `Security warning`, `User Account Control` or any other security window shows up when you open some file or some program left mouse button click on the `Yes`, `Run` or whatever button it is to confirm, that you allow to open it.

{{< figure src="/images/other/Win10en_-_msdih_reg_open_file_security_warning_-_run.jpeg" title="Security warning for file opening" >}} {{< figure src="/images/other/Win10en_-_UAC_-_registry_editor_-_yes.jpeg" title="User Account Control for program opening" >}}

## 1. METHOD (easyer): With prepared registry files

In this method you simply download correct registry file and apply it. I created the files but if you do not trust them you can use manual way in the [2. Method](#2-method-harder-manually-inside-the-windows-registry "Click/tap to jump to second method!").

(Click on the individual step title or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Download the correct registry file" openByDefault=true >}}

  To hide the shortcut use [spotlight-desktop-icon-hide.reg](/scripts/spotlight-desktop-icon-hide.reg "Click/tap to download the file!") and to show hidden shortcut use [spotlight-desktop-icon-show.reg](/scripts/spotlight-desktop-icon-show.reg "Click/tap to download the file!").

  1. To download it with the right mouse button click on the file link and then left mouse button click `Save link as...`.
  
     {{< figure align=center src="/images/Brave/Brave_en_-_save_link_as__reg_file.jpeg" >}}

  2. Open the desired folder where you want to save it and left mouse button click on the `Save` button.

     {{< figure src="/images/Brave/Brave_en_-_save_window_-_save_btn.jpeg" >}}

  3. If web browser asks you if you want to keep the downloaded file, left mouse button on `Keep` or whatever button is like in your web browser. I used [Brave](https://brave.com/ "Click/tap to open the website!").

     {{< figure src="/images/Brave/Brave_en_-_save_fiile__-_keep_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** Open the folder where you downloaded the file and open the file with left mouse button click" openByDefault=true >}}

  {{< figure align=center src="/images/other/Win10en_-_desktop_-_file_msdih_reg_open.jpeg" >}}

  if any security window pops up check [what to do](#what-to-do-if-security-notifications-shows-up-when-opening-a-file-or-program "Click/tap to jump to the section!") at the almost top of this web page!

{{< /collapse >}}

{{< collapse summary="**Step 3:** In the `Registry Editor` notification window left mouse button click on the `Yes` button to apply into a registry" openByDefault=true >}}

  {{< figure align=center src="/images/other/Win10en_-_registry_editor_msdih_-_yes.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 4:** When you get notification that registry file is successfully imported left mouse button click on the `Ok` button to close it" openByDefault=true >}}

  {{< figure align=center src="/images/other/Win10en_-_registry_editor_msdih_-_success_-_ok.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 5:** Right mouse button click on the Windows desktop and then left mouse button click on the Refresh button to see the change" openByDefault=true >}}

  {{< figure align=center src="/images/other/Win10en_-_desktop_-_rmb_refresh.jpeg" >}}

{{< /collapse >}}

## 2. METHOD (harder): Manually inside the Windows Registry

To do this correctly do **EXACTLY** as I do otherwise you can damage to your Windows and/or it's content or in best case there will be no change to Windows or elsewhere! If you are not sure, do the easyer [1. Method](#1-method-easyer-with-prepared-registry-files "Click/tap to jump to first method!") instead.

(Click on the individual step title or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Left mouse button click on the Start menu button" openByDefault=true >}}

  {{< figure align=center src="/images/other/Win10_-_start_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** With the keyboard start typing `Registry Editor` and left mouse button click on the result `Registry Editor`" openByDefault=true >}}

  {{< figure align=center src="/images/other/Win10en_-_start_-_search_registry_editor.jpeg" title="Start - searching" >}} {{< figure align=center src="/images/other/Win10en_-_start_-_search_-_registry_editor_open.jpeg" title="Start - searching result" >}}

  if any security window pops up check [here](#what-to-do-if-security-notifications-shows-up-when-opening-a-file-or-program "Click/tap to jump to the section!") almost at the top of this web page!
  
{{< /collapse >}}

{{< collapse summary="**Step 3:** Go to the `NewStartPanel` entry" openByDefault=true >}}

  Location: 
  
    Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\HideDesktopIcons\NewStartPanel

  You can open it it in two ways:
  
  1. With the left mouse button select the location path above, right mouse button click on the selected text and then left mouse button click on the button `Copy`. 

     {{< figure align=center src="/images/Brave/Brave_en_-_selected_text_copy.jpeg" >}}

     Now on the top of `Windows Registry` window in text area remove existing text, right mouse button click in it and left mouse button click `Paste` to paste previously copied text.

     {{< figure align=center src="/images/other/Win10en_-_registry_editor_location_paste.jpeg" >}}

     To confirm new location press `Enter` key on the keyboard.

     {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
     {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}
  
  2. With left mouse button click arrows on the left side of the keys to expand the keys until you are inside `NewStartPanel`.

     {{< figure align=center src="/images/other/Win10_-_registry_editor_-_expand_NewStartPanel.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 4:** Create `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` value but if it alerady exists skip this step and go to the `Step 5`" openByDefault=true >}}

  New value title/name: 
  
    {2cc5ca98-6485-489a-920e-b3e88a6ccce3}

  If you want to create new `Value` with name that already exists, you will get an error massage. New value is still created with default name but you can delete it.

  {{< figure align=center src="/images/other/Win10en_-_registry_editor_-_value_name_exists_err.jpeg" >}}

  To create new value:

  1. With left mouse button select value name `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}`, right mouse button click on the selected text and left mouse button click on the `Copy` button.

     {{< figure align=center src="/images/Brave/Brave_en_-_reg_value_msdih_copy.jpeg" >}}

  2. Make sure you are inside `NewStartPanel` and on the right side of the window, right mouse button click in the empty area, go over `New` and left mouse button click the `DWORD (32-bit) Value`.

     {{< figure align=center src="/images/other/Win10en_-_registry_editor_-_rmb_new_dword32.jpeg" >}}

  3. Now right mouse button click on the selected default value name `New Value #1`, and with left mouse button click click on the `Paste` to paste the previously copied value name `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}`.

     {{< figure align=center src="/images/other/Win10en_-_registry_editor_-_new_dword32_-_paste_title.jpeg" >}}

     To confirm new name press `Enter` key on the keyboard.

     {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
     {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 5:** Right mouse button click on `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` and then left mouse button click on the `Modify` button" openByDefault=true >}}

  {{< figure align=center src="/images/other/Win10en_-_registry_editor_-_dword32_-_rmb_modify.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 6:** Under the `Value data` in text box make sure it is `1` (`1` means hidden shortcut, `0` or deleted value for shown shortcut) and left mouse button click on the `Ok` button to confirm the change" openByDefault=true >}}

  {{< figure align=center src="/images/other/Win10en_-_registry_editor_-_dword32_-_modify_-_1_-_ok.jpeg" >}}

  To change the value just left mouse button click in the text area under the `Value data` (you can use keyboard button `Backspace` or `Del` / `Delete` to delete existing content) and keyboard type in what you need for example `1` .

{{< /collapse >}}

{{< collapse summary="**Step 7:** Refresh Windows desktop to see the change." openByDefault=true >}}

  {{< figure align=center src="/images/other/Win10en_-_desktop_-_rmb_refresh.jpeg" >}}

{{< /collapse >}}

## Video version

*(25.07.2025, 18:00 / 06:00 PM, timezone: CEST / UTC+2 / GMT+2)*

{{< youtube "-7RQ2Vk0p0g" >}}