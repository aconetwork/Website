---
title: "Sakrijte prečicu Spotlight sa Windows radne površine"
date: 2025-07-25T00:00:00+02:00
# publishDate: 2025-04-17T12:00:00+02:00
url: /mspotlight-precica-sr/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - kako
tags: 
  - Windows
  - Microsoft Spotlight
showtoc: true  # Tabela sadržaja: Sakriti (false) ili pokazati (true).
draft: false   # Prikaz na javnoj stranici: Prikaz (false) ili sakriti (true).
language: "Srpski"
---

Microsoft Spotlight je alat koji menja pozadinsku sliku vaše radne površine u operativnom sistemu Windows preuzimanjem slika sa interneta. U ovom tutorijalu če naučite, kako da sakrijete (i pokažete) prečicu Spotlajta na radnoj površini `Saznajte više o ovoj slici` ali i da zadržite pozadinske slike Spotlajta na 2 načina unutar Windows registra.

{{< figure align=center src="/images/other/win10/Winsrcyrl_-_radna_povrsina_-_saznajte_vise_o_ovoj_slici.jpeg" >}} {{< figure align=center src="/images/other/win10/Winsr_-_radna_povrsina_saznajte_vise_o_slici.jpeg" >}} {{< figure align=center src="/images/other/win10/Winen_-_desktop_-_learn_about_this_pic.jpeg" >}}

## Šta uraditi ako se pojave bezbednosna obaveštenja prilikom otvaranja datoteke ili programa?

Ako se kod otvaranja neke datoteke ili programa pojavi `Bezbednosno upozorenje`, `Kontrola korisničkog naloga` ili bilo koji drugi bezbednosni prozor, kliknite levim dugmetom miša na dugme `Da`, `Pokreni` ili bilo koje drugo dugme da potvrdite dozvoljavanje otvaranje.

{{< figure align=center src="/images/other/win10/Winsr_-_msdih_reg_otvoriti_bezbednostno_upozorenje.jpeg" title="Bezbednosno upozorenje za otvaranje datoteke" >}} {{< figure align=center src="/images/other/win10/Winsr_-_UAC_-_registry_editor_-_da.jpeg" title="Kontrola korisničkog naloga za otvaranje programa" >}}

## 1. METODA (lakša): Sa pripremljenim fajlovima registra

