---
title: "QNAP TS-212P raztvaranje, čiščenje, ..."
date: 2025-12-26T00:00:00+01:00
# publishDate: 2025-12-26T14:52:39+01:00
url: /qnap-ts-212p-sr/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - kako
tags: 
  - kako
  - hardver
showtoc: true  # Tabela sadržaja: Sakriti (false) ili pokazati (true).
draft: false   # Prikaz na javnoj stranici: Prikaz (false) ili sakriti (true).
language: "Srpski"
---

Dobio sam NAS QNAP TS-212P od prijatelja, a danas je na redu rastavljanje, čišćenje, zamena termalne paste i još ponešto. Ovo je spor NAS, ali za osnovno deljenje fajlova preko mreže, FTP i slično je sasvim dovoljan. NAS je skraćenica za Network Attached Storage.

## Rastavljanje

{{< notice note >}}
  Kada rastavljate ili radite bilo šta unutar uređaja, ne žurite jer ako niste pažljivi možete brzo nešto oštetiti.
{{< /notice >}}

*(Kliknite na pojedinačni korak ili trougao da sakrijete ili prikažete detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Skinite dva šrafa sa zadnje strane" openByDefault=true >}}

   U mom slučaju ti šrafovi su nedostajali pa je ovaj deo preskočen.

   {{< figure align=center src="/images/qnap_ts-212p/back_2_screws.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Gornji deo kućišta povucite napred i u stranu" openByDefault=true >}}

   {{< figure align=center src="/images/qnap_ts-212p/top_case_remove.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Isključite ventilator i 2 SATA konektora i prerežite zip-vezicu koja drži žice ventilatora" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/3_connectors_side.jpeg" title="konektori" >}}
  {{< figure align=center src="/images/qnap_ts-212p/fan_wire_zip_ties.jpeg" title="Zip-vezica" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Odvijte sve šrafove koji drže diskove sa obe strane i izvadite ih" openByDefault=true >}}

  Donji disk, kada se odvrnu šrafovi, pomerite napred pa ga onda izvadite.

  {{< figure align=center src="/images/qnap_ts-212p/disks_screwed_in_1.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Odvijte 4 šrafa koji drže kavez za diskove i matičnu ploču u kućištu" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/for_disk_metal_case_screws_inside.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Odvijte ventilator i izvadite ga" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/fan_screws.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 7:** Odlepite metalnu traku taman toliko da se matična ploča može izvaditi i izvadite matičnu ploču" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/metal_tape_peel_off_usb.jpeg" >}}

{{< /collapse >}}

Da biste skinuli hladnjak, nastavite čitanje ispod.

## Zamena termalne paste

Za ovo sam koristio papirni ubrus, izopropil alkohol (IPA) i ako je stara pasta suva i tvrda pa papirni ubrus i IPA nisu dovoljni, koristite nešto plastično da je ostrugate **ALI NE KORISTITE METAL** jer to oštećuje hladnjak!

Ako je termalna pasta mekana i nije suva, verovatno je ne treba menjati.

*(Kliknite na pojedinačni korak ili trougao da sakrijete ili prikažete detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Kleštima stisnite i izgurajte obe plastične kopče koje drže hladnjak" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/cooler_plastic_clip_squize.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Na hladnjaku i procesoru uklonite staru termalnu pastu (ako je suva i tvrda)" openByDefault=true >}}

  Prvo stavite IPA na površinu ili papirni ubrus pa onda očistite staru termalnu pastu. **NE DIRAJTE** očišćeno područje prstima!

  {{< figure align=center src="/images/qnap_ts-212p/cooler_dry_thermal_towel_clean.jpeg" >}}

  Ako je previše suva i tvrda, uzmite nešto plastično (npr. staru kreditnu karticu) i prvo je ostrugajte, a kasnije očistite IPA-om i ubrusom.

  {{< figure align=center src="/images/qnap_ts-212p/cooler_thermal_plastic_card_remove.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Stavite termalnu pastu veličine graška na procesor ili hladnjak i vratite hladnjak na matičnu ploču" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/arctic_mx-4_thermal_paste_tube.jpeg" title="ARCTIC MX-4 termalna pasta" >}}

  {{< figure align=center src="/images/qnap_ts-212p/spreading_new_thermal_paste.jpeg" title="Razmazivanje" >}}

  {{< figure align=center src="/images/qnap_ts-212p/cooler_fresh_attach_to_mb.jpeg" >}}

{{< /collapse >}}

## Šta je sledeće?

Verovatno želite da zamenite bateriju tipa CR2032 i zamena mora biti isti model! Najbolji način je da proverite njen napon (V) multimetrom (podešenim na jednosmernu struju (DC)) i uverite se da je najmanje 3–3,1 V; ako je niži, zamenite je novom.

{{< figure align=center src="/images/qnap_ts-212p/cr2032_in_socket.jpeg" title="CR2032" >}}
{{< figure align=center src="/images/qnap_ts-212p/multimeeter_V_DC.jpeg" title="Multimetar DC" >}}
{{< figure align=center src="/images/qnap_ts-212p/CR2032_voltage_new.jpeg" title="Napon nove baterije" >}}

Sada kada je sve gotovo, samo vratite sve nazad u obrnutom redosledu do ove tačke. Sada samo priključite napajanje i mrežni kabl da uključite i koristite uređaj. Kada vidite zeleno svetlo pored `STATUS` na prednjoj strani uređaja, to znači da je uređaj potpuno pokrenut; obavestiće vas prvi bip kada uključite uređaj, a drugi bip kada je potpuno pokrenut i spreman (zeleno svetlo statusa).

## Resetovanje QNAP NAS-a

{{< notice note >}}
  Za resetovanje, logovanje ili bilo šta drugo, uverite se da je uređaj uključen i da je zeleno svetlo pored `STATUS` na prednjoj strani uređaja.
{{< /notice >}}

Postoji nekoliko načina da resetujete NAS. Možete to uraditi ručno spolja na zadnjoj strani uređaja dugmetom `RESET` ili kada ste ulogovani u NAS iz njegovih podešavanja.

Ako želite druge opcije resetovanja, proverite odeljak [Resursi](#resources "Kliknite/dodirnite da otvorite sajt!").

*(Kliknite na pojedinačni korak ili trougao da sakrijete ili prikažete detalje (slike, informacije, ...))*

{{< collapse summary="**RESET dugme** u rupi na zadnjoj strani uređaja" openByDefault=true >}}

  Kada je uređaj uključen i radi sa zelenim svetlom pored `STATUS` na prednjoj strani, uzmite nešto tanko poput čačkalice ili slično i pritisnite i držite `RESET` dugme u rupi:

  - **3 sekunde za delimično resetovanje**
    
    NAS jednom bipne da označi uspešno resetovanje, a podaci ostaju netaknuti.

    Sledeća podešavanja se vraćaju na podrazumevana:

    - **Lozinka administratora:** Resetovana na podrazumevanu ili prvi MAC adres. Pogledajte ovde.
    - **Nivo bezbednosti:** Postavljen na Nizak (dozvoljava sve konekcije)
    - **Povezivanje servisa:** Svi NAS servisi dostupni na svim interfejsima
    - **Sistemski port:** Postavljen na 8080
    - **Mrežna (TCP/IP) podešavanja:** Prebačeno na DHCP, onemogućeni Jumbo Frame i VLAN, Port Trunking postavljen na Active Backup (kod modela sa dva LAN-a)

  - **10 sekundi za potpuno resetovanje**

    Jedan bip je na 3 sekunde, a drugi na 10 sekundi. Podaci na diskovima ostaju netaknuti.
    - Svi deljeni folderi se brišu.
    - Sva sistemska podešavanja se vraćaju na podrazumevana.

{{< /collapse >}}

## Logovanje pomoću QFinder Pro (preuzimanje, instalacija, pokretanje, skeniranje)

{{< notice note >}}
  Za logovanje ili bilo šta drugo, uverite se da je uređaj uključen i da je zeleno svetlo pored `STATUS` na prednjoj strani uređaja. Povežite mrežni kabl na NAS i vaš kućni ruter da biste mu pristupili sa računara.
{{< /notice >}}

Hajde da preuzmemo, instaliramo i pokrenemo program.

*(Kliknite na pojedinačni korak ili trougao da sakrijete ili prikažete detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Otvorite veb stranicu za `QFinder Pro` i levim tasterom miša kliknite na plavo dugme `Download`" openByDefault=true >}}

    https://www.qnap.com/en/software/qfinder-pro
  
  Možete ga potražiti i u vašem pretraživaču poput [Google](https://www.google.com/ "Kliknite/dodirnite da otvorite sajt!") i otvoriti rezultat.

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_site_-_download_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Skrolujte nadole i levim tasterom miša kliknite na odgovarajuće dugme za preuzimanje instalacije; ja imam Windows OS pa ćemo kliknuti `Download (.exe)`" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_site_-_download_page_-_dl_win_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Otvorite preuzimanja u veb pregledaču i levim tasterom miša kliknite na preuzetu datoteku da je otvorite" openByDefault=true >}}

  Ako se pojavi prozor `User Account Control` (UAC), levim tasterom miša kliknite na dugme `Yes`.

  {{< figure align=center src="/images/qnap_ts-212p/download_btn_brave.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_file_dl_btn_brave.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_UAC.jpeg" >}}
  

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Levim tasterom miša kliknite na dugme `OK`" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_1.jpeg" >}}
  

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Levim tasterom miša kliknite na dugmad `Next`, `Install` i `Finish` da završite instalaciju" openByDefault=true >}}

  Tokom instalacije levim klikom možete označiti ili odznačiti kućice za dodatne opcije.

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_next_btn.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_install_btn.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_finish_btn.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_6_checkbox_hover.jpeg" title="Kućica za označavanje" >}}
  
{{< /collapse >}}

{{< collapse summary="**Korak 6:** Prvi put program pita za region, samo levim tasterom miša kliknite na dugme `OK`" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_region.jpeg" >}}

  Ako Windows prikaže upozorenja o programu, samo ih potvrdite. Takođe, za označavanje ili odznačavanje kućica levim tasterom miša kliknite na njih.

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_UAC.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_WSA.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_6_checkbox_hover.jpeg" title="Kućica za označavanje" >}}
  
{{< /collapse >}}

{{< collapse summary="**Korak 7:** Ako program prikaže grešku da nema pronađenih uređaja, levim tasterom miša kliknite na dugme `OK`" openByDefault=true >}}

  Ovo može da se desi ako uređaj nije pokrenut, ako je IP adresa mreže uređaja pogrešna, ako nije povezan na istu mrežu kao vaš računar, ...

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_no_devices_err.jpeg" >}}
  
{{< /collapse >}}

{{< collapse summary="**Korak 8:** Levim tasterom miša kliknite na dugme za osvežavanje da skenirate mrežu za NAS uređaj" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_refresh_btn.jpeg" >}}
  
{{< /collapse >}}

{{< collapse summary="**Korak 9:** Da otvorite `Login` stranicu za vaš NAS uređaj, desnim tasterom miša kliknite na NAS u rezultatima pa onda levim tasterom miša kliknite na dugme `Login`" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_nas_rmb_login.jpeg" >}}
  
{{< /collapse >}}

{{< collapse summary="**Korak 10:** Levim tasterom miša kliknite na dugme `Login`" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/nas_login_page_-_login_btn.jpeg" >}}
  
{{< /collapse >}}

{{< collapse summary="**Korak 11:** Popunite kredencijale pa onda levim tasterom miša kliknite na dugme `Login`" openByDefault=true >}}

  Podrazumevane vrednosti korisničkog imena i lozinke:

     admin

  {{< figure align=center src="/images/qnap_ts-212p/nas_login_page_-_login_page_login_btn.jpeg" >}}

  I sada možete početi da konfigurišete vaš NAS uređaj, uživajte :)
  
{{< /collapse >}}

## Resursi
- [QNAP](https://www.qnap.com/ "Kliknite/dodirnite da otvorite sajt!")
- [How do I reset my NAS settings?](https://www.qnap.com/en/how-to/faq/article/how-can-i-reset-my-nas "Kliknite/dodirnite da otvorite sajt!")
- [QFinder Pro](https://www.qnap.com/en/software/qfinder-pro "Kliknite/dodirnite da otvorite sajt!")

## Video verzija
*(26.12.2025, 18:00 / 06:00 PM, vremenska zona: CET / UTC+1 / GMT+1)*

{{< youtube "3SL-hPF4TK0" >}}