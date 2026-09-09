---
title: "Creating new Linux user"
date: 2026-09-09T17:00:00+02:00
# publishDate: 2026-08-03T20:19:36+02:00
url: /linux-new-user-en/
# image: images/2024-thumbs/new-linux-user.jpg
categories: 
  - How to
tags: 
  - How to
  - Linux
  - Mint
showtoc: true  # Table of content: Hide (false) or show (true)
draft: false  # Draft: Show (false) or hide (true)
language: "English"
---

So this is practically my first Linux tutorial. We will be creating new Linux user from the Linux settings and 2 ways in Terminal. Making new user is not the same on all Linux systems. If you have any questions you can ask internet or write your question in the comments bellow the YouTube video where others and/or I will try to help you.

<a id="username-pass-req"></a>
{{< notice warning >}}
  - **Username** can be maximum of 32 characters. Best practice is to use short username, first character must be ONLY a lower-case letter `a-z` or underscores `_` folowed by lower-case letters `a-z`, numbers `0-9`, underscores `_` and/or hyphens `-`. Non-latin characters (cyrillic, Chinese, Greek, ...) can be used but it is higly un-advised because it can cause compactibility and other issues, so just user best practice ones.
  - **Password** can contain lower case and capital letters `a–z`, numbers `0-9` and/or symbols `!@#$%^&*()_+-=[]{}|;:',.<>/?`, spaces and unicode characters are generally accepted if your Linux environment uses UTF-8 encoding. Minimum lenght is 8 characters.
  - **Keep at least one administrator user** because if you delete all admin accounts and you are left with only standard accounts you you can not manage your Linux anymore and only reinstallation of Linux will help.
{{< /notice >}}

<a id="usr-groups"></a>
{{< notice info >}}
  Here’s a list of the common groups in popular Linux distributions for users to be part up for various functionality:
    
  - **sudo** is essential for administrative privileges, allowing the user to execute commands with root-level access.
  - **adm** is often used to allow access to system logs and administrative tasks.
  - **cdrom** is usually used to allow user access to optical drives.
  - **plugdev** grants permission to access external storage devices like external disk drive and USB drives.
  - **sambashare** grants permission to create and manage Samba (Microsoft Windows) network file shares.
  - **dip** allows access to dial-up modem connections.
  - **lpadmin** grants access to printer and print job administration.
  - **audio** provides access to audio devices.
  - **video** allows access to video capture and GPU hardware.
  - **users** is a basic group for system users.
  - **dialout** typically required for modem and serial device access.
  - **games** is sometimes used to give access to game software.
{{< /notice >}}

{{< notice tip >}}
  - Terminal keyboard shortcut is `CTRL + ALT + T`.
  - Press `Enter` keyboard key to confirm each command line!
{{< /notice >}}

{{< notice note >}}
  This tutorial was made in 64-bit Linux Mint distribution / distro, version 22.3 Zena with Cinnamon flavor.
{{< /notice >}}

## Terminal methods

{{< notice info >}}
  `sudo` is to elevate command like `adduser`, `useradd`, ... with administrative privileges.
{{< /notice >}}

