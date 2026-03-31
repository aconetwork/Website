---
title: "Onemogočite novo stransko vrstico v Mozilla Firefox "
date: 2026-03-31T14:26:42+02:00
# publishDate: 2026-03-31T14:26:42+02:00
url: /firefox-onemogoci-nsvrstico-sl/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - Kako
tags: 
  - Kako
  - Windows
  - Linux
  - Mozilla Firefox
showtoc: false  # Seznam vsebine: Skriti (false) ali prikazati (true)
draft: false  # Prikaz na javni strani: Prikaz (false) ali skriti (true)
language: "Slovenski"
---

Nova stranska vrstica v Firefox-u je moteča saj se v mojem primeru pojavlja sama od sebe, zato jo onemogočimo in zamenjajmo s stransko vrstico s zaznamki ali zgodovino odvisno od nastavitev brskalnika.

{{< figure align=center src="/images/Mozilla-Firefox/mfirefox_nova_stranska_vrstica_s_tipko_-_tipka.sl.jpeg">}}

{{< notice tip >}}
  Preden začnete obvezno odprite spletni brskalnik Mozilla Firefox!
{{< /notice >}}

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** Z levo miškino tipko kliknite znotraj naslovne vrstice v Mozzili Firefox, napišite `about:config` in nato pritisnite tipko `Enter` na tipkovnici" openByDefault=true >}}

  Če je v polju že nekaj teksta ga odstranite ali izberite in začnite pisati naslov:

    about:config
  
  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_url_-_about_config.jpeg">}}

  {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" title="Leva Enter tipka">}}
  {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" title="Desna Enter tipka">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Če zagledate opozorilo `Nadaljujte previdno` z levo miškino tipko kliknite na tipko `Sprejmi tveganje in nadaljuj`" openByDefault=true >}}
  
  To opozorilo velja če res želite vstopiti v napredne konfiguracije brskalnika. Če natančno sledite tem vodiču ne boste imeli nobenih težav.

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_about_config_-_tipka_sprejmi.sl.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Z levo miškino tipko kliknite znotraj iskalnega polja, napišite `sidebar.rev` da zagledate rezultat `sidebar.revamp`" openByDefault=true >}}

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_about_config_-_sidebar.revamp_-_true.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Z levo miškino tipko kliknite na tipko `Preklopi` na koncu vrstice `sidebar.revamp` za vklop ali izklop nove stranske vrstice" openByDefault=true >}}

  `true` za omogočiti ali `false` za onemogočiti nove stranske vrstice.

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_about_config_-_sidebar.revamp_-_true_-_tipka_preklopi.sl.jpeg" title="true">}}
  {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_-_about_config_-_sidebar.revamp_-_false_-_tipka_preklopi.sl.jpeg" title="false">}}

{{< /collapse >}}