---
title: "Skrijte bljižnico Spotlight s Windows namizja"
date: 2025-07-25T00:00:00+02:00
# publishDate: 2025-04-17T12:00:00+02:00
url: /mspotlight-bljiznica-sl/
# image: images/2024-thumbs/spotlight-reset.jpg
categories: 
  - Kako
tags: 
  - Windows
  - Microsoft Spotlight
showtoc: true  # Table of content: Hide (false) or show (true)
draft: false  # Draft: Show (false) or hide (true)
language: "Slovenski"
---

Microsoft Spotlight je orodje, ki spremeni ozadje namizja sistema Windows tako, da prenese slike z interneta. V tem vodiču se boste naučili na 2 načina kako skriti (ter prikazati) bližnjico Spotlight na namizju `Več o tej sliki` in obdržati Spotlight slike.

{{< figure align=center src="/images/other/win10/Winsl_-_namizje_vec_o_tej_sliki.jpeg" >}} 
{{< figure align=center src="/images/other/win10/Winen_-_desktop_-_learn_about_this_pic.jpeg" >}}

## Kaj storiti, če se pri odpiranju datoteke ali programa prikažejo varnostna obvestila?

Če se pri odpiranju datoteke ali programa prikaže `Varnostno opozorilo`, `Nadzor uporabniškega računa` ali katero koli drugo varnostno okno, z levo miškino tipko kliknite `Da`, `Zaženi` ali kateri koli drugo tipko za potrditev, da dovolite odpiranje.

{{< figure align=center src="/images/other/win10/Winsl_-_msdih_reg_odprtje_fajla_varnostno_opozorilo_-_zazeni.jpeg" title="Varnostno opozorilo za odprto datoteko" >}} {{< figure align=center src="/images/other/win10/Winsl_-_UAC_-_registry_editor_-_da.jpeg" title="Nadzor uporabniškega računa za odpiranje programa" >}}
  
## 1. METODA (lažja): S pripravljenimi registrskimi datotekami