Open the `Terminal` window and create new user with the desired command bellow and always confirm with the `Enter` keyboard key.

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**adduser** wraper/script method " openByDefault=true >}}

  `adduser` is wraper/script for easyer use that uses `useradd` commands. It exists in several Ubuntu based distributions or distros like in our case is Linux Mint. Check the [beggining of this tutorial](#username-pass-req "Click/tap to jump to that part!") for what characters are allowed. 
  
  To create standard user (will convert it later to administrator-sudo):

    sudo adduser tomatobox

  Elevating with `sudo` the script `adduser` to create new user which in our case is `tomatobox` but you choose whatever username you want to create. Result and additional info entry example:

    [sudo] password for testbox:          
    info: Adding user `tomatobox' ...
    info: Selecting UID/GID from range 1000 to 59999 ...
    info: Adding new group `tomatobox' (1001) ...
    info: Adding new user `tomatobox' (1001) with group `tomatobox (1001)' ...
    info: Creating home directory `/home/tomatobox' ...
    info: Copying files from `/etc/skel' ...
    New password: 
    Retype new password: 
    passwd: password updated successfully
    Changing the user information for tomatobox
    Enter the new value, or press ENTER for the default
    Full Name []: TomatoBox
    Room Number []: 
    Work Phone []: 
    Home Phone []: 
    Other []: 
    Is the information correct? [Y/n] y
    info: Adding new user `tomatobox' to supplemental / extra groups `users' ...
    info: Adding user `tomatobox' to group `users' ...

  After each input confirm it with the `Enter` keyboard key.

  - **[sudo] password for testbox:** type in your current logged in user password (in our case is `testbox`) if it asks you.
  - **New password:** type in new password for the new user (check the [beggining of this tutorial](#username-pass-req "Click/tap to jump to that part!") for what characters are allowed). It's normal for Linux not to show you when you type in so it stays empty.
  - **Retype new password:** type in that new password again. It's normal for Linux not to show you when you type in so it stays empty.
  - **Full Name []:** here type in the name for the profile like example `Tomato Box` where we can use spaces and other characters.
  - **Room Number []:** / **Work Phone []:** / **Home Phone []:** / **Other []:**  those you can leave empty or type in what ever you want.
  - **Is the information correct? [Y/n]** here type in `Y` or `y` to confirm all data we entered are correct or `N` / `n` to fix the data. Confirm it all with the `Enter` keyboard key.

  Now new standard user is created with new user's home folder `/home/tomatobox`, added to a newly created user group `tomatobox`. Now let's join new user to groups like `sudo` for administrator privileges and other groups for more access and functionality, of course change `tomatobox` to your new user name and choose desired groups. Example of adding groups to a user:

    sudo usermod -aG sudo,adm,cdrom,plugdev,sambashare,dip,audio,video,dialout,games,bluetooth tomatobox
  
  `sudo` elevates the script `usermod` to join user `tomatobox` to new groups seperated by comma `,` with the flag `-aG` OR `-a -G`. Check the [beggining of this tutorial](#usr-groups "Click/tap to jump to that part!") for each group meaning!

  Now new user is created. I suggest you restart your computer before you log-in into the new profile, little lower I written down how to do it.

{{< /collapse >}}

{{< collapse summary="**useradd** method" openByDefault=true >}}
  
  To create new user (check the [beggining of this tutorial](#username-pass-req "Click/tap to jump to that part!") for what characters are allowed) use:

    sudo useradd -m -s /bin/bash tomatobox2

  - **-m** is a flag to automatically create home folder with new username (our example `/home/tomatobox2`).
  - **-s /bin/bash** `-s` is a flag that defines the path to the user's default login shell which must be followed by the path like in our case is `/bin/bash`. If you exclude `-s /bin/bash` your new user will get `/bin/sh`. `bash` and `sh` are two drifferent shells where `bash` is like `sh` but with more features, better syntax where most commands works the same but they are not the same thing.
  
  To set the password (check the [beggining of this tutorial](#username-pass-req "Click/tap to jump to that part!") for what characters are allowed) for the new user use:

    sudo passwd tomatobox2

  The result is:

    [sudo] password for testbox:          
    New password: 
    Retype new password: 
    passwd: password updated successfully

  - **[sudo] password for testbox:** type in your current logged in user password if it asks you.
  - **New password:** Type in new password for the new user.
  - **Retype new password:** Type in again same new user password.

  To set the full name for the new user use:

    sudo usermod -c "Tomato Box2" tomatobox2

  You write what you want between the quotes but leave the quotes alone! Full name can contain spaces and other characters.

  Now new standard user is created with new user's home folder `/home/tomatobox2`, added to a newly created user group `tomatobox2`. Now let's join new user to groups like `sudo` for administrator privileges and other groups for more access and functionality. Example of adding groups to a user, of course change `tomatobox2` to your new user name:

    sudo usermod -aG sudo,adm,cdrom,plugdev,sambashare,dip,audio,video,dialout,games,bluetooth tomatobox2
  
  `sudo` elevating script `usermod` to join user `tomatobox2` to new groups seperated by comma `,` with the flag `-aG` OR `-a -G`. Check the [beggining of this tutorial](#usr-groups "Click/tap to jump to that part!") for each group meaning!

{{< /collapse >}}

Now when the new user is created and restart the computer to apply changes and then log-in to new user account.

1. Left mouse button click on the `LM` menu button.

   {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_btn_hover.jpeg">}}

2. Left mouse button click on the `Shut down` button.

   {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_power_btn_hover.jpeg">}}

3. Left mouse button click on the `Restart` button in the `Shut down` window.

   {{< figure align=center src="/images/LinuxMint/en_-_shut_down_window_-_restart_btn_hover.jpeg">}}

{{< collapse summary="List all users with home folder" openByDefault=false >}}

    cat /etc/passwd | grep '/home'

  `cat` command shows file content, can combine files and also create new files. With our command we look into `passwd` file located in `/etc` folder and commanting it to show lines that contains only `/home` and here is the result example:
  
    testbox:x:1000:1000:Test Box,,,:/home/testbox:/bin/bash
    tomatobox:x:1001:1001:Tomato Box,,,:/home/tomatobox:/bin/bash
    tomatobox2:x:1002:1002:Tomato Box2:/home/tomatobox2:/bin/bash

  Individual elements in each line are seperated by colon `:`.

  - **testbox** is the user name or login name.
  - **x** – Encrypted password is stored in the `/etc/shadow` file.
  - **1000** – UID (user identification number)
  - **1000** is primary GID (primary identification group number)
  - **Test Box,,,** It may include user’s full name, building and room number, contact person or any other user information seperated by comma `,`.
  - **/home/testbox** Home directory for the user.
  - **/bin/bash** Login shell for the user. Pathnames of valid login shells comes from the `/etc/shells` file.

{{< /collapse >}}

{{< collapse summary="**deluser** to delete specific user and it's home folder" openByDefault=false >}}

    sudo deluser --remove-home tomatobox2

  - **deluser** is command to delete user.
  - **--remove-home** is a flag to permanently delete that user home folder.
  - **tomatobox2** is the username to delete, you write your username you want to delete.

  **Confirm user deletion with the Enter keyboard key and once you delete, profile folder and that user is gone for ever so be sure you want to do it!**

{{< /collapse >}}

## Linux settings method: Users and Groups

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Open the window `Users and Groups` and use password of currently logged in Linux user to show the window" openByDefault=true >}}

  We can open window in few different ways:

  1. Left mouse button click `LM` menu, type `users` and then left mouse button click on the result `Users and Groups`.
     
     {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_search_res_-_users_groups_btn_hover.jpeg">}}

  2. Left mouse button click on the `LM` menu and then click on the `System settings`,
   
      {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_sys_settings_btn_hover.jpeg">}}

      1. left mouse button click in the search box, type `users` and then left mouse button click on the result `Users and Groups` 
     
          {{< figure align=center src="/images/LinuxMint/En_-_sys_settings_-_searchbox_user.jpeg" title="Search box">}}
          {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_sys_settings_-_search_res_-_users_groups_btn_hover.jpeg" title="Result">}}
     
          **OR**
     
     2. scrool down to the bottom and left mouse button click on the `Users and Groups`.
       
        {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_sys_settings_-_scrool_-_users_groups_btn_hover.jpeg">}}

  In new window type in logged-in user password and then left mouse button click on `Authenticate` button.

  {{< figure align=center src="/images/LinuxMint/en_-_auth_req_-_users_groups_-_authenticate_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** left mouse button click on the `Add` button to add new user" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_add_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** fill out the data and then left mouse button click on the `Add` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_new_user_form_-_add_btn_hover.jpeg">}}

  - **Account Type** in our case is `Administrator` but you can also set as `Standard` with limited functionality.
  - **Full Name** is for the user's full name, for example `Tomato Box` or like `John` or whatever you want.
  - **Username** is the actual username (check the [beggining of this tutorial](#username-pass-req "Click/tap to jump to that part!") for what characters are allowed) for your new Linux user profile.

{{< /collapse >}}

{{< collapse summary="**Step 4:** in the previous window left mouse button click on the new user where we can set user details" openByDefault=true >}}
  
  {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_user_tomato_box2_btn_hover.jpeg">}}

  With left mouse button you click on the desired element to change.
  
  {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_user_tomato_box2_elements.jpeg">}}

  - **Account Type** in our case is `Administrator` but you can also set as `Standard` with limited functionality.
  - **Full Name** is for the user's full name, for example `Tomato Box` or like `John` or whatever you want.
  - **Username** is the actual username (check the [beggining of this tutorial](#username-pass-req "Click/tap to jump to that part!") for what characters are allowed).
  - **Groups** which groups user is joined or edit them with few clicks.

{{< /collapse >}}

{{< collapse summary="**Step 5:** set the new user password" openByDefault=true >}}
  
  1. Left mouse button click on the `No password set` button, in the new window input new password in both text boxes and confirm it with the OK button.

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_no_pass_set_btn_hover.jpeg">}}

  2. Type in your same new password in both text boxes and then left mouse button click on `Change` button.

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_change_pass_-_window_change_btn_hover.jpeg">}}

     - **New password** is for your new desired password (check the [beggining of this tutorial](#username-pass-req "Click/tap to jump to that part!") for what characters are allowed).
     - **Confirm password** here you type in the new password again to confirm you wrote it correctly.
     - **Show password** checkbox you can click to show the passwords and then correct them.

{{< /collapse >}}

{{< collapse summary="**Step 6:** set the groups for the new user" openByDefault=true >}}
  
  1. Left mouse button click on the list of groups near the `Groups`.

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_user_tomatobox2_groups_list_btn_hover.jpeg">}}

  2. Select group checkboxes you want that user to be associated with and then left mouse button click on the `OK` button.

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_groups_-_window_OK_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="Deleting the selected acocunt" openByDefault=true >}}
  
  In the main `Users and Groups` window:

  1. In the levt column left mouse button click the username you want to delete.

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_user_tomato_box2_btn_hover.jpeg">}}

  2. Left mouse button click on the `Delete` button on the bottom.

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_delete_btn_hover.jpeg">}}

  3. Left mouse button click on the `Yes` button.

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_delete_-_yes_btn_hover.jpeg">}}

  Now user account and it's home folder is deleted.

{{< /collapse >}}

## Restart and login into new username

Now when the new user is created and restart the computer to apply changes and then log-in to new user account.

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** left mouse button click on the `LM` menu button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** Left mouse button click on the `Shut down` button" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_power_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** left mouse button click on the `Restart` button in the `Shut down` window" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_shut_down_window_-_restart_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 4:** when Linux login screen shows up left mouse button click on the new user" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_login_-_user_tomato_box_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 5:** type in the password and to login press `Enter` keyboard key to log-in" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_login_-_user_tomato_box_pass_enter.jpeg">}}

{{< /collapse >}}

## After you log-in into a new user

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="First you see Welcome window, feel free to research it" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_welcome_window.jpeg">}}

  If you do not want this window to come up again when you turn on your computer just left mouse button click to uncheck the bottom checkbox near the `Show this dialogue at startup`.

  {{< figure align=center src="/images/LinuxMint/en_-_welcome_-_checkbox_checked_hover.jpeg">}}

  {{< figure align=center src="/images/LinuxMint/en_-_welcome_-_checkbox_unchecked_hover.jpeg">}}

  Now you can close this window by clicking ![X](/images/LinuxMint/en_-_close_x_btn_hover.jpeg) button in the top right corner.

{{< /collapse >}}

{{< collapse summary="Change screen resolution if needed" openByDefault=false >}}

  1. In the free space on the desktop right mouse button click and then left mouse button click on the `Display settings`
  
     {{< figure align=center src="/images/LinuxMint/en_-_desktop_-_rmb_-_display_settings_btn_hover.jpeg">}}

  2. Left mouse button click on the selection box near the `Resolution`.
  
     {{< figure align=center src="/images/LinuxMint/en_-_display_-_resolution_selection_hover.jpeg">}}

  3. Left mouse button click on the desired resolution, in my case is 1080p or 1920 x 1080 pixels.
  
     {{< figure align=center src="/images/LinuxMint/en_-_display_-_resolution_-_1080p_select_hover.jpeg">}}

  4. You can change other elements and when all is done left mouse button click on the `Apply` button.
  
     {{< figure align=center src="/images/LinuxMint/en_-_display_-_apply_btn_hover.jpeg">}}

  5. Linux will ask you if you want to keep the settings you set and left mouse button click on the `Keep changes` button.
  
     {{< figure align=center src="/images/LinuxMint/en_-_display_-_keep_settings_-_keep_changes_btn_hover.jpeg">}}

  Now you can close the settings window by clicking ![](/images/LinuxMint/en_-_close_x_btn_hover.jpeg) button in the top right corner.

{{< /collapse >}}

{{< collapse summary="**System Reports** notification" openByDefault=false >}}

  1. Left mouse button click on the `System Reports` button notification.
  
     {{< figure align=center src="/images/LinuxMint/en_-_panel_-_notification_system_btn_hover.jpeg">}}

  2. Wait till system checks are completed.
  
     {{< figure align=center src="/images/LinuxMint/en_-_system_informations_-_system_reports_-_running_checks.jpeg">}}

  3. You can set `Timeshift` if you want by left mouse button click on the `Launch Timeshift` button but because that is not the scope of this tutorial will just left mouse button click on the `Ignore this report` button. Timeshift is very important and you should use it, will do tutorial in the future about it.
  
     {{< figure align=center src="/images/LinuxMint/en_-_system_informations_-_system_reports_-_timeshift_ignore_btn_hover.jpeg">}}

  4. Linux is asking us if you really want to ignore that report, just left mouse button click on the `OK` button.
  
     {{< figure align=center src="/images/LinuxMint/en_-_system_informations_-_system_reports_-_want_to_ignore_-_ok_btn_hover.jpeg">}}

  Now you can close the window by clicking ![](/images/LinuxMint/en_-_close_x_btn_hover.jpeg) button in the top right corner.

{{< /collapse >}}

{{< collapse summary="**Update Manager** notification" openByDefault=false >}}

  1. Left mouse button click on the `Update Manager` button notification.
  
     {{< figure align=center src="/images/LinuxMint/en_-_panel_-_update_manager_btn_hover.jpeg">}}

  2. In the `Welcome to the Update Manager` window just left mouse button click on the `OK` button to confirm.
  
     {{< figure align=center src="/images/LinuxMint/en_-_update_manager_-_welcome_-_ok_btn_hover.jpeg">}}

  Now you can close the window by clicking ![](/images/LinuxMint/en_-_close_x_btn_hover.jpeg) button in the top right corner.

{{< /collapse >}}

## Links

- [Linux tutorial playlist](https://www.youtube.com/playlist?list=PLAqqAAF5KyKw "Click/tap to open the site!")
- [Linux Mint](https://linuxmint.com "Click/tap to open the site!")

## Video version

*(11.09.2026, 18:00 / 06:00 PM, timezone: CEST / UTC+2 / GMT+2)*

{{< youtube "Nu2t9lKPnbU" >}}

<!--*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** TEXTHERE" openByDefault=true >}}

  DATA

{{< /collapse >}}

*(This tutorial was made with Windows 11 24H2 64-bit)*

[]( "Click/tap to open the site!")
![](/images/social-logos/X.png)

{{< figure align=center src="/images/Brave/PICTURE.jpeg" title="" float=left >}}
{{< figure align=center src="/images/Brave/PICTURE.jpeg">}}


{{< recipe-header >}}

  {{< figure align=center src="/images/Recipes/Pancakes_rolled.jpeg" float=left >}}

  DATA

{{< /recipe-header >}}

## Ingredients (for 2 people and 3 servings)

- 

## Process

1. 

Bon appétit :).


## Video version

*(..2025, 18:00 / 06:00 PM, timezone: CEST / UTC+2 / GMT+2)*

{{< youtube "O1DA0HpFK-4" >}}

{{< rawhtml >}}
<p style="color:green;text-align:center;">Hello World!</p>
{{< /rawhtml >}}

{{< notice info >}}
  TEXT
{{< /notice >}}

{{< notice note >}}
  TEXT
{{< /notice >}}

{{< notice tip >}}
  TEXT
{{< /notice >}}

{{< notice warning >}}
  TEXT
{{< /notice >}}

-->