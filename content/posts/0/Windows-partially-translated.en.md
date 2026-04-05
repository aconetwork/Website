---
title: "Windows Partially Translated"
date: 2025-04-10T22:22:03+02:00
# publishDate: 2025-04-10T22:22:03+02:00
url: /Windows-partially-translated/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
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
showtoc: false  # Tabela sadržaja: Sakriti (false) ili pokazati (true).
draft: true   # Prikaz na javnoj stranici: Prikaz (false) ili sakriti (true).
language: "Srpski"
---

using elevated powershell prompt.

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

   Set-WinUserLanguageList -LanguageList (New-WinUserLanguageList -Language sr-Latn-RS) -Force

   Language codes: https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/available-language-packs-for-windows?view=windows-11

Restart the computer after settup.

If Windows is partially translated remove old language and restart computer. After that in my case Windows settings and start menu did not open but I opened Terminal and reinstalled old language. When it is done, restart your computer and your system should be translated.