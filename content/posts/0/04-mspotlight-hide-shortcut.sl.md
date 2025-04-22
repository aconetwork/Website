---
title: "Skrijte bljižnico Spotlight s namizja"
date: 2025-04-17T12:00:00+02:00
# publishDate: 2025-04-17T12:00:00+02:00
url: /mspotlight-skriti-bljiznico-sl/
# image: images/2024-thumbs/spotlight-reset.jpg
categories: 
  - kako
tags: 
  - Windows
showtoc: true  # Table of content: Hide (false) or show (true)
draft: true  # Draft: Show (false) or hide (true)
language: "Slovenski"
---

Microsoft Spotlight je orodje, ki spremeni sliko Windows namizja s prenosom slik iz interneta. V tej vodiču vas bom naučil, kako skriti bližnjico `Več o tej sliki` s namizja pa s tem obdržati Spotlight slike na 2 načina.

## Določite svojo sliko ozadja, diaprojekcijo, barvo, ...

(Kliknite na posamezni naslov koraka ali trikotnik, da skrijete ali prikažete podrobnosti (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Z desno miškino tipko kliknite prazno območje namizja Windows in nato z levo miškino tipko kliknite `Prilagodi`" openByDefault=true >}}

 

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Pod `Ozadje` z levo miškino tipko kliknite na `Windows spotlight` da izberete kaj vi želite" openByDefault=true >}}

 Želeno možnost `Slika`, `Barva`, `Slideshow` ali `Windows spotlight` lahko potrdite s klikom na levo miškino tipko. Zdaj samo nastavite svoje nastavitve in uživajte.

{{< /collapse >}}

## Skrijte bljižnico `Več o tej sliki` s namizja s pripravljeno registrko datoteko (lažji način)

Če želite SAMO skriti bližnjico na namizju `Več o tej sliki`, morate dodati nov ali spremeniti obstoječ registrski ključ v registru Windows. Prvi način je, da prenesete registrsko datoteko s končnico `.reg`, ki sem jo pripravil za vas in jo uporabite. Ti datoteki spodaj sem jaz generiral ampak če jim ne zaupate, lahko uporabite [težji način](#ročno-skrijte-bljižnico-več-o-tej-sliki-s-namizja-v-registru-windows-težja-metoda "Kliknite/tapnite da skočite na ta odsek!") spodaj v naslednjem odseku. Torej:

(Kliknite na posamezni naslov koraka ali trikotnik, da skrijete ali prikažete podrobnosti (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Presnamite registersko datoteko" openByDefault=true >}}

 Za skriti bljižnico uporabite [spotlight-desktop-icon-hide.reg](/scripts/spotlight-desktop-icon-hide.reg "Click/tap to download the file!") in za prikaz skrite bljižnice pa uporabite [spotlight-desktop-icon-show.reg](/scripts/spotlight-desktop-icon-show.reg "Click/tap to download the file!").

 1. Za prenos z desno miškino tipko kliknite povezavo in z levo miškino tipko kliknite `Shrani povezavo kot`.

    

 2. Odprite želeno mapo kamor jo želite shraniti in z levo miškino tipko kliknite na gumb `Shrani`.



{{< /collapse >}}

{{< collapse summary="**Korak 2:** Odprite mapo v katero ste prenesli datoteko in jo odprite z levo miškino tipko" openByDefault=true >}}

 Če se odpre `Nadzor uporabniškega računa` ali katero koli drugo varnostno okno z levim gumbom miške kliknite gumb `Da`, da potrdite, da dovolite njegovo odpiranje.

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Z levo miškino tipko kliknite gumb `Da` v oknu `Urejevalnik registra`" openByDefault=true >}}



{{< /collapse >}}

{{< collapse summary="**Korak 4:** Ko je datoteka registra uspešno uvožena z levo miškino tipko kliknite tipko `Ok`" openByDefault=true >}}

  

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Osvežite namizje za uveljavitev spremembe" openByDefault=true >}}

  In to je to.

{{< /collapse >}}

## Ročno skrijte bljižnico `Več o tej sliki` s namizja v registru Windows (težja metoda)

(Kliknite na posamezni naslov koraka ali trikotnik, da skrijete ali prikažete podrobnosti (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** S levo miškino tipko kliknite na Start meni tipko" openByDefault=true >}}



{{< /collapse >}}

{{< collapse summary="**Korak 2:** Začnite pisati na tipkovnici `Urejevalnik registra` in ga odprite z levo miškino tipko na `Urejevalnik registra`" openByDefault=true >}}

  Če se odpre `Nadzor uporabniškega računa` ali katero koli drugo varnostno okno z levim gumbom miške kliknite gumb `Da`, da potrdite, da dovolite njegovo odpiranje.

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Z levo miškino tipko kliknite tipko `Da` v oknu `Urejevalnik registra`" openByDefault=true >}}

  Če se odpre `Nadzor uporabniškega računa` ali katero koli drugo varnostno okno z levim gumbom miške kliknite gumb `Da`, da potrdite, da dovolite njegovo odpiranje.

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Pojdite na ključ `NewStartPanel`" openByDefault=true >}}

  Lokacija: `Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\HideDesktopIcons\NewStartPanel`

Kopirajte in prilepite ali vpišite lokacijo v zgornje polje za vnos besedila in pritisnite tipko `Enter` na tipkovnici ALI preprosto odpirajte ključe dokler ne pridete v `NewStartPanel`.

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Izdelajte ključ `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` ampak če pa že obstaja pa preskočite ta korak in pojdite na `Korak 6`" openByDefault=true >}}

  1. Prepričajte se, da ste znotraj `NewStartPanel` in z desno miškino tipko kliknite na prazno območje.
  2. Pojdite na Novo in z levim gumbom miške kliknite `DWORD (32-bit) Value`.
  3. Vnesite `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` (ali kopirajte in prilepite) in pritisnite tipko Enter na tipkovnici.

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Z desno miškino tipko kliknite na novo narejen ključ `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` in s levo miškino tipko klinite na `Uredi`" openByDefault=true >}}

 

{{< /collapse >}}

{{< collapse summary="**Korak 7:** Pod `Podatki o vrednosti` se prepričajte, da je `1` in ne `0` in z levo miškino tipko kliknite na tipko `V redu`" openByDefault=true >}}

  

{{< /collapse >}}

{{< collapse summary="**Korak 8:** Osvežite namizje za uveljavitev spremembe" openByDefault=true >}}

  In to je to.

{{< /collapse >}}

## Video verzija
<!--
{{< youtube "" >}}
-->