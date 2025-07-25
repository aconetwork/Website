---
title: "Windows Partially Translated"
date: 2025-04-10T22:22:03+02:00
# publishDate: 2025-04-10T22:22:03+02:00
url: /Windows-partially-translated/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - kako
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

using elevated powershell prompt)

   Install-Language "sr-Latn-RS"
   Set-WinUILanguageOverride
   Set-WinUserLanguageList -LanguageList (New-WinUserLanguageList -Language "sr-Latn-RS") -Force

   Language codes: https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/available-language-packs-for-windows?view=windows-11