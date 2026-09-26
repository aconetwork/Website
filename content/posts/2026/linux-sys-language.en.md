---
title: "Linux Sys Language"
date: 2026-09-25T18:00:00+02:00
# publishDate: 2026-09-25T18:00:00+02:00
url: /linux-sys-language-en/
# image: images/2024-thumbs/linux-sys-language.jpg
categories: 
  - How to
tags: 
  - How to
  - Linux
showtoc: true  # Table of content: Hide (false) or show (true)
draft: false  # Draft: Show (false) or hide (true)
language: "English"
---

Today we are changing Linux operating system system language, how to install and remove language, apply new settings and more. 

{{< notice tip >}}
  If you do not know the language your system is in just follow the icons in the tutorial, they are the same. [Restarting the computer](#restarting-the-computer "Click/tap to visit the section!") 
{{< /notice >}}

{{< notice warning >}}
  When you finish making language changes just restart your computer to apply new settings fully!
{{< /notice >}}

## Get to the Language window and it's elements

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** left mouse button click on the `LM` menu button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** left mouse button click on the `System settings` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_sys_settings_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** left mouse button click on the `Languages` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_sys_settings_-_languages_btn_hover.jpeg">}}

{{< /collapse >}}

Now you have `Language Settings` window open.

{{< figure align=center src="/images/LinuxMint/en_-_language_settings_window.jpeg">}}

To change curent user profile language settings change first 3 elements based on alerady installed languages (check the [Set the new language settings for the user](#set-the-new-language-settings-for-the-user "Click/tap to visit the section!") guide) but if it not there then install it, check the (check the [Install new language](#install-new-language "Click/tap to visit the section!") guide bellow.

To change whole system language (default fallback system language settings, login window, other profiles, ...) check the [Apply selected user language settings system wide](#apply-selected-user-language-settings-system-wide "Click/tap to visit the section!") guide bellow.

To install or remove some language use the `Install/Remove Languages... button`, check the [Install new language](#install-new-language "Click/tap to visit the section!") and [Remove installed language](#remove-installed-language "Click/tap to visit the section!") guide bellow.

## Set the new language settings for the user

- **Language** language for the Linux user profile.
- **Region** region for the user.
- **Time format** time and date format for the user.

{{< figure align=center src="/images/LinuxMint/en_-_installed_language_list_-_language_btn_hover.jpeg" title="Example of the installed languages list install">}}

{{< notice tip >}}
  Remember that if you do not have desired language installed just follow [Install or remove new language](#install-or-remove-new-language "Click/tap to visit the section!") guide.
{{< /notice >}}

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Change user language:** left mouse button click on the current language button and then select the desired language from the list with the left mouse button click" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_language_settings_window_-_language_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Change user region:** left mouse button click on the current `Region` button and then select the desired language from the list with the left mouse button click" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_language_settings_window_-_region_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Change user date and time format:** left mouse button click on the current `Time format` button and then select the desired language from the list with the left mouse button click" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_language_settings_window_-_time_format_btn_hover.jpeg">}}

{{< /collapse >}}

## Apply selected user language settings system wide 

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** left mouse button click on the `Apply System-Wide` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_language_settings_window_-_apply_system_wide_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** in the `Authentication Required` window type in your current logged-in user password and confirm it with the left mouse button click on the Authenticate button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_auth_req_-_languages_-_authenticate_btn_hover.jpeg">}}

{{< /collapse >}}

## Install new language

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** left mouse button click on the `Install/Remove Languages... button` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_language_settings_window_-_inst_rem_langs_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** in the Authentication Required window type in your cuttent logged-in user password and confirm it with the left mouse button click on the Authenticate button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_auth_req_-_languages_-_authenticate_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** in the new window `Install / Remove Languages` and then left mouse button click on the `Add...` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_add_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 4:** in the new window `Add a new Language` left mouse button click on the desired language and confirm it with the left mouse button click on the `Install` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_inst_new_language_window_-_german_luxenburg_hover.jpeg" title="Example of a selected language">}}
  {{< figure align=center src="/images/LinuxMint/en_-_inst_new_language_window_-_install_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 5:** in the previous window `Install / Remove Languages` left mouse button click on the language you installed and then left mouse button click on the `Install language packs` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_ger_lux_hover_lps_missing.jpeg" title="Example of installed language">}}
  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_install_lang_packs_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_installing_packages_window.jpeg">}}
  
  Now wait untill all packets are installed.

{{< /collapse >}}

{{< collapse summary="**Step 6:** left mouse button click on the `Close` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_close_btn_hover.jpeg">}}

{{< /collapse >}}

Now you can change your language like we did in the [Set the user new language settings](#set-the-user-new-language-settings "Click/tap to visit the section!") guide

## Remove installed language

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** left mouse button click on the `Install/Remove Languages... button` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_language_settings_window_-_inst_rem_langs_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** in the Authentication Required window type in your cuttent logged-in user password and confirm it with the left mouse button click on the Authenticate button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_auth_req_-_languages_-_authenticate_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** in the new window `Install / Remove Languages` left mouse button click on the desired language to remove and then left mouse button click on the `Remove` button" openByDefault=true >}}

  Do this for all the languages you want to remove.

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_ger_lux_hover.jpeg">}}

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_remove_btn_hover.jpeg">}}

  If `Aditional software has to be removed` window shows up just left mouse button click on the `Continue` button.

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_additional_to_remove_window_-_continue_btn_hover.jpeg">}}

  Now just wait untill all the packages are removed.

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_removing_packages_window.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 4:** left mouse button click on the `Close` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_close_btn_hover.jpeg">}}

{{< /collapse >}}

## Restarting the computer

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** left mouse button click on the `LM` menu button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** left mouse button click on the red `Shut Down` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_shut_down_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** left mouse button click on the `Restart` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_shut_down_window_-_restart_btn_hover.jpeg">}}

{{< /collapse >}}

## Links

- [Linux tutorials on this site](/en/tags/linux/ "Click/tap to open the site!")
- [Linux Mint](https://linuxmint.com/ "Click/tap to open the site!")
- [Make new Linux user in few ways + more](/linux-new-user-en "Click/tap to open the site!")
- [Linux playlist - YouTube](https://www.youtube.com/playlist?list=PLAqqAAF5KyKw "Click/tap to open the site!")

## Video version

*(25.09.2026, 18:00 / 06:00 PM, timezone: CEST / UTC+2 / GMT+2)*

{{< youtube "aLugf2c_jfM" >}}