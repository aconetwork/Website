---
title: "Disable new sidebar in Mozilla Firefox"
date: 2026-03-31T14:26:20+02:00
# publishDate: 2026-03-31T14:26:20+02:00
url: /firefox-disable-nsidebar-en/
# image: images/2024-thumbs/03-firefox-new-sidebar-disable.jpg
categories: 
  - How to
tags: 
  - How to
  - Windows
  - Linux
  - Mozilla Firefox
showtoc: false  # Table of content: Hide (false) or show (true)
draft: false  # Draft: Show (false) or hide (true)
language: "English"
---

New sidebar in Firefox is annoying it keeps appearing by it self so let's disable and replace it with the bookmarks or history sidebar depends on the browser setting.

{{< figure align=center src="/images/Mozilla-Firefox/mfirefox_new_sidebar_and_button_-_button.en.jpeg">}}

{{< notice tip >}}
  Before you begin make sure you open Mozilla Firefox web browser!
{{< /notice >}}

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Left mouse button click inside Mozilla Firefox URL area, type in `about:config` and then press Enter key on the keyboard" openByDefault=true >}}

  If there is already some text in the box remove or select it and then start typing the address:

    about:config

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_url_-_about_config.jpeg">}}

  {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" title="Left Enter key">}}
  {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" title="Right Enter key">}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** If `Proceed with Caution` warning pops up, left mouse button click on the `Accept the Risk and Continue` button" openByDefault=true >}}
  
  This warning is if you really want to enter advanced browser configurations. If you follow this tutorial exactly you will have no problem at all.

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_about_config_-_button_accept.en.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** Left mouse button click inside the search box and type in `sidebar.rev` to see the `sidebar.revamp` result bellow" openByDefault=true >}}

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_about_config_-_sidebar.revamp_-_true.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Step 4:** Left mouse button click on the `Toggle` button on the end of `sidebar.revamp` line to turn new sidebar on or off" openByDefault=true >}}

  `true` to enable or `false` to disable the new sidebar.

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_about_config_-_sidebar.revamp_-_true_-_button_Toggle.en.jpeg" title="true">}}
  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_about_config_-_sidebar.revamp_-_false_-_button_Toggle.en.jpeg" title="false">}}

{{< /collapse >}}