---
title: "Sprememba sistemskega Linux jezika"
date: 2026-09-25T18:00:00+02:00
# publishDate: 2026-09-25T15:36:26+02:00
url: /linux-sis-jezik-sl/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - Kako
tags: 
  - Kako
  - Linux
showtoc: false  # Seznam vsebine: Skriti (false) ali prikazati (true)
draft: false  # Prikaz na javni strani: Prikaz (false) ali skriti (true)
language: "Slovenski"
---

Danes bomo spremenili sistemski jezik operacijskega sistema Linux ter si ogledali, kako namestiti ter odstraniti jezik, uveljaviti nove nastavitve in še več.

{{< notice tip >}}
  Če ne poznate jezika vašega sistema, preprosto sledite ikonam v tem vodiču, so enaki.
{{< /notice >}}

{{< notice warning >}}
  Ko končate s spreminjanjem jezikov, ponovno zaženite računalnik, da se nove nastavitve v celoti uveljavijo! [Ponoven zagon računalnika](#ponoven-zagon-racunalnika "Kliknite/tapnite da skočite na ta oddelek!").
{{< /notice >}}

## Dostop do okna Laguages oziroma Jeziki in njegovih elementov

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** z levo miškino tipko kliknite na tipko `LM` menija" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** z levo miškino tipko kliknite na tipko `System settings` oziroma `Sistemske nastavitve`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_sys_settings_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_lm_meni_-_sis_nastavitve_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** z levo miškino tipko kliknite na tipko `Languages` oziroma `Jeziki`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_sys_settings_-_languages_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_sis_nastavitve_-_jeziki_btn_hover.jpeg">}}

{{< /collapse >}}

Sedaj imaste odpreto okno `Language Settings` oziroma `Jezikovne nastavitve`.

{{< figure align=center src="/images/LinuxMint/en_-_language_settings_window.jpeg">}}
{{< figure align=center src="/images/LinuxMint/sl_-_jezikovne_nastavitve_okno.jpeg">}}

