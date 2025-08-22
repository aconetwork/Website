---
title: "How to install and use Bulk Crap Uninstaller (basics)"
date: 2025-08-22T00:00:00+02:00
# publishDate: 2025-08-03T15:59:51+02:00
url: /bcu-en/
# image: images/2024-thumbs/08-bcu-en.jpg
categories: 
  - how to
tags: 
  - Windows
  - Bulk Crap Uninstaller
showtoc: true  # Table of content: Hide (false) or show (true)
draft: false  # Draft: Show (false) or hide (true)
language: "English"
---

[Bulk Crap Uninstaller](https://www.bcuninstaller.com/ "Click/tap to open the site!") (also known as BCUninstaller or short BCU) is free opensource program uninstaller for operating sistems [Windows](https://www.microsoft.com/en-us/windows "Click/tap to open the site!"), there is also option to download the program for [Linux](https://www.linux.org/ "Click/tap to open the site!"), [Mac](https://www.apple.com/mac/ "Click/tap to open the site!"), ... and like any other uninstallers ([Revo Uninstaller](https://www.revouninstaller.com/ "Click/tap to open the site!"), [GEEK UNINSTALLER](https://geekuninstaller.com/ "Click/tap to open the site!"), [IObit Uninstaller](https://www.iobit.com/en/advanceduninstaller.php "Click/tap to open the site!"), [Uninstalr](https://uninstalr.com/ "Click/tap to open the site!") and others) they try to remove leftovers (files, folders, registry entries) by it's own official unninstaller program you uninstalled. BCU has a lot of options and it guide you thru every step. No uninstaller program will delete every single trace every time because of different folder names, etc..

{{< notice warning >}}
  In few cases (low possibility) uninstaller leftover results MAY have unvanted elements that if deleted something other in your system can start missbehaving. No uninstaller program is perfect and I am not responsible for any possible damages! In case something not working good anymore, go to YouTube video comments and write your question.
{{< /notice >}}

{{< notice note >}}
  This tutorial was made on Windows 11 24H2 64-bit
{{< /notice >}}

## Install BCU with winget

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Right mouse button click on the `Start` menu button and then on the `Windows PowerShell` OR `Terminal` as Administrator" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Win10en_-_start_btn_start.jpeg" title="Windows 10 Start" >}}
  {{< figure align=center src="/images/other/win11/Win11en_-_start_btn_start.jpeg" title="Windows 11 Start" >}}
  {{< figure align=center src="/images/other/win10/Win10en_-_start_btn_-_windows_powershell_admin_btn.jpeg" >}}
  {{< figure align=center src="/images/other/win11/Win11en_-_start_btn_-_terminal_admin_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** In new window type in winget command and then press `Enter` key on the keyboard to install BCU" openByDefault=true >}}

  Winget command:

    winget install -e --id Klocman.BulkCrapUninstaller

  Terminal window:

  {{< figure align=center src="/images/other/win11/Win11_-_terminal_window.jpeg" >}}

  `Enter` key on the keyboard:

  {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
  {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}

  In the future I plan making `Winget` tutorial.

{{< /collapse >}}

## Download Bulk Crap Uninstaller setup and portable version

{{< notice tip >}}
  Setup file is intended to install the BCU but portable version not, just run it. Portable version you just download, unpack with archive program like [7zip](https://www.7-zip.org/ "Click/tap to open the site!") or integrated archive extractor included in Windows 10 and 11 (check [portable section](#portable-bcu-unpack-and-run "Click/tap to go to the section!")] to see how to extract and open it) and run it. 
{{< /notice >}}

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** With left mouse button open your web browser and visit the BCU website" openByDefault=true >}}

  In the address area of desired web browser (Google Chrome, Mozilla Firefox, Brave, ...) type in or copy paste BCU website address and press enter key on the keyboard. 
  
  If there is some existing web address in the URL area, left mouse button click in the empty part of URL area so current address is selected and you can start typing your address. If URL area is empy, you can just left mouse button click somewhere inside and start typing.
  
  BCU website:

    https://www.bcuninstaller.com/

  Website URL/address area:

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefoxen_-_url_area.jpeg" title="Mozilla Firefox URL" >}}

  Enter key on the keyboard:

  {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
  {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** On the BCU website left mouse button click on the green button `Download on dAppCDN` or `Download on SourceForge`" openByDefault=true >}}

  You can download it from  `dAppCDN` or  `SourceForge`. For this tutorial I used `SourceForge`.

  {{< figure align=center src="/images/bcu/bcu_-_website_download_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** Left mouse button click on `Files`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcu_-_website_download_-_files.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 4:** Left mouse button click on the newest version" openByDefault=true >}}

  At the time of making this tutorial is latest version is `v5.9`.

  {{< figure align=center src="/images/bcu/bcu_-_website_download_-_files_-_ver5.9.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 5:** Left mouse button click on what you want to download and wait to be downloaded" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcu_-_website_download_-_files_-_ver5.9_-_setup.jpeg" title="Setup/installation" >}}
  {{< figure align=center src="/images/bcu/bcu_-_website_download_-_files_-_ver5.9_-_portable.jpeg" title="Portable" >}}

{{< /collapse >}}


## Install Bulk Crap Uninstaller manually with previously downloaded setup file

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** With left mouse button click open the setup file (in my case is `BCUninstaller_5.9.0_setup.exe`)" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcu_-_file_setup_5.9_mouse_hover.jpeg" title="Setup for the installation" >}}

  If Microsoft Defender SmartScreen notification window shows up, first left mouse button click on the `More info` and then `Run anyway`.

  {{< figure align=center src="/images/bcu/bcu_-_file_setup_-_win11en_smartscreen_-_more_info_btn.jpeg" title="More info" >}}
  {{< figure align=center src="/images/bcu/bcu_-_file_setup_-_win11en_smartscreen_-_run_anyway_btn.jpeg" title="Run anyway" >}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** left mouse button click on the `OK` button and optionally you can change installation language with the left mouse button" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_1_-_language_-_ok_btn.jpeg" title="Setup language" >}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** Left mouse button click on checkbox circle `I accept the licence agreement` to select and then `Next` button" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_2_-_license_-_next_btn.jpeg" title="Program license agreement" >}}

  You can read the license agreement if you desire.

{{< /collapse >}}

{{< collapse summary="**Step 4:** Left mouse button click on the `Next` button but optionally you can change the installation folder by left mouse button click on the `Browse` button" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_3_-_destination_-_next_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 5:** Left mouse button click on the `Next` button, optionally you can select/deselect checkboxes with the left mouse button for the components" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_4_-_components_-_next_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 6:** Left mouse button click on the `Next` button, optionally you can change name and location in the Start menu with the left mouse button click on `Browse` button or just not to create it" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_5_-_start_menu_shortcut_-_next_btn.jpeg" >}}

  `Don't create Start Menu folder` if you do not want it left mouse button click on the chexbox to select it!

{{< /collapse >}}

{{< collapse summary="**Step 7:** Left mouse button click on the `Next` button and optionally if checkbox near the `Create a desktop shortcut` is selected Windows desktop shortcut will be created" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_6_-_win_desktop_shortcut_-_next_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 8:** Review your settings and then left mouse button click on the `Install` button " openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_7_-_ready_to_install_-_install_btn.jpeg" >}}

  If you left mouse button click on the `Back` button you can change previously defined settings in this installation window.

{{< /collapse >}}

{{< collapse summary="**Step 9:** Left mouse button click on the `Finish` button and optionally if checkbox near the `Launch BCUninstaller` is selected BCU program will open after you click `Finish` button" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_8_-_finished_-_finish_next_btn.jpeg">}}

  In case you selected for BCU to open on finished installation you may see notification `Windows User Account Control` if you want to open the `BCUninstaller.exe` just left mouse button click on the `Yes` button to confirm.

  {{< figure align=center src="/images/bcu/bcu_-_bcuninstaller_exe_-_win11en_UAC_-_yes_btn.jpeg" >}}

{{< /collapse >}}

## Portable BCU unpack and run

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Open previously downloaded archive portable file folder" openByDefault=true >}}

{{< /collapse >}}

{{< collapse summary="**Step 2** To unpack it right mouse button click on the BCU archive file (in my case is `BCUninstaller_5.9.0_portable.zip`) and then left mouse button on `Extract All...`" openByDefault=true >}}

  You can upack with archive program like [7zip](https://www.7-zip.org/ "Click/tap to open the site!"), [WinRAR](https://www.win-rar.com/ "Click/tap to open the site!"), ... but for this tutorial I am using Windows 11 (also available in Windows 10) integrated archive extractor. 

  {{< figure align=center src="/images/bcu/bcu_-_file_portable_5.9_-_win11en_extract_all.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** Left mouse button click on the `Extract` button and wait to be extracted, optionally you can change where to unpack with left mouse button click on the `Browse` button" openByDefault=true >}}

  If `Show extracted folder when completed` checkbox is selected upon of finished extracting extracted folder will be open inside Windows file manager.

  {{< figure align=center src="/images/bcu/bcu_-_file_portable_5.9_-_win11en_extract_window_-_extract_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 4:** In the extracted folder left mouse button click on the `BCUninstaller.exe` program" openByDefault=true >}}

  `.exe` extension may be shown or not, it depends on your Windows settings. 

  {{< figure align=center src="/images/bcu/bcu_-_file_portable_5.9_-_win11en_extracted_BCUninstaller.exe_hover.jpeg" >}}

  If `Windows User Account Control` asks you if you want to open the `BCUninstaller.exe` just left mouse button click on the `Yes` button to confirm.

  {{< figure align=center src="/images/bcu/bcu_-_bcuninstaller_exe_-_win11en_UAC_-_yes_btn.jpeg" >}}

  Now you should be able to use the BCU.

{{< /collapse >}}

## BCU first run initial settings

Everytime BCU is opened it will scan your system for the uninstallers to show them on the list. When BCU opens for the first time it will go through initial settings (bellow).

{{< figure align=center src="/images/bcu/bcuen_-_window_-_scanning.jpeg" >}}

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Left mouse button click on the `Continue` button, optionally you can change the program language" openByDefault=true >}}

  If you want to change the program language left mouse button click on the `Default` and change the program language where after selecting left mouse button click on the `Apply` button to confirm your selection.

  {{< figure align=center src="/images/bcu/bcuen_-_welcome_settings_-_1_-_language_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** Set list view options and left mouse button click on the `Continue` button" openByDefault=true >}}

  Left mouse button click on the checkboxes to select/deselect desired options:

  - `Show uninstallers in groups` Uninstallers will be grouped by the first character of the uninstaller title.
  - `Select using checkboxes` If you want to uninstall multiple programs at once, but I prefer checked it off to do one at a time.
  - `Highlight certified uninstallers` Higlight uninstallers certified by relevant authoroties.

  {{< figure align=center src="/images/bcu/bcuen_-_welcome_settings_-_2_-_list_view_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** Leave checkboxes unchecked and left mouse button click on the `Continue` button but if you are advanced user select your options" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_welcome_settings_-_3_-_advanced_users_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 4:** With left mouse button select your options and then left mouse button click on the `Continue` button" openByDefault=true >}}

  Left mouse button click on the checkboxes to select/deselect desired options:

  - `Higlight invalid uninstallers` to higlight invalid/corrupted uninstallers.
  - `Show unregistered applications in the list` Check to show programs that are not registred in Windowsbut it is part of the main program.

  {{< figure align=center src="/images/bcu/bcuen_-_welcome_settings_-_4_-_corrupted_uninstallers_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 5:** With left mouse button select your options and then left mouse button click on the `Continue` button" openByDefault=true >}}

  Left mouse button click on the checkboxes to select/deselect desired options:

  - `Automatically look for updates on aplication start` To check for BCU updates when it starts up.
  - `Automatically send anonymous usage statistics` If you allow the BCU to send usage statistics to it's owner.
  - `Enable user ratings of aplications` Usable to know if program is on good or bad standing. I think if there is no rating for an program BCU will post it as one star.

  {{< figure align=center src="/images/bcu/bcuen_-_welcome_settings_-_5_-_network_access_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 6:** To conclude setup left mouse button click on the `Finish setup` button" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_welcome_settings_-_6_-_setup_finished_-_finish_setup_btn.jpeg" >}}

{{< /collapse >}}

## Uninstalling a program

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Right mouse button on the program you want to uninstall and then left mouse button click on the `Uninstall` button" openByDefault=true >}}

  I am using `VLC media player` for this tutorial.

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_1_-_vlc_-_uninstall_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** Set your options and then left mouse button click on the `Continue` button" openByDefault=true >}}

  Left mouse button click on the checkboxes to select/deselect desired options:

  - `Uninstall` If you want to uninstall desired program with his official uninstaller.
  - `Quiet` Uninstall program without any user input of the official program uninstaller.

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_2_-_confirm_vlc_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** If BCU detects uninstaling program or program connected to it is running BCU will whow this step to stop the program othervise will jump to next step" openByDefault=true >}}

  With left mouse button click on the program to stop from the list and then click `Kill` button. When program is killed, left mouse button click on the `Continue` button.

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_3a_-_close_vlc_-_kill_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 4:** Left mouse button click on the `Continue` button, optionally you can check/uncheck options but leaving it by default is okay" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_4_-_settings_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 5:** Left mouse button click on the `BEGIN UNINSTALLATION` button to start the uninstallation progress" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_5_-_vlc_-_begin_uninstallation_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 6:** Uninstall program with official uninstaller (left) while BCU window waits in the background to be completed" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_6_-_vlc_uninstaller_start_-_ok_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 7:** When uninstalled left mouse button click on the `Close` button" openByDefault=true >}}

  When uninstallation is finished in BCU window you will see the check. In some cases some uninstallers will open some kind of window like an website, close that window or windows to proceed to left mouse button click on the `Close` button.

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_7_-_bcu_detected_vlc_finished_-_close_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 8:** Left mouse button click on the `Yes` button to search for the leftovers and wait untill search is completed" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_8_-_ask_leftovers_-_yes_btn.jpeg" >}}
  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_9_-_searching_for_leftovers.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 9:** With left mouse button select the desired options and then click on the `Delete selected` button, you can also use confidence dropdown..." openByDefault=true >}}

  You can just left mouse button click on the `Delete selected` button but you can do few stuff:

  - Checked checkbox means that leftover will be deleted, while unchecked will not.
  - You can select different confidence levels, good and very good are in almost all cases okay to delete while `Questionable` or `Bad` be carefull about. All results bellow the selected confidence will be ignored. It may be that non of the leftovers are available. If you select `Bad` you will get an notification if you really want to show them because it can be dangerous!

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_10c_-_leftovers_vlc_-_delete_selected_btn.jpeg" title="List of the leftovers" >}}
  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_10a_-_leftovers_vlc_-_confidence_-_bad_sel.jpeg" title="Confidence of the files" >}}
  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_10b_-_leftovers_vlc_-_confidence_-_bad_-_yes_btn.jpeg" title="Bad confidence level notification" >}}

{{< /collapse >}}

{{< collapse summary="**Step 10:** If there are registry leftovers BCU will ask you if you want to create a backup of those registry entries.Left mouse button click on the `Create` button, select the folder where to backup and then left mouse button on `Select Folder`" openByDefault=true >}}

  I used Windows Desktop for registry leftovers backup in this tutorial.

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_10d_-_leftovers_vlc_-_removal_reg_backup_-_create_btn.jpeg" >}}
  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_10e_-_leftovers_vlc_-_reg_backup_-_win11en_-_directory_select_btn.jpeg" title="Select where to save registry leftovers" >}}
  
  Now the program and the traces should be removed.

{{< /collapse >}}

## Few BCU elements

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**BCU main interface**" openByDefault=false >}}

  {{< figure align=center src="/images/bcu/bcuen_-_window_-_left_quick_select_settings.jpeg" title="Left quick select settings" >}}
  {{< figure align=center src="/images/bcu/bcuen_-_window_-_main_menu.jpeg" title="Top main menu" >}}

{{< /collapse >}}

{{< collapse summary="**Reload uninstallers list** manually" openByDefault=false >}}

   {{< figure align=center src="/images/bcu/bcuen_-_main_menu_file__-_reload_uninstallers_btn.jpeg" title="Reload uninstallers list" >}}
   {{< figure align=center src="/images/bcu/bcuen_-_window_-_scanning.jpeg" title="Scanning for the programs" >}}

{{< /collapse >}}

{{< collapse summary="**Tool Startup manager** for Windows" openByDefault=false >}}

   {{< figure align=center src="/images/bcu/bcuen_-_main_menu_tools_-_open_startup_manager_btn.jpeg" title="" >}}
   {{< figure align=center src="/images/bcu/bcuen_-_startup_manager_yes_-_enabled_btn.jpeg" title="Disable on startup" >}}
   {{< figure align=center src="/images/bcu/bcuen_-_startup_manager_no_-_enabled_btn.jpeg" title="Enable on startup" >}}

{{< /collapse >}}

## Links

[Bulk Crap Uninstaller website](https://www.bcuninstaller.com/ "Click/tap to open the site!")

## Video version

*PREMIERE (22.08.2025, 18:00 / 06:00 PM, timezone: CEST / UTC+2 / GMT+2)*

{{< youtube "7Z0XDGHRX0o" >}}