Kod ove metode jednostavno preuzimete datoteku registra i upotrebite je. Ja sam kreirao datoteke, ali ako im ne verujete, možete koristiti ručni način u [2. Metoda](#2-metoda-teža-ručno-uređivanje-u-windows-registru "Kliknite/tapnite, da skoknete na 2. metodu!").

*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Presnimajte potrebnu datoteku registra" openByDefault=true >}}

  Da sakrijete prečicu na radnoj površini upotrebite [spotlight-desktop-icon-hide.reg](/scripts/spotlight-desktop-icon-hide.reg "Kliknite/tapnite da presnimate datoteku!") i da pokažete upotrebite [spotlight-desktop-icon-show.reg](/scripts/spotlight-desktop-icon-show.reg "Kliknite/tapnite da presnimate datoteku!").

  1. Da je presnimate, kliknite desnim dugmetom miša na vezu datoteke, a zatim kliknite levim dugmetom miša `Spremi vezu kao...`.

     {{< figure align=center src="/images/Brave/Brave_hr_-_spremi_vezu_kao.jpeg" >}}

  2. Otvorite željenu fasciklu u koju želite da je sačuvate i kliknite levim dugmetom miša na dugme `Sačuvaj`.

     {{< figure align=center src="/images/Brave/Brave_hr_-_spremi_prozor_-_sacuvaj_dugme.jpeg" >}}

  3. Ako vas veb pregledač pita ako želite da zadržite presnimanu datoteku, kliknite levim dugmetom miša na dugme `Zadrži` ili kako vaš veb pregledač pokaže. Ja sam snimao na [Brave](https://brave.com/ "Kliknite/tapnite, da otvorite veb sajt!").

     {{< figure align=center src="/images/Brave/Brave_hr_-_spremi_fajl_-_zadrzi_dugme.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Otvorite fasciklu u koju ste preuzeli datoteku i otvorite je sa klikom levog dugmeta miša" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winen_-_desktop_-_file_msdih_reg_open.jpeg" >}}

  Ako se pojavi bilo koji bezbednosni prozor, proverite [ovde](#šta-uraditi-ako-se-pojave-bezbednosna-obaveštenja-prilikom-otvaranja-datoteke-ili-programa "Kliknite/tapnite, da skoknete na razdelak!") na vrh (skoro) ove veb stranice!

{{< /collapse >}}

{{< collapse summary="**Korak 3:** U prozoru obaveštenja `Registry Editor` kliknite levim dugmetom miša na dugme `Da`, da unesete u registar" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsr_-_fajl_msdih_reg_potvrditi_-_da.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Kada dobijete obaveštenje, da je datoteka registra uspešno uvezena, kliknite levim dugmetom miša na dugme `U redu`, da je zatvorite" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsr_-_registry_editor_msdih_-_success_-_u_redu.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Kliknite desnim dugmetom miša na radnu površinu Windows-a, a zatim levim dugmetom miša kliknite na dugme Osveži da vidite promenu" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsr_-_radna_povrsina_-_rmb_osvezi.jpeg" >}}

{{< /collapse >}}

## 2. METODA (teža): Ručno uređivanje u Windows registru

Da ovo uradite ispravno, uradite sve **ISTO** kao ja inače možete oštetiti svoj Windows i/ili njegov sadržaj ili u najboljem slučaju neće biti promena u Windows-u ili bilo gde drugde! Ako niste sigurni, uradite lakši način u [1. METODA](#1-metoda-lakša-sa-pripremljenim-fajlovima-registra "Kliknite/tapnite da skočite na 1. metodu!").

*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Sa levim dugmetom miša kliknite na dugme `Start` / `Početak`" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsr_-_start_btn_pocetak.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Sa tastaturom počnite da pišete `Registry Editor` i sa levim dugmetom miša kliknite na rezultat `Registry Editor`" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsr_-_start_-_trazenje_registry_editor.jpeg" title="Start - traženje" >}} {{< figure align=center src="/images/other/win10/Winsr_-_start_-_trazenje_-_registry_editor_otvoriti.jpeg" title="Start - rezultat traženja" >}}

  Ako se pojavi bilo koji bezbednosni prozor, proverite [ovde](#šta-uraditi-ako-se-pojave-bezbednosna-obaveštenja-prilikom-otvaranja-datoteke-ili-programa "Kliknite/tapnite, da skoknete na razdelak!") skoro na vrhu ove veb stranice!
  
{{< /collapse >}}

{{< collapse summary="**Korak 3:** Uđite u ključ `NewStartPanel`" openByDefault=true >}}

  Lokacija: 
  
    Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\HideDesktopIcons\NewStartPanel

  Može da ga otvorite na 2 načina:
  
  1. Levim dugmetom miša označite put lokacije iznad, kliknite desnim dugmetom miša na izabrani tekst a zatim levim dugmetom miša kliknite na dugme `Kopiraj`. 

     {{< figure align=center src="/images/Brave/Brave_hr_-_oznacen_tekst_reg_kopiraj.jpeg" >}}

     Sada na vrhu prozora `Windows Registry` u polju za tekst uklonite postojeći tekst, kliknite desnim dugmetom miša u polje i sa levim dugmetom miša kliknite na dugme `Nalepi`, da nalepite pre kopiran tekst.

     {{< figure align=center src="/images/other/win10/Winsr_-_registry_editor_lokacija_nalepi.jpeg" >}}

     Da potvrdite novu lokaciju kliknite dugme `Enter` na tastaturi.

     {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}} 
     {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}
  
  2. Sa levim dugmetom miša kliknite strelice sa leve strane ključeva, dok ne otvorite `NewStartPanel`.

     {{< figure align=center src="/images/other/win10/Win_-_registry_editor_-_expand_NewStartPanel.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Napravite vrednost `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` ali ako več postoji preskočite ovaj korak i idite na `Korak 5`" openByDefault=true >}}

  Ime nove vrednosti: 
  
    {2cc5ca98-6485-489a-920e-b3e88a6ccce3}

  Ako želite da kreirate novu `Vrednost` (engleski `Value`) a ako postoji več vrednost sa istim imenom, dobičete poruku o grešci. Nova vrednost je i dalje kreirana sa podrazumevanim imenom, možete je obrisati.

  {{< figure align=center src="/images/other/win10/Winen_-_registry_editor_-_value_name_exists_err.jpeg" >}}

  Da napravite novu vrednost:

  1. Sa levim dugmetom miša označite `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}`, sa desnim dugmetom mišta kliknite na odabran tekst i onda levim dugmetom miša kliknite na dugme `Kopiraj`.

     {{< figure align=center src="/images/Brave/Brave_hr_-_reg_value_msdih_kopiraj.jpeg" >}}

  2. Uverite se da ste unutar `NewStartPanel` i na desnoj strani prozora kliknite desnim tasterom miša na prazno područje, idite preko `New` i sa levim dugmetom miša kliknite `DWORD (32-bit) Value`.

     {{< figure align=center src="/images/other/win10/Winen_-_registry_editor_-_rmb_new_dword32.jpeg" >}}

  3. Sada kliknite desnim dumetom miša na izabrano ime podrazumevane vrednosti `New Value #1` (srpski: Nova vrednost #1), i sa levim dugmetom miša kliknite na dugme `Nalepi` da nalepite pre kopiran tekst `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}`.

     {{< figure align=center src="/images/other/win10/Winsr_-_registry_editor_-_new_dword32_nalepi_dugme.jpeg" >}}

     Da potvrdite novo ime kliknite dugme `Enter` na tastaturi.

     {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
     {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Sa desnim dugmetom miša kliknite na `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` i onda sa levim dugmetom miša kliknete na `Modify` (srpski: Uredi)" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winen_-_registry_editor_-_dword32_-_rmb_modify.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Ispod `Value data` u tekstualnom polju uverite se, da jeste `1` (`1` je za sakrivenu prečicu, `0` ili izbrisana vrednost je za pokazanu prečicu) i sa levim dugmetom miša kliknite na dugme `Ok` da potvrdite promenu" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winen_-_registry_editor_-_dword32_-_modify_-_1_-_ok.jpeg" >}}

  Da promenite vrednost sa levim dumetom miša kliknite u polje za tekst ispod `Value data` (možete da upotrebite dugmeta tastature `Backspace` ili `Del` / `Delete` da izbrišete postoječi sadržaj) i sa tastaturom upišite šta želite, naprimer `1`.

{{< /collapse >}}

{{< collapse summary="**Korak 7:** Osvežite Windows radnu površinu, da vidite promene" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Winsr_-_radna_povrsina_-_rmb_osvezi.jpeg" >}}

{{< /collapse >}}

## Video verzija

*(27.07.2025, 18:00 / 06:00 PM, timezone: CEST / UTC+2 / GMT+2)*

{{< youtube "r1BVxVWCJOs" >}}