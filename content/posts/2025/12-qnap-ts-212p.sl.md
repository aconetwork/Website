---
title: "QNAP TS-212P razdiranje, čiščenje, ..."
date: 2025-12-26T00:00:00+01:00
# publishDate: {{ .Date }}
url: /qnap-ts-212p-sl/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - kako
  - zdravje
tags: 
  - kako
  - Strojna oprema
showtoc: true  # Seznam vsebine: Skriti (false) ali prikazati (true)
draft: false  # Prikaz na javni strani: Prikaz (false) ali skriti (true)
language: "Slovenski"
---

Od prijatelja sem dobil NAS QNAP TS-212P, danes pa je na sporedu razstavljanje, čiščenje, zamenjava termalne paste in še kaj. To je počasen NAS, vendar je za osnovno omrežno deljenje datotek, FTP in podobno dovolj dober. NAS je okrajšava za Network Attached Storage (omrežno priključeno shranjevanje).

## Razstavljanje

{{< notice note >}}
  Ko razstavljate ali opravljate kakršno koli delo znotraj naprave, ne hitite, saj lahko, če niste previdni, hitro kaj poškodujete.
{{< /notice >}}

*(Kliknite na posamezen korak ali trikotnik, da skrijete ali prikažete podrobnosti (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Odstranite dva vijaka na zadnji strani" openByDefault=true >}}

   V mojem primeru sta ta vijaka manjkala, zato je bil ta del izpuščen.

   {{< figure align=center src="/images/qnap_ts-212p/back_2_screws.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Zgornji del ohišja potegnite naprej in stran" openByDefault=true >}}

   {{< figure align=center src="/images/qnap_ts-212p/top_case_remove.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Odklopite ventilator in 2 SATA konektorja ter prerežite kabelsko vezico, ki drži žice ventilatorja" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/3_connectors_side.jpeg" title="konektorji" >}}
  {{< figure align=center src="/images/qnap_ts-212p/fan_wire_zip_ties.jpeg" title="Kabelska vezica" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Odvijte vse vijake, ki držijo diskovne pogone na obeh straneh, in jih odstranite" openByDefault=true >}}

  Spodnji diskovni pogon po odvijanju potisnite naprej in ga nato odstranite.

  {{< figure align=center src="/images/qnap_ts-212p/disks_screwed_in_1.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Odvijte 4 vijake, ki držijo kletko za diske in matično ploščo v ohišju" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/for_disk_metal_case_screws_inside.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Odvijte ventilator in ga odstranite" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/fan_screws.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 7:** Odlepite kovinski trak ravno toliko, da lahko vzamete matično ploščo ven, in odstranite matično ploščo" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/metal_tape_peel_off_usb.jpeg" >}}

{{< /collapse >}}

Za odstranitev hladilnika nadaljujte z branjem spodaj.

## Zamenjava termalne paste

Za to sem uporabil papirnato brisačo, izopropilni alkohol (IPA) in če je stara pasta suha in trda, tako da papirnata brisača in IPA nista dovolj, uporabite nekaj plastičnega, da jo ostrgate stran **VENDAR NE UPORABLJAJTE KOVINE**, ker to poškoduje hladilnik!

Če je termalna pasta mehka in ne suha, verjetno je ni treba zamenjati.

*(Kliknite na posamezen korak ali trikotnik, da skrijete ali prikažete podrobnosti (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** S kleščami stisnite in potisnite ven obe plastični sponki, ki držita hladilnik" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/cooler_plastic_clip_squize.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Na hladilniku in procesorju odstranite staro termalno pasto (če je suha in trda)" openByDefault=true >}}

  Najprej nanesite na površino ali papirnato brisačo IPA in nato očistite staro termalno pasto. **NE DOTIKAJTE SE** očiščenega območja s prsti!

  {{< figure align=center src="/images/qnap_ts-212p/cooler_dry_thermal_towel_clean.jpeg" >}}

  Če je preveč suha in trda, vzemite nekaj plastičnega (na primer staro kreditno kartico) in jo najprej ostrgajte, kasneje pa očistite z IPA in brisačo.

  {{< figure align=center src="/images/qnap_ts-212p/cooler_thermal_plastic_card_remove.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Nanesite termalno pasto v velikosti graha na procesor ali hladilnik in pritrdite hladilnik nazaj na matično ploščo" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/arctic_mx-4_thermal_paste_tube.jpeg" title="Termalna pasta ARCTIC MX-4" >}}

  {{< figure align=center src="/images/qnap_ts-212p/spreading_new_thermal_paste.jpeg" title="Razmazovanje" >}}

  {{< figure align=center src="/images/qnap_ts-212p/cooler_fresh_attach_to_mb.jpeg" >}}

{{< /collapse >}}

## Kaj je naslednje?

Verjetno želite zamenjati gumbno baterijo CR2032, zamenjava pa mora biti enak model! Najbolje je preveriti njeno napetost (V) z multimetrom (nastavljenim na enosmerni tok (DC)) in poskrbeti, da je vsaj 3–3,1 V; če je nižja, jo zamenjajte z novo.

{{< figure align=center src="/images/qnap_ts-212p/cr2032_in_socket.jpeg" title="CR2032" >}}
{{< figure align=center src="/images/qnap_ts-212p/multimeeter_V_DC.jpeg" title="Multimeter DC" >}}
{{< figure align=center src="/images/qnap_ts-212p/CR2032_voltage_new.jpeg" title="Napetost nove baterije" >}}

Zdaj, ko je vse končano, jo samo sestavite nazaj v obratnem vrstnem redu do te točke. Zdaj samo priključite napajalni adapter in omrežni kabel, da vklopite in uporabite napravo. Ko vidite zeleno lučko pri `STATUS` spredaj na napravi, to pomeni, da je naprava popolnoma zagnana; ob vklopu vas obvesti prvi pisk, ko je popolnoma zagnana in pripravljena pa drugi pisk (zelena lučka statusa).

## Ponastavitev QNAP NAS

{{< notice note >}}
  Za ponastavitev, prijavo ali kar koli drugega poskrbite, da je naprava vklopljena in da je zelena lučka pri `STATUS` spredaj na napravi.
{{< /notice >}}

Obstaja več načinov za ponastavitev NAS. Ročno jo lahko izvedete zunaj na zadnji strani naprave z gumbom `RESET` ali ko ste prijavljeni v NAS iz njegovih nastavitev.

Če želite druge možnosti ponastavitve, preverite razdelek [Viri](#resources "Kliknite/potapkajte za odprtje strani!").

*(Kliknite na posamezen korak ali trikotnik, da skrijete ali prikažete podrobnosti (slike, informacije, ...))*

{{< collapse summary="**Gumb RESET** v luknjici na zadnji strani naprave" openByDefault=true >}}

  Ko je naprava vklopljena in deluje z zeleno lučko pri `STATUS` spredaj na napravi, vzemite nekaj tankega, kot je zobotrebec ali podobno, in pritisnite ter držite gumb `RESET` v luknjici za:

  - **3 sekunde za delno ponastavitev**
    
    NAS enkrat zapiska, kar pomeni uspešno ponastavitev, podatki pa ostanejo nedotaknjeni.

    Naslednje nastavitve se povrnejo na privzete:

    - **Geslo skrbnika:** Ponastavljeno na privzeto ali prvo MAC naslov. Glejte tukaj.
    - **Varnostna raven:** Nastavljena na nizko (dovoli vse povezave)
    - **Vezava storitev:** Vse storitve NAS so na voljo na vseh vmesnikih
    - **Sistemski vrata:** Nastavljena na 8080
    - **Omrežne nastavitve (TCP/IP):** Preklopljeno na DHCP, onemogočeni Jumbo Frame in VLAN, Port Trunking nastavljen na Active Backup (pri modelih z dvema LAN)

  - **10 sekund za popolno ponastavitev**

    En pisk je pri 3 sekundah in drugi pri 10 sekundah. Podatki na diskih ostanejo nedotaknjeni.
    - Vse deljene mape se izbrišejo.
    - Vse sistemske nastavitve se povrnejo na privzete.

{{< /collapse >}}

## Prijava s QFinder Pro (prenos, namestitev, zagon, iskanje)

{{< notice note >}}
  Za prijavo ali kar koli drugega poskrbite, da je naprava vklopljena in da je zelena lučka pri `STATUS` spredaj na napravi. Priključite omrežni kabel na NAS in vaš domači usmerjevalnik, da lahko do njega dostopate iz računalnikov.
{{< /notice >}}

Prenesimo, namestimo in zaženimo program.

*(Kliknite na posamezen korak ali trikotnik, da skrijete ali prikažete podrobnosti (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Odprite spletno stran za `QFinder Pro` in z levim gumbom miške kliknite na modri gumb `Download`" openByDefault=true >}}

    https://www.qnap.com/en/software/qfinder-pro
  
  Lahko ga poiščete tudi v vašem iskalniku, kot je [Google](https://www.google.com/ "Kliknite/potapkajte za odprtje strani!") in odprete rezultat.

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_site_-_download_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Pomaknite se navzdol in z levim gumbom miške kliknite na ustrezen gumb za prenos namestitve, jaz imam Windows OS, zato bomo kliknili `Download (.exe)`" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_site_-_download_page_-_dl_win_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Odprite prenose v spletnem brskalniku in z levim gumbom miške kliknite na preneseno datoteko, da jo odprete" openByDefault=true >}}

  Če se prikaže okno `User Account Control` (UAC), z levim gumbom miške kliknite na gumb `Yes`.

  {{< figure align=center src="/images/qnap_ts-212p/download_btn_brave.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_file_dl_btn_brave.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_UAC.jpeg" >}}
  

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Z levim gumbom miške kliknite na gumb `OK`" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_1.jpeg" >}}
  

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Z levim gumbom miške kliknite na gumbe `Next`, `Install` in `Finish`, da zaključite namestitev" openByDefault=true >}}

  Med namestitvijo lahko z levim gumbom miške označite ali odznačite potrditvena polja za dodatne možnosti.

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_next_btn.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_install_btn.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_finish_btn.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_6_checkbox_hover.jpeg" title="Potrditveno polje" >}}
  
{{< /collapse >}}

{{< collapse summary="**Korak 6:** Prvič program vpraša po regiji, samo z levim gumbom miške kliknite na gumb `OK`" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_region.jpeg" >}}

  Če Windows prikaže opozorila o programu, jih samo potrdite. Tudi za označevanje ali odznačevanje potrditvenih polj z levim gumbom miške kliknite nanje.

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_UAC.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_WSA.jpeg" >}}
  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_install_6_checkbox_hover.jpeg" title="Potrditveno polje" >}}
  
{{< /collapse >}}

{{< collapse summary="**Korak 7:** Če program prikaže napako, da ni najdenih naprav, z levim gumbom miške kliknite na gumb `OK`" openByDefault=true >}}

  To se lahko zgodi, če naprava ni zagnana, če je naslov IP omrežja naprave napačen, če ni povezana v isto omrežje kot vaš računalnik, ...

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_no_devices_err.jpeg" >}}
  
{{< /collapse >}}

{{< collapse summary="**Korak 8:** Z levim gumbom miške kliknite na gumb za osvežitev, da poiščete NAS napravo v omrežju" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_refresh_btn.jpeg" >}}
  
{{< /collapse >}}

{{< collapse summary="**Korak 9:** Za odprtje strani `Login` za vašo NAS napravo z desnim gumbom miške kliknite na NAS napravo v rezultatih in nato z levim gumbom miške kliknite na gumb `Login`" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/qfinder_pro_open_nas_rmb_login.jpeg" >}}
  
{{< /collapse >}}

{{< collapse summary="**Korak 10:** Z levim gumbom miške kliknite na gumb `Login`" openByDefault=true >}}

  {{< figure align=center src="/images/qnap_ts-212p/nas_login_page_-_login_btn.jpeg" >}}
  
{{< /collapse >}}

{{< collapse summary="**Korak 11:** Izpolnite poverilnice in nato z levim gumbom miške kliknite na gumb `Login`" openByDefault=true >}}

  Privzete vrednosti uporabniškega imena in gesla:

     admin

  {{< figure align=center src="/images/qnap_ts-212p/nas_login_page_-_login_page_login_btn.jpeg" >}}

  In zdaj lahko začnete konfigurirati vašo NAS napravo, uživajte :)
  
{{< /collapse >}}

## Povezave

- [QNAP](https://www.qnap.com/ "Kliknite/tapnite da odprete spletno stran!")
- [How do I reset my NAS settings?](https://www.qnap.com/en/how-to/faq/article/how-can-i-reset-my-nas "Kliknite/tapnite da odprete spletno stran!")
- [QFinder Pro](https://www.qnap.com/en/software/qfinder-pro "Kliknite/tapnite da odprete spletno stran!")

## Video verzija

*(26.12.2025, 18:00 / 06:00 PM, časovna zona: CET / UTC+1 / GMT+1)*

{{< youtube "3SL-hPF4TK0" >}}