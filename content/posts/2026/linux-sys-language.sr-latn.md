---
title: "Promena sistemskog Linux jezika"
date: 2026-09-25T18:00:00+02:00
# publishDate: 2026-09-25T15:36:39+02:00
url: /linux-sis-jezik-sr/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - Kako
tags: 
  - Kako
  - Linux
showtoc: false  # Tabela sadržaja: Sakriti (false) ili pokazati (true).
draft: false   # Prikaz na javnoj stranici: Prikaz (false) ili sakriti (true).
language: "Srpski"
---

Danas menjamo sistemski jezik operativnog sistema Linux, kako instilirati i izbrisati jezik, ažurirati nova podešavanja i više..

{{< notice tip >}}
  Ako ne znate jezika vašeg sistema samo sledite ikonama u ovom tutorijalu, isti su.
{{< /notice >}}

{{< notice warning >}}
  Kad završite sa promenama podešavanja jezika ponovno pokrenite računar, da se nova podešavanja ažuriraju u sistem kompletno! [Ponovno pokretanje računara](#ponovno-pokretanje-računara "Kliknite/tapnite, da posetita taj odeljak!")
{{< /notice >}}

## Otvaranje prozora Laguages ili Jezici i njegovih elementata

*(Kliknite na pojedinačni korak ili trougao da sakrijete ili pokažete detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** sa levim dugmetom miša kliknite na dugme `LM` menija" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_lm_menu_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** sa levim dugmetom miša kliknite na dugme `System settings` ili `Postavke sistema`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_lm_menu_-_sys_settings_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_lm_meni_-_postavke_sis_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** sa levim dugmetom miša kliknite na dugme `Languages` ili `Jezici`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_sys_settings_-_languages_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_postavke_sis_prozor_-_jezici_btn_hover.jpeg">}}

{{< /collapse >}}

Sedaj imaste odpreto okno `Language Settings` ili `Postavke jezika`.

{{< figure ilign=center src="/images/LinuxMint/en_-_language_settings_window.jpeg">}}
{{< figure ilign=center src="/images/LinuxMint/sr_-_postavke_jezika_prozor.jpeg">}}