Če želite spremeniti jezikovne nastavitve trenutnega uporabnila, prilagodite prve tri elemente glede na že nameščene jezike (poglejte spodnja navodila [Nastavite nove jezične nastavitve trenutnega uporabnika](#nastavite-nove-jezične-nastavitve-trenutnega-uporabnika "Kliknite/tapnite da skočite na ta oddelek!")), če želenega jezika ni na seznamu, ga morate najprej namestiti, poglejte spodnja navodila za [Namestitev novega jezika](#namestitev-novega-jezika "Kliknite/tapnite da skočite na ta oddelek!").

Če želite spremeniti jezik celotnega sistema (privzete sistemske nastavitve, prijavno okno, drugi profili ...), poglejte spodnja navodila [Nastavite trenutne jezikovne nastavitve uporabnika za cel sistem](#nastavite-trenutne-jezikovne-nastavitve-uporabnika-za-cel-sistem "Kliknite/tapnite da skočite na ta oddelek!").

Za namestitev ali odstranitev jezika uporabite tipko `Install/Remove Languages...` oziroma `Namesti/ostrani jezike...`, poglejte spodnja navodila [Namestitev novega jezika](#namestitev-novega-jezika "Kliknite/tapnite da skočite na ta oddelek!") ali [Odstranitev obstoječega jezika](#odstranitev-obstoječega-jezika "Kliknite/tapnite da skočite na ta oddelek!").

## Nastavite nove jezične nastavitve trenutnega uporabnika

- **Language** oziroma `Jezik` Linux uporabnika.
- **Region** oziroma `Regija` uporabnika.
- **Time format** oziroma `Oblika zapisa časa` in datuma.

{{< figure align=center src="/images/LinuxMint/en_-_installed_language_list_-_language_btn_hover.jpeg" title="Primer seznama nameščenih jezikov">}}

{{< notice tip >}}
  Če nimate nameščenega željenega jezika poglejte spodnja navodila [Namestitev novega jezika](#namestitev-novega-jezika "Kliknite/tapnite da skočite na ta oddelek!").
{{< /notice >}}

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Sprememba jezika uporabnika:** z levo miškino tipko kliknite na tipko jezika-trenutnega jezika in z levo miškino tipko izberite željen jezik s seznama" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_language_settings_window_-_language_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Spremenite regijo uporabnika:** z levo miškino tipko kliknite na tipko jezika trenutne regije in z levo miškino tipko izberite željen jezik s seznama" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_language_settings_window_-_region_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Spremenite format časa in datuma uporabnika:** z levo miškino tipko kliknite na tipko trenutnega formata časa in z levo miškino tipko izberite željen jezik s seznama" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_language_settings_window_-_time_format_btn_hover.jpeg">}}

{{< /collapse >}}

## Nastavitev trenutnih jezikovnih nastavitev uporabnika za cel sistem

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** z levo miškino tipko kliknite na tipko `Apply System-Wide` oziroma `Uveljavi za celoten sistem`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_language_settings_window_-_apply_system_wide_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_jezikovne_nastavitve_okno_-_uveljavi_cel_sistem_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** v oknu `Authentication Required` oziroma `Zahtevana je overitev`, vpišite geslo trenutno prijavljenega uporabnika in z klikom leve miškine tipke potrdite `Authenticate` oziroma `Overi`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_auth_req_-_languages_-_authenticate_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_overovitev_zahtevana_-_jeziki_-_overi_btn_hover.jpeg">}}

{{< /collapse >}}

## Namestitev novega jezika

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** z levo miškino tipko kliknite na tipko `Install/Remove Languages...` oziroma `Namesti/ostrani jezike...`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_language_settings_window_-_inst_rem_langs_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_jezikovne_nastavitve_okno_-_namesti_odstr_jezike_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** v oknu `Authentication Required` oziroma `Zahtevana je overitev`, vpišite geslo trenutno prijavljenega uporabnika in z klikom leve miškine tipke potrdite `Authenticate` oziroma `Overi`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_auth_req_-_languages_-_authenticate_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_overovitev_zahtevana_-_jeziki_-_overi_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** V oknu `Install / Remove Languages` oziroma `Namesti / odstrani jezike` in nato z levo miškino tipko kliknite na tipko `Add...` oziroma `Dodaj...`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_add_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_namesti_odstrani_jezike_okno_-_dodaj_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** V oknu `Add a new Language` oziroma `Dodaj nov jezik` z levo miškino tipko kliknite na željen jezik in nato z levo miškino tipko kliknite na tipko `Install` oziroma `Namesti`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/sl_-_namesti_nov_jezik_okno_-_finish_finland_hover.jpeg" title="Primer izbranega jezika">}}
  {{< figure align=center src="/images/LinuxMint/en_-_inst_new_language_window_-_install_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_namesti_nov_jezik_okno_-_namesti_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** v prejšnjem oknu `Install / Remove Languages` z levo miškino tipko kliknite na željen jezik in nato z levo miškino tipko kliknite na tipko `Install language packs` oziroma `Namesti jezikovne pakete`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/sl_-_namesti_odstrani_jezike_okno_-_finish_finland_manjkajo_paketi_hover.jpeg" title="Primer nameščenega jezika">}}
  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_install_lang_packs_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_namesti_odstrani_jezike_okno_-_namesti_jez_pakete_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_namesti_odstrani_jezike_okno_-_namescanje_paketov_okno.jpeg">}}

  Sedaj pa počakajte, da se vsi paketi namestijo.

{{< /collapse >}}

{{< collapse summary="**Korak 6:** z levo miškino tipko kliknite na tipko `Close` oziroma `Zapri`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_close_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_namesti_odstrani_jezike_okno_-_zapri_btn_hover.jpeg">}}

{{< /collapse >}}

Sedaj lahko spremenite svoj jezik, kot smo prej v [Nastavite nove jezične nastavitve trenutnega uporabnika](#nastavite-nove-jezične-nastavitve-trenutnega-uporabnika "Kliknite/tapnite da skočite na ta oddelek!").

## Odstranitev obstoječega jezika

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** z levo miškino tipko kliknite na tipko `Install/Remove Languages...` oziroma `Namesti/odstrani jezike...`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_language_settings_window_-_inst_rem_langs_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_jezikovne_nastavitve_okno_-_namesti_odstr_jezike_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** V oknu `Authentication Required` oziroma `Zahtevana je overitev` vpišite geslo trenutno prijavljenega uporabnika in potrdite z levo miškino tipko na tipko `Authenticate` oziroma `Overi`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_auth_req_-_languages_-_authenticate_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_overovitev_zahtevana_-_jeziki_-_overi_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** V novem oknu `Install / Remove Languages` oziroma `Namesti/odstrani jezike...` z levo miškino tipko kliknite na željen jezik za odstranitev in nato z levo miškino tipko kliknite na tipko `Remove` oziroma `Odstrani`" openByDefault=true >}}

  Naredite tole za vse jezike, ki želite odstraniti.

  {{< figure align=center src="/images/LinuxMint/sl_-_namesti_nov_jezik_okno_-_finish_finland_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_remove_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_namesti_nov_jezik_okno_-_odstrani_btn_hover.jpeg">}}

  Če se pojavi obvestilo `Aditional software has to be removed` oziroma `Dodatno programsko opremo je treba odstraniti` z levo miškino tipko kliknite na tipko `Continue` oziroma `Nadaljuj`.

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_additional_to_remove_window_-_continue_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_namesti_odstrani_jezike_okno_-_dod_prog_opremo_odstr_okno_-_nadaljuj_btn_hover.jpeg">}}

  Sedaj samo počakajte, dokler se paketi odstranijo.

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_removing_packages_window.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_namesti_odstrani_jezike_okno_-_odstranjevanje_paketov.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** z levo miškino tipko kliknite na tipko `Close` oziroma `Zapri`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_inst_rem_languages_window_-_close_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_namesti_odstrani_jezike_okno_-_zapri_btn_hover.jpeg">}}

{{< /collapse >}}

## Ponoven zagon računalnika

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** z levo miškino tipko kliknite na tipko `LM` menija" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** z levo miškino tipko kliknite na rdečo tipko `Shut Down` oziroma `Izklop računalnika`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_shut_down_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** z levo miškino tipko kliknite na tipko `Restart` oziroma `Ponovno zaženi`" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_shut_down_window_-_restart_btn_hover.jpeg">}}
  {{< figure align=center src="/images/LinuxMint/sl_-_lm_meni_-_izklop_racunalnika_okno_-_ponovno_zazeni_btn_hover.jpeg">}}

{{< /collapse >}}

## Povezave

- [Linux tutoriali na tej strani](/sl/tags/linux/ "kliknite/tapnite, da odprete spletno stran!")
- [Linux Mint](https://linuxmint.com/ "kliknite/tapnite, da odprete spletno stran!")
- [Izdelati novega Linux uporabnika v nekaj načinov + več](/linux-nov-uporabnik-sl "kliknite/tapnite, da odprete spletno stran!")
- [Linux predvajalni seznam - YouTube](https://www.youtube.com/playlist?list=PLAqqAAF5KyKw "kliknite/tapnite, da odprete spletno stran!")

## Video verzija

*(26.09.2026, 18:00 / 06:00 PM, časovni pas: CEST / UTC+2 / GMT+2)*

{{< youtube "MwRkly5BZWg" >}}