---
title: "QNAP TS-212P dissasembly, cleanup...P"
date: 2025-12-26T00:00:00+01:00
# publishDate: 2025-12-26T08:54:28+01:00
url: /qnap-ts-212p-en/
# image: images/2024-thumbs/12-qnap-ts-212p.jpg
categories: 
  - how to
tags: 
  - how to
  - Hardware
showtoc: true  # Table of content: Hide (false) or show (true)
draft: false  # Draft: Show (false) or hide (true)
language: "English"
---

I got NAS QNAP TS-212P from a friend and today is dissasembly, cleanup, thermal paste replacement and more on the agenda. This is slow NAS but for basic network share, FTP and similar is good enough. NAS is short for Network Attached Storage.

## Dissasembly

{{< notice note >}}
  When you go dissasemble or do any work inside the device do not hurry because if not carefull you can quickly damage something.
{{< /notice >}}

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Remove the two screws in the back" openByDefault=true >}}

   In my case those screws were missing so this part was skipped.

   {{< figure align=center src="/images/qnap_ts-212p/back_2_screws.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** Top part of the case pull to front and away" openByDefault=true >}}

   {{< figure align=center src="/images/qnap_ts-212p/top_case_remove.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** Disconnect fan and 2 SATA connectors and cut the zip-tie holding fan wires" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/3_connectors_side.jpeg" title="connectors" >}}
  {{< figure align=center src="/images/qnap_ts-212p/fan_wire_zip_ties.jpeg" title="Zip-tie" >}}

{{< /collapse >}}

{{< collapse summary="**Step 4:** Unscrew all screws holding disk drives on both sides and remove them" openByDefault=true >}}

  Bottom disk drive when unscrewed slide it towards the forward and then remove it.

  {{< figure align=center src="/images/qnap_ts-212p/disks_screwed_in_1.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 5:** Unscrew 4 screws holding disks cage and motherboard in the case" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/for_disk_metal_case_screws_inside.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 6:** Unscrew fan and remove it" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/fan_screws.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 7:** Peel away metal tape just enough that motherboard can be taken out and remove the motherboard" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/metal_tape_peel_off_usb.jpeg" >}}

{{< /collapse >}}

To take off the cooler, continue reading below.

## Thermal paste replacement

For this I used paper towel, isopropyl alcohol (IPA) and if the old paste is dry and hard which paper towel and IPA is not enough use some plastic to scrape it all off **BUT DO NOT USE METAL** because it damages the cooler! 

If the thermal paste is soft and not dry probably you do not need to replace it.

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** With pliers squize and push out both plastic clips holding the cooler" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/cooler_plastic_clip_squize.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** On the cooler and processor remove old thermal paste (if it is dry and hard)" openByDefault=true >}}

  First put on the surface or paper towel IPA and then clean the old thermal paste off. **Do NOT touch** cleaned area with your fingers!

  {{< figure align=center src="/images/qnap_ts-212p/cooler_dry_thermal_towel_clean.jpeg" >}}

  If it is too dry and hard take some plastic (like old credit card for example) and scrape it off first and later clean it with IPA and towel.

  {{< figure align=center src="/images/qnap_ts-212p/cooler_thermal_plastic_card_remove.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** Put pea size thermal paste on the processor or cooler and attach the cooler back to the motherboard" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/arctic_mx-4_thermal_paste_tube.jpeg" title="ARCTIC MX-4 thermal paste" >}}

  {{< figure align=center src="/images/qnap_ts-212p/spreading_new_thermal_paste.jpeg" title="Spreading it" >}}

  {{< figure align=center src="/images/qnap_ts-212p/cooler_fresh_attach_to_mb.jpeg" >}}

{{< /collapse >}}

## What is next?

You probably want to change the coin battery CR2032 and replacement battery must be the same model! Best way is to check it's voltage (V) with the multimeter (set do direct current (DC)) and make sure it is at least 3-3,1V and if lower than that replace it with new one.

{{< figure align=center src="/images/qnap_ts-212p/cr2032_in_socket.jpeg" title="CR2032" >}}
{{< figure align=center src="/images/qnap_ts-212p/multimeeter_V_DC.jpeg" title="Multimeeter DC" >}}
{{< figure align=center src="/images/qnap_ts-212p/CR2032_voltage_new.jpeg" title="New battery voltage" >}}

Now when all is done just put it back together but in reverse order until that point. Now just connect the power adapter and network cable to turn on and use the device. When you see green light is near `STATUS` in front of the device that means that device is fully booted up and you will be notified with first beep when you power on the device and second beep when it is fully booted up and ready (green status light).

## Reseting the QNAP NAS

{{< notice note >}}
  To reset, login or whatever make sure that the device is powered on and green light is near `STATUS` in front of the device.
{{< /notice >}}

There are several ways to reset the NAS. You can manually do it outside in the back of the device with the `RESET` button or when logged in to the NAS from it's settings.

If you want other reset options, check the [Resources](#resources "Click/tap to open the site!") section.

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**RESET button** in the hole on the back side of the device" openByDefault=true >}}

  When the device is turned on and running with green light near the `STATUS` in front of the device take something thin like tooth pick or something na push and hold the `RESET` button inside the hole for the:

  - **3 seconds for partial reset**
    
    The NAS beeps once to indicate a successful reset and data remains intact.

    The following settings are restored to default:

    - **Admin password:** Reset to default or first MAC address. See here.
    - **Security level:** Set to Low (allows all connections)
    - **Service binding:** All NAS services available on all interfaces
    - **System port:** Set to 8080
    - **Network (TCP/IP) settings:** Switched to DHCP, disables Jumbo Frame and VLANs Port Trunking set to Active Backup (on dual LAN models)

  - **10 seconds for full reset**

    One beep is at 3 seconds and second one at 10 seconds. Data on the drives remains intact.
    - All shared folders are deleted.
    - All system settings are restored to default.

{{< /collapse >}}

## Login with QFinder Pro (download, install, run, scan)

{{< notice note >}}
  To login or whatever make sure that the device is powered on and green light is near `STATUS` in front of the device. Connect network cable to the NAS and your home router to be able to access it from the computers.
{{< /notice >}}

Let's download, install and run the program.

*(Click on the individual step or triangle to hide or show the details (images, info, ...))*

{{< collapse summary="**Step 1:** Open the web page for the `QFinder Pro` and left mouse button click on the `Download` blue button" openByDefault=true >}}

    https://www.qnap.com/en/software/qfinder-pro
  
  You can also search it in your search engine like [Google](https://www.google.com/ "Click/tap to open the site!") and open the result

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_site_-_download_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 2:** Scrool down and left mouse button on the correct installation download button, I have Windows OS so we will click `Download (.exe)`" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_site_-_download_page_-_dl_win_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Step 3:** Open veb browser downloads and left mouse button click on the downloaded file to open it" openByDefault=true >}}

  If `User Account Controll` (UAC) window shows left mouse button click on the `Yes` button.

  {{< figure align=center src="/images/qnap_ts-212p/download_btn_brave.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_file_dl_btn_brave.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_UAC.jpeg" >}}
  

{{< /collapse >}}

{{< collapse summary="**Step 4:** Left mouse button click on the `OK` button" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_1.jpeg" >}}
  

{{< /collapse >}}

{{< collapse summary="**Step 5:** Left mouse button click on the `Next`, `Install` and `Finish` buttons to complete the installation" openByDefault=true >}}

  During the installation with left mouse button click you can check or uncheck checkboxes for aditionall options.

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_next_btn.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_install_btn.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_finish_btn.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_6_checkbox_hover.jpeg" title="Checkbox" >}}
  
{{< /collapse >}}

{{< collapse summary="**Step 6:** First time program asks for the region, just left mouse button click on the `OK` button" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_region.jpeg" >}}

  If Windows gives you alerts about the program just confirm it all. Also to check or uncheck checkboxes left mouse button click them.

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_UAC.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_WSA.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_6_checkbox_hover.jpeg" title="Checkbox" >}}
  
{{< /collapse >}}

{{< collapse summary="**Step 7:** If program shows you error that no devices found left mouse button click on the `OK` button" openByDefault=true >}}

  This can happen if device is not started, device IP network address is not correct, not connected to same network as your computer, ...

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_no_devices_err.jpeg" >}}
  
{{< /collapse >}}

{{< collapse summary="**Step 8:** Left mouse button click on the refresh button to scan network for the NAS device" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_refresh_btn.jpeg" >}}
  
{{< /collapse >}}

{{< collapse summary="**Step 9:** To open `Login` page for your NAS device right mouse button click on the NAS device in the results and then left mouse button click on the `Login` button" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_nas_rmb_login.jpeg" >}}
  
{{< /collapse >}}

{{< collapse summary="**Step 10:** Left mouse button click on the `Login` button" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/nas_login_page_-_login_btn.jpeg" >}}
  
{{< /collapse >}}

{{< collapse summary="**Step 11:** Fill out the credentials and then left mouse button click on the `Login` button" openByDefault=true >}}

  Default username and passoword values:

     admin

  {{< figure align=center src="/images/qnap_ts-212p/nas_login_page_-_login_page_login_btn.jpeg" >}}

  And now you can start configuring your NAS device, enjoy :)
  
{{< /collapse >}}

## Resources

- [QNAP](https://www.qnap.com/ "Click/tap to open the site!")
- [How do I reset my NAS settings?](https://www.qnap.com/en/how-to/faq/article/how-can-i-reset-my-nas "Click/tap to open the site!")
- [QFinder Pro](https://www.qnap.com/en/software/qfinder-pro "Click/tap to open the site!")

## Video version

*(26.12.2025, 18:00 / 06:00 PM, timezone: CET / UTC+1 / GMT+1)*

{{< youtube "3SL-hPF4TK0" >}}