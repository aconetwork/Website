---
title: "Kako da podesite istu glasnoču za više MP3 od jedamput u foobar2000"
date: 2022-06-19T18:00:00+02:00
url: /foobar2000-mp3-glasnoca-sr/
# image: images/2022-thumbs/0617_foobar2000.jpg
categories:
    - kako
tags:
    - Windows
    - kako
    - foobar2000
showtoc: true
draft: false
language: "Srpski"
---

Program [foobar2000](https://www.foobar2000.org/ "Click/tap to open the website!") je muzički plejer sa puno funkcija uključujući normalizaciju više MP3 audio datoteka odjednom. Zapamtite da ovaj program podešava jačinu zvuka prema percipiranoj jačini zvuka, a ne prema stvarnoj jačini zvuka!

## Prvo pokretanje programa i uvoz muzičkih fajlova

Kada se program `foobar2000` otvori prvi put u prozoru `brzo podešavanje izgleda`, možete izabrati željeni program `Glavni izgled`, `Boje` i `Izgled liste za reprodukciju` (pogledajte video ispod za više detalja). Sada uvezite muzički MP3 prevlačenjem muzičkih datoteka iz fascikle na vašem računaru u `foobar2000` listu pesama ILI u meniju programa kliknite na `Datoteka` i `Dodaj datoteke...`.

## Analizirajte/skenirajte glasnoče više MP3 muzičkih datoteka (ako želite da znate glasnoču pre normalizacije)

{{< collapse summary="**Korak 1:** Izaberite svu muziku sa liste koje želite da analizirate i kliknite desnim dugmetom miša na izabrano" openByDefault=true >}}

   {{< figure align=center src="/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Idite preko `ReplayGain` i sa levim dugmetom miša kliknite na `Scan per-file track gain` (prevod: Skeniraj i ojačaj inviduelnu datoteku)" openByDefault=true >}}

   {{< figure align=center src="/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb-scan.jpeg" >}}

   V novem oknu vidite seznam glasbenih datotek, pod stolpcem `Track gain` (prevod: glasnost posnetka) pa vidite, koliko glasnejše (+) ali tišje (-) so glasnosti od 89db (**d**eci**b**el). Ako želite trenutačne vrednosti ubaciti u informacije datoteka MP3, sa levim dugmetom miša kliknite na durgme `Update File Tags` (prevod: Ažuriraj oznake datoteka), u nasprotnom primeru pa sa levim dugmetom miša kliknite na durgme `Cancel` (prevod: otkaži).

{{< /collapse >}}

## Normalizujte jačinu većih MP3 muzičkih datoteka

**PRE nego što bilo šta uradite sa svojim audio datotekama, prvo ćete modifikovati napraviti rezervnu kopiju, na primer duplikat foldera sa vašim muzičkim fajlovima, tako da kada uređujete original, imate kopiju u slučaju da nešto krene po zlu!!!!**

{{< collapse summary="**Korak 1:** Izaberite svu muziku sa liste koje želite da analizirate i kliknite desnim dugmetom miša na izabrano" openByDefault=true >}}

   {{< figure align=center src="/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Idite preko `ReplayGain` i sa levim dugmetom miša kliknite na `Apply gain to file content...` (prevod: Primeni pojačanje na sadržaj datoteke...)" openByDefault=true >}}

   {{< figure align=center src="/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb-apply.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Možete koristiti podrazumevana podešavanja (kao na slici ispod) i kliknuti levim dugmetom miša na dugme `Start`" openByDefault=true >}}

   {{< figure align=center src="/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb-apply-start.jpeg" >}}

   U prozoru `Apply gain to file contents - Setup` (prevod: Primeni podešavanja na sadržaj datoteke - Podešavanje) možete podesiti gomilu stvari, ali predlažem da izaberete:
   - Izaberite `Apply track ReplayGain` (prevod: Primeni ReplayGain po datoteki) .
   - Podesite `Target volume level:` (prevod: Ciljni nivo jačine zvuka:) na `89db`. 
   - Izaberite `Make files louder or quieter` (prevod: Učini datoteke glasnije ili tiše).
   - Proverite `Lower adjustment to prevent clipping according to peak information` (prevod: Smanjite podešavanje da bi sprečili kliping u skladu sa informacijama vrhova) u slučaju da je bilo koji deo muzike glasniji od 98db (to znači kliping) program će automatski smanjiti jačinu muzike ispod izabranog `Ciljni nivo jačine:` ali ako nije označeno, preglasni delovi će i dalje biti prisutni, ali će i većina muzičkih plejera jednostavno rezati preglasne delove.

{{< /collapse >}}   <!-- (prevod: ) -->

## Posle normalizacije

Sada možete ponovo [analizirati/skenirati](#analizirajteskenirajte-glasnoče-više-mp3-muzičkih-datoteka-ako-želite-da-znate-glasnoču-pre-normalizacije "Kliknite/tapnite, da otvorite razdelak!") datoteke da bi proverili trenutne glasnoče fajlova. 

Zdaj lahko znova [analizirate](#analizirajte-več-glasbenih-datotek-mp3-za-ogled-glasnosti-če-želite-vedeti-glasnosti "Kliknite/tapnite, da otvorite razdelak!") datoteke, da preverite trenutno glasnost zvoka. Uobičajeno je, da postoje veoma male razlike u glasnočima nakon normalizacije.

## Linkovi, više info

- [foobar2000 site](https://www.foobar2000.org/ "Kliknite/tapnite, da otvorite veb stranicu!")
- [How to download and install foobar2000 - moj tutorial](/foobar2000-instalacija-sr/ "Kliknite/tapnite, da otvorite tutorijal!")
- [Perceived Volume vs Real Volume](https://www.youtube.com/vatch?v=5SKFV8fv0Ho "Kliknite/tapnite, da otvorite video!") ![- YouTube](/images/social-logos/YouTube.png)
- [Objašnjeno perceived Loudness](https://www.blackghostaudio.com/blog/perceived-loudness-ekplained "Kliknite/tapnite, da otvorite veb stranicu!")
- [Loudness)](https://en.wikipedia.org/wiki/Loudness "Kliknite/tapnite, da otvorite veb stranicu!") ![- Wikipedia](/images/social-logos/logo_Wikipedia_20x20px.png)
- [Objašnjenje glasnoće](https://www.youtube.com/vatch?v=rRskvDd59kc "Kliknite/tapnite, da otvorite video!") ![- YouTube](/images/social-logos/YouTube.png)

## Video tutorijal

{{< youtube "BWtKYqebcQQ" >}}