---
title: "Windows Partially Translated"
date: 2025-04-10T22:22:03+02:00
publishDate: 2025-04-10T22:22:03+02:00
url: /Windows-partially-translated/
image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - Kako
  - AST
  - AFT
  - ART
  - WIT
  - zdravlje
tags: 
  - Windows
  - Linux
  - Ubuntu
  - Android
  - Šta je to
  - hardver
showtoc: false
draft: true
language: "Srpski"
---

I acountered the issue when I installed Serbian latin (sr-Latn-RS) language and setted it as primary one but after the computer restart Windows was only partialy in Serbian language. Same issue was with the Slovenian and English language at first. So after testing I found out the solution with couple of the commands using PowerShell or Terminal opened as administrator. Just copy lines bellow and paste it in to the PowerShell or Terminal with the right mouse button click in the empty area of the window.

Commands (replace sr-Latn-RS with the language code you need, [here is the list of codes](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/available-language-packs-for-windows?view=windows-11 "Click/tap to open the site!")):

    Install-Language sr-Latn-RS  # Installing the desired language with aditionall
    Set-WinUILanguageOverride -Language sr-latn-RS
    Set-WinUserLanguageList sr-Latn-RS -Force
    Restart-Computer -Force

## Meaning of the individual commands:

Install-Language sr-Latn-RS

Set-WinUILanguageOverride -Language sr-latn-RS

Set-WinUserLanguageList sr-Latn-RS -Force

Restart-Computer -Force

**Get all installed languages:**

   Get-InstalledLanguage

**Install the desired language**

   Install-Language sr-Latn-RS

**Display user-preferred language override list:**

If the override setting is not used, it will not return a value othervise you shourld get language list or if language installation is pending it will show you it is pending.

   Get-WinUILanguageOverride
   

**Set the desired language overide** 

   Set-WinUILanguageOverride

OR

   Set-WinUILanguageOverride -Language sr-latn-RS

**Forcibly change user language:**

   Set-WinUserLanguageList sr-Latn-RS -Force

   Set-WinUserLanguageList -LanguageList (New-WinUserLanguageList -Language sr-Latn-RS) -Force

## Set Location to United Kingdom
Set-WinSystemLocale sr-Latn-RS
Set-WinHomeLocation -GeoId 0xF2

## Set regional format (date/time etc.) to English (United Kingdon) - this applies to all users
Set-Culture sr-Latn-RS




--- Copy Settings to System and Welcome Screen ---

This applies the language to the system and the welcome screen

You may need to run this section in a separate user session for it to fully apply

Or use a scheduled task to run it under the logged-on user [7, 9]

    Copy-UserInternationalSettingsToSystem -WelcomeScreen $True

   Language codes: https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/available-language-packs-for-windows?view=windows-11

Restart the computer after settup.

    Restart-Computer -Force

If Windows is partially translated remove old language and restart computer. After that in my case Windows settings and start menu did not open but I opened Terminal and reinstalled old language. When it is done, restart your computer and your system should be translated.