Pri tej metodi preprosto prenesete pravilno datoteko registra in jo uporabite. Datoteke sem ustvaril sam, če pa jim ne zaupate, lahko uporabite ročni način v [drugi metodi](#2-metoda-težja-ročno-znotraj-windows-registra "Kliknite/tapnite za skok na drugo metodo!").

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** Presnamite pravilno registrsko datoteko" openByDefault=true >}}

  Da skrijete bljižnico uporabite [spotlight-desktop-icon-hide.reg](/scripts/spotlight-desktop-icon-hide.reg "Kliknite/tapnite za prenos datoteke!") in da jo prikažete [spotlight-desktop-icon-show.reg](/scripts/spotlight-desktop-icon-show.reg "Kliknite/tapnite za prenos datoteke!").

  1. Za prenos kliknite z desno miškino tipko na povezavo do datoteke in nato z levo miškino tipko kliknite `Shrani povezavo kot...`.

     {{< figure align=center src="/images/Brave/Brave_sl_-_shrani_povezavo_kao_reg_fajl.jpeg" >}}

  2. Odprite želeno mapo kamor želite shraniti datoteko in z levo miškino tipko kliknite na tipko `Shrani`.

     {{< figure align=center src="/images/Brave/Brave_sl_-_shraniti_okno_-_shrani_btn.jpeg" >}}

  3. Če vas spletni brskalnik vpraša, če želite obdržati datoteko, kliknite tipko `Obdrži` oziroma kako je v vašem brskalniku. Jaz sem snemal na spletnem brskalniku [Brave](https://brave.com/ "Kliknite/tapnite, da odprete spletno stran!").

     {{< figure align=center src="/images/Brave/Brave_sl_-_shraniti_fajl_obdrzi_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Odprite mapo, kamor ste prenesneli datoteko in odprite datoteko s klikom na levo miškino tipko nanjo" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsl_-_namizje_-_fajl_msdih_reg_odpreti.jpeg" >}}

  Če se odpre katerokoli varnostno okno ko odpirate program ali datoteko poglejte [tukaj](#kaj-storiti-če-se-pri-odpiranju-datoteke-ali-programa-prikažejo-varnostna-obvestila "Kliknite/tapnite da skočite na odsek!") na vrhu (skoraj) te spletne strani!

{{< /collapse >}}

{{< collapse summary="**Korak 3:** V oknu obvestila urejevalnika registra oziroma `Registry Editor` kliknite z levo miškino tipko na tipko `Da` za uvoz v register" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsl_-_registry_editor_msdih_-_da.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Ko se prikaže obvestilo o uspešnem uvozu v register, z levo miškino tipko kliknite tipko `V redu`, da ga zaprete" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsl_-_registry_editor_msdih_-_uspeh_-_v_redu.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Z desno miškino tipko kliknite na namizje sistema Windows in nato z levo miškino tipko kliknite na tipko Osveži za prikaz spremembe" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsl_-_namizje_-_rmb_osvezi.jpeg" >}}

{{< /collapse >}}

## 2. METODA (težja): Ročno znotraj Windows registra

Da se to naredi pravilno naredite **TOČNO** tako kot jaz sicer lahko poškodujete svoj Windows in/ali njegovo vsebino ali pa v najboljšem primeru ne bo nič spremenjeno v Windows ali kje drugje! Če niste prepričani, uporabite lažjo [1. metodo](#1-metoda-lažja-s-pripravljenimi-datotekami-registra "Kliknite/tapnite za skok na prvo metodo!").

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** z levo miškino tipko kliknite na tipko `Start` oziroma `Začetek`" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsl_-_start_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Na tipkovnici začnite pisati `Registry Editor` (slovensko: urejevalnik registra) in z levo miškino tipko kliknite na rezultat `Registry Editor`" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsl_-_start_-_iskanje_registry_editor.jpeg" title="Start - iskanje" >}}
  {{< figure align=center src="/images/other/win10/Winsl_-_start_-_iskanje_-_registry_editor_sdpreti.jpeg" title="Start - rezultat iskanja" >}}

  Če se odpre katerokoli varnostno okno ko odpirate program ali datoteko poglejte [kaj morate narediti](#kaj-storiti-če-se-pri-odpiranju-datoteke-ali-programa-prikažejo-varnostna-obvestila "Kliknite/tapnite da skočite na odsek!") skoraj na vrhu te spletne strani!
  
{{< /collapse >}}

{{< collapse summary="**Korak 3:** Odprite registrski ključ `NewStartPanel`" openByDefault=true >}}

  Lokacija: 
  
    Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\HideDesktopIcons\NewStartPanel

  Lahko ga odprete na dva načina:
  
  1. z levo miškino tipko izberite lokacijo zgoraj, z desno miškino tipko kliknite na izbrano in nato z levo miškino tipko kliknite na tipko `Kopiraj`. 

     {{< figure align=center src="/images/Brave/Brave_sl_-_oznacen_tekst_kopiraj.jpeg" >}}

     Sedaj na vrhu okna `Windows Registry` v polju besedila lokacije ozdstranite obstoječo besedilo, z desno miškino tipko kliknite v polje in z levo miškino tipko kliknite tipko `Prilepi`, da prilepite prej kopirano lokacijo.

     {{< figure align=center src="/images/other/win10/Winsl_-_registry_editor_prilepi_lokacijo.jpeg" >}}

     Da potrdite novo lokacijo pritisnite tipko `Enter` na tipkovnici.

     {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
     {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}
  
  2. z levo miškino tipko kliknite puščice na levi strani ključev da razširite ključe, dokler ne prispete `NewStartPanel`.

     {{< figure align=center src="/images/other/win10/Win_-_registry_editor_-_expand_NewStartPanel.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Izdelajte vrednost `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` vendar če že obstaja preskočite na `Korak 5`" openByDefault=true >}}

  Naslov nove vrednosti: 
  
    {2cc5ca98-6485-489a-920e-b3e88a6ccce3}

  Če izdelate novo `Vrednost` (angleško `Value`) in druga vrednost že obstaja s enakim imenom boste prejeli obvestilo, da vrednost že obstaja. Nova vrednost bo kljub temu narejena s privzetim imenom, lahko jo kar izbrišete.

  {{< figure align=center src="/images/other/win10/Winsl_-_registry_editor_-_vrednost_ze_obstaja.jpeg" >}}

  Da izdelate novo vrednost:

  1. z levo miškino tipko označite `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}`, z desno miškino tipko kliknite na izbrano in nato z levo miškino tipko kliknite na tipko `Kopiraj`.

     {{< figure align=center src="/images/Brave/Brave_sl_-_reg_vrednost_msdih_kopiraj.jpeg" >}}

  2. Poskrbite, da se nahajate v ključu `NewStartPanel`, na desni strani okna z desno miškino tipko kliknite v praznem prostoru, pojdite preko `New` (slovensko: Nov) in z levo miškino tipko kliknite na tipko `DWORD (32-bit) Value`.

     {{< figure align=center src="/images/other/win10/Winen_-_registry_editor_-_rmb_new_dword32.jpeg" >}}

  3. Sedaj z desno tipko miške kliknite na izbrano privzeto vrednost z imenom `New Value #1` (slovensko: Nova vrednost #1) in z levo tipko miške kliknite na `Prilepi`, da prilepite prej kopirano ime vrednosti `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}`.

     {{< figure align=center src="/images/other/win10/Winsl_-_registry_editor_-_new_dword32_prilepi_ime.jpeg" >}}

     Da potrdite novo ime pritisnite tipko `Enter` na tipkovnici.

     {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
     {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** z desno miškino tipko kliknite na `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` in nato z levo miškino tipko kliknite na tipko `Modify` (slovensko: Uredite)" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winen_-_registry_editor_-_dword32_-_rmb_modify.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Pod `Value data` v polju besedila bodite prepričani, da je napisana številka `1` (`1` pomeni skrito bližnjico, `0` ali izbrisano vrednost pa prikazano bližnjico) in nato z levo miškino tipko kliknite na tipko `Ok` za potrditev spremembe" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winen_-_registry_editor_-_dword32_-_modify_-_1_-_ok.jpeg" >}}

  Za spremembo vrednosti preprosto kliknite z levo tipko miške v besedilno polje pod `Value data` (slovensko: Podatki vrednosti) (za brisanje obstoječe vsebine lahko uporabite tipko `Backspace` ali `Del` / `Delete`) in vtipkajte želeno vrednost kot na primer `1`.

{{< /collapse >}}

{{< collapse summary="**Korak 7:** Osvežite namizje Windowsa da vidite spremembo" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsl_-_namizje_-_rmb_osvezi.jpeg" >}}

{{< /collapse >}}

## Video verzija

*(26.07.2025, 18:00 / 06:00 PM, timezone: CEST / UTC+2 / GMT+2)*

{{< youtube "-mxZabjl4VA" >}}