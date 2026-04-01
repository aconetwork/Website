---
title: "Onemogučite novu bočni panel/traku u Mozilla Firefox"
date: 2026-03-31T14:26:55+02:00
# publishDate: 2026-03-31T14:26:55+02:00
url: /firefox-onemoguci-nbtraku-sr/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - Kako
tags: 
  - Kako
  - Windows
  - Linux
  - Mozilla Firefox
showtoc: false  # Tabela sadržaja: Sakriti (false) ili pokazati (true).
draft: false   # Prikaz na javnoj stranici: Prikaz (false) ili sakriti (true).
language: "Srpski"
---

Nova bočna traka u Firefox-u je dosadna; stalno se sama pojavljuje, pa je hajde da je onemogućimo i zamenimo bočnom trakom sa obeleživačima ili istorijom, u zavisnosti od podešavanja pregledača.

{{< figure align=center src="/images/Mozilla-Firefox/mfirefox_new_sidebar_and_button_-_button.en.jpeg">}}

{{< notice tip >}}
  Pre nego što počnete, obavezno otvorite Mozilla Firefox veb pregledač!
{{< /notice >}}

*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Korak levim dugmetom miša kliknite unutar URL polja u Mozilla Firefox-u, otkucajte `about:config` i zatim pritisnite dugme Enter na tastaturi" openByDefault=true >}}

  Ako već postoji neki tekst u polju, uklonite ga ili ga označite, pa zatim počnite da kucate adresu:

    about:config

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_url_-_about_config.jpeg">}}

  {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" title="Levo dugme Enter">}}
  {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" title="Desno dugme Enter">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Ako se pojavi upozorenje `Nastavi oprezno` sa levim dugmetom miša kliknite na dugme `Prihvati rizik i nastavi`" openByDefault=true >}}
  
  Ovo upozorenje služi ako zaista želite da uđete u napredna podešavanja pregledača. Ako tačno pratite ovaj vodič nećete imati nikakvih problema.

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_about_config_-_dugme_prihvati.sr.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Levim dugmetom miša kliknite unutar polja za pretragu i ukucajte `sidebar.rev` da vidite rezultat `sidebar.revamp` ispod" openByDefault=true >}}

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_about_config_-_sidebar.revamp_-_true.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Korak levim dugmetom miša kliknite na dugme `Uključi/izključi` na kraju reda `sidebar.revamp` da biste uključili ili isključili novu bočnu traku" openByDefault=true >}}

  `true` znači uključeno, a `false` znači isključeno za novu bočnu traku.

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_about_config_-_sidebar.revamp_-_true_-_dugme_ukljuci_izkljuci.sr.jpeg" title="true">}}
  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_about_config_-_sidebar.revamp_-_false_-_button_Toggle.en.jpeg" title="false">}}

{{< /collapse >}}

## Video verzija

*(Četvrtak, 02.april.2026, 18:00 / 06:00 PM, vremenska zona: CEST / UTC+2 / GMT+2)*

{{< youtube "h_uCyxVRivM" >}}