Ako želite da promenite podešavanja jezika trenutačnog koristnika, promenite prva 3 elemenata sa več instiliranim jezicima (pogledajte uputstva ispod [Podesimo jezikovna podešavanja za trenutačnog koristnika](#podesimo-jezikovna-podešavanja-za-trenutačnog-koristnika "Kliknite/tapnite, da posetita taj odeljak!"). Ako željenog jezika nema na spisku ga prvo morate da instilirate, pogledajte uputstva ispod [Instalacija novog jezika](#instalacija-novog-jezika "Kliknite/tapnite, da posetita taj odeljak!").

Ako želite da promenite jezik celg sistema (podrazumevani sistemski jezik, ekran za prijavu, drugi profili...),, pogledajte uputstva ispod [Ažuriranje trenutačnih podešavanja za ceo sistem](#ažuriranje-trenutačnih-podešavanja-za-ceo-sistem "Kliknite/tapnite, da posetita taj odeljak!").

Za instalaciju ili brisanje željenog jezika upotrebite dugme `Install/Remove Languages...` ili `Instiliraj/ukloni jezike...`, pogledajte uputstva ispod [Instalacija novog jezika](#instalacija-novog-jezika "Kliknite/tapnite, da posetita taj odeljak!") ili [Brisanje instaliranog jezika](#brisanje-instaliranog-jezika "Kliknite/tapnite, da posetita taj odeljak!").

## Podesimo jezikovna podešavanja za trenutačnog koristnika

- **Language** ili `Jezik` Linux koristnika.
- **Region** ili `Regija` koristnika.
- **Time format** ili `Format vremena` i datuma.

{{< figure ilign=center src="/images/LinuxMint/en_-_installed_language_list_-_language_btn_hover.jpeg" title="Primer liste instaliranih jezika">}}

{{< notice tip >}}
  Ako nemate instaliranog željenog jezika pogledajte uputstva ispod [Instalacija novog jezika](#instalacija-novog-jezika "Kliknite/tapnite, da posetita taj odeljak!").
{{< /notice >}}

*(Kliknite na pojedinačni korak ili trougao da sakrijete ili pokažete detalje (slike, informacije, ...))*

{{< collapse summary="**Promena jezika koristnika:** sa levim dugmetom miša kliknite na dugme jezika - trenutačnog jezika i sa levim dugmetom miša odaberite željen jezik sa liste" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_language_settings_window_-_language_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Promenite regiju koristnika:** sa levim dugmetom miša kliknite na dugme jezika trenutačne regije i sa levim dugmetom miša odaberite željen jezik sa liste" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_language_settings_window_-_region_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Promenite format vremena i datuma koristnika:** sa levim dugmetom miša kliknite na dugme trenutačnog formata vremena i sa levim dugmetom miša odaberite željen jezik sa liste" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_language_settings_window_-_time_format_btn_hover.jpeg">}}

{{< /collapse >}}

## Ažuriranje trenutačnih podešavanja za ceo sistem

*(Kliknite na pojedinačni korak ili trougao da sakrijete ili pokažete detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** sa levim dugmetom miša kliknite na dugme `Apply System-Wide` ili `Uveljavi za celoten sistem`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_language_settings_window_-_apply_system_wide_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_postavke_jezika_prozor_-_primeni_ceo_sistem_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** u prozoru `Authentication Required` ili `Potrebno je potvrđivanje identiteta` upišite lozinku trenutačno prijavljenog koristnika i sa klikom levog dugmeta miša potvrdite `Authenticate` ili `Potvrdi identitet`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_auth_req_-_languages_-_authenticate_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_potrebna_potvrda_identiteta_-_jezici_-_potvrdi_identitet_btn_hover.jpeg">}}

{{< /collapse >}}

## Instalacija novog jezika

*(Kliknite na pojedinačni korak ili trougao da sakrijete ili pokažete detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** sa levim dugmetom miša kliknite na dugme `Install/Remove Languages...` ili `Namesti/ostrani jezike...`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_language_settings_window_-_inst_rem_langs_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sr_-_postavke_jezika_prozor_-_instaliraj_ukloni_jezike_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** u prozoru `Authentication Required` ili `Potrebno je potvrđivanje identiteta` upišite lozinku trenutačno prijavljenog koristnika i sa klikom levog dugmeta miša potvrdite sa `Authenticate` ili `Potvrdi identitet`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_auth_req_-_languages_-_authenticate_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_potrebna_potvrda_identiteta_-_jezici_-_potvrdi_identitet_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** u prozoru `Install / Remove Languages` ili `Instaliraj / ukloni jezike` i onda sa levim dugmetom miša kliknite na dugme `Add...` ili `Dodaj...`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_add_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_instaliraj_ukloni_jezike_prozor_-_dodaj_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** u prozoru `Add a new Language` ili `Dodaj nov jezik` sa levim dugmetom miša kliknite na željen jezik i onda sa levim dugmetom miša kliknite na dugme `Install` ili `Instaliraj`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/sr_-_dodaj_novi_jezik_prozor_-_german_austria_hover.jpeg" title="Primer isabranog jezika">}}
  {{< figure ilign=center src="/images/LinuxMint/en_-_inst_new_language_window_-_install_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_dodaj_novi_jezik_prozor_-_instaliraj_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** u prošlom prozoru `Install / Remove Languages` ili `Instaliraj / ukloni jezike` sa levim dugmetom miša kliknite na željen jezik i nato sa levim dugmetom miša kliknite na dugme `Install language packs` ili `Instaliraj jezičke pakete pakete`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/sr_-_instaliraj_ukloni_jezike_prozor_-_german_austria_nedostaju_paketi_hover.jpeg" title="Primer nameščenega jezika">}}
  {{< figure ilign=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_install_lang_packs_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_instaliraj_ukloni_jezike_prozor_-_instaliraj_jez_pakete_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_instaliraj_ukloni_jezike_prozor_-_instaliram_pakete_prozor.jpeg">}}

  Sada pa saćekajte, da se paketi instaliraju.

{{< /collapse >}}

{{< collapse summary="**Korak 6:** sa levim dugmetom miša kliknite na dugme `Close` ili `Zatvori`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_close_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_instaliraj_ukloni_jezike_prozor_-_zatvori_btn_hover.jpeg">}}

{{< /collapse >}}

Sada možete da promenite jezik, kao što smo pre u [Podesimo jezikovna podešavanja za trenutačnog koristnika](#podesimo-jezikovna-podešavanja-za-trenutačnog-koristnika "Kliknite/tapnite, da posetita taj odeljak!").

## Brisanje instaliranog jezika

*(Kliknite na pojedinačni korak ili trougao da sakrijete ili pokažete detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** sa levim dugmetom miša kliknite na dugme `Install/Remove Languages...` ili `Instaliraj / ukloni jezike...`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_language_settings_window_-_inst_rem_langs_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sr_-_postavke_jezika_prozor_-_instaliraj_ukloni_jezike_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** u prozoru `Authentication Required` ili `Potrebno je potvrđivanje identiteta` upišite lozinku trenutačno prijavljenog koristnika i sa klikom levog dugmeta miša potvrdite sa `Authenticate` ili `Potvrdi identitet`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_auth_req_-_languages_-_authenticate_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_potrebna_potvrda_identiteta_-_jezici_-_potvrdi_identitet_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** u novom prozoru `Install / Remove Languages` ili `Instaliraj / ukloni jezike...` sa levim dugmetom miša kliknite na željen jezik za brisanje i onda sa levim dugmetom miša kliknite na dugme `Remove` ili `Ukloni`" openByDefault=true >}}

  Napravite ovo za sve jezike, koje želite da izbrišete.

  {{< figure ilign=center src="/images/LinuxMint/sr_-_instaliraj_ukloni_jezike_-_german_austria_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_remove_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_instaliraj_ukloni_jezike_-_ukloni_btn_hover.jpeg">}}

  Ako se pojavi prozor `Aditional software has to be removed` ili `Dodatni softver mora da bude uklonjeni` sa levim dugmetom miša kliknite na dugme `Continue` ili `Nastavi`.

  {{< figure ilign=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_additional_to_remove_window_-_continue_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_instaliraj_ukloni_jezike_prozor_-_dod_softver_uklonjen_prozor_-_nastavi_btn_hover.jpeg">}}

  Sada samo sačekajte, da se paketi izbrišu/uklone.

  {{< figure ilign=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_removing_packages_window.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_instaliraj_ukloni_jezike_prozor_-_uklanjam_pakete_prozor.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** sa levim dugmetom miša kliknite na dugme `Close` ili `Zatvori`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_close_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_instaliraj_ukloni_jezike_prozor_-_zatvori_btn_hover.jpeg">}}

{{< /collapse >}}

## Ponovno pokretanje računara

*(Kliknite na pojedinačni korak ili trougao da sakrijete ili pokažete detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** sa levim dugmetom miša kliknite na dugme `LM` menija" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_lm_menu_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** sa levim dugmetom miša kliknite na crveno dugme `Shut Down` ili `Ugasi`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_lm_menu_-_shut_down_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** sa levim dugmetom miša kliknite na dugme `Restart` ili `Ponovno pokreni`" openByDefault=true >}}

  {{< figure ilign=center src="/images/LinuxMint/en_-_lm_menu_-_shut_down_window_-_restart_btn_hover.jpeg">}}
  {{< figure ilign=center src="/images/LinuxMint/sr_-_lm_meni_-_ugasi_prozor_-_ponovno_pokreni_btn_hover.jpeg">}}

{{< /collapse >}}

## Linkovi

- [Linux tutoriili na ovoj stranici](/sr-latn/tags/linux/ "kliknite/tapnite, da otvorite veb stranicu!")
- [Linux Mint](https://linuxmint.com/ "kliknite/tapnite, da otvorite veb stranicu!")
- [Izrada novog Linux koristnika na nekoliko načina + više](/linux-nov-koristnik-sr "kliknite/tapnite, da otvorite veb stranicu!")
- [Linux plejlista - YouTube](https://www.youtube.com/playlist?list=PLAqqAAF5KyKw "kliknite/tapnite, da otvorite veb stranicu!")

## Video verzija

*(27.09.2026, 18:00 / 06:00 PM, vremenska zona: CEST / UTC+2 / GMT+2)*

{{< youtube "1XjgVQt-t5I" >}}