---
title: "Nastaviti isto glasnost na več MP3 datotek hkrati s foobar2000"
date: 2022-06-18T18:00:00+02:00
url: /foobar2000-mp3-glasnost-sl/
# image: images/2022-thumbs/0617_foobar2000.jpg
categories:
    - kako
tags:
    - Windows
    - kako
    - foobar2000
showtoc: true
draft: false
language: "Slovenski"
---

Program [foobar2000](https://www.foobar2000.org/ "Kliknite/tapnite, da odprete spletno stran!") je predvajalnik glasbe z veliko funkcijami, vključno z normalizacijo več zvočnih datotek MP3 hkrati. Ne pozabite, da ta program nastavlja glasnost glede na zaznano glasnost in ne glede na dejansko glasnost!

## Prvi zagon programa in uvoz glasbenih datotek

Ko prvič odprete program `foobar2000` se odpre okno `quick Apperance Setup` (prevod: Hitra nastavitev videza), lahko nastavite `Main layout` (prevod: Glavna postavitev), `Colors` (prevod: Barve) in `Playlist Layout` (prevod: Postavitev seznama predvajanja) (preverite spodnji [video](#video-verzija "Kliknite/tapnite, da odprete razdelek!") za več podrobnosti). Zdaj uvozite glasbeni MP3 tako, da povlečete glasbene, datoteke iz mape na vašem računalniku v seznam predvajanja ALI v meniju programa kliknite `File` (prevod: Datoteka) in `Add files` (prevod: Dodaj datoteke...). (Poglejte razdelek [Video verzija](#video-verzija "Kliknite/tapnite, da odprete razdelek!") za slikovno predstavitev)

## Analizirajte več glasbenih datotek MP3 za ogled glasnosti (če želite vedeti glasnosti)

{{< collapse summary="**Korak 1:** Izberite vso glasbo s seznama predvajanja, ki jo želite analizirati in z desno miškino tipko kliknite na izbrano" openByDefault=true >}}

   ![](/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb.jpeg)

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Pojdite čez `ReplayGain` in z levo miškino tipko kliknite na `Scan per-file track gain` (prevod: Skeniraj in ojačaj posamezno datoteko)" openByDefault=true >}}

   ![](/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb-scan.jpeg)

   V novem oknu vidite seznam glasbenih datotek, pod stolpcem `Track gain` (prevod: ojačitev posnetka) pa vidite, koliko glasnejše (+) ali tišje (-) so glasnosti od 89db (**d**eci**b**el). Če želite trenutne vrednosti `ReplayGain` vstaviti v informacije datotek MP3, s levo miškino tipko kliknite na gumb `Update File Tags` (prevod: Posodobi oznake datoteke), v nasprotnem primeru pa z levo miškino tipko kliknete tipko `Cancel` (prevod: Prekliči).

{{< /collapse >}}

## Normalizirajte glasnost več glasbenih datotek MP3

**PREDEN naredite karkoli z zvočnimi datotekami, jih boste spremenili, najprej naredite varnostno kopijo, na primer podvojeno mapo z glasbenimi datotekami, tako da boste ob urejanju izvirnika imeli kopijo, če gre kaj narobe!!!**

{{< collapse summary="**Korak 1:** Izberite vso glasbo s seznama predvajanja, ki jo želite urediti in z desno miškino tipko kliknite na izbrano" openByDefault=true >}}

   ![](/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb.jpeg)

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Pojdite čez `ReplayGain` in z levo miškino tipko kliknite na `Apply gain to file content...` (prevod: Uporabi ojačanje za vsebino datoteke...)" openByDefault=true >}}

   ![](/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb-apply.jpeg)

{{< /collapse >}}

{{< collapse summary="**Korak 3:** You can use default settings (like on picture bellow) and left mouse button click on the `Start` button" openByDefault=true >}}

   ![](/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb-apply-start.jpeg)

   V oknu `Apply gain to file contents - Setup` lahko nastavite ogromno stvari, vendar predlagam, da izberete:
   - Izberite `Apply track ReplayGain` (prevod: Nastavi ReplayGain na datoteko).
   - Nastavite `Target volume level:` (prevod: Ciljni nivo glasnosti) na `89db`.
   - Izberite `Make files louder or quieter` (prevod: Naredi datoteko glasneje ali tiše).
   - Označite `Lower adjustment to prevent clipping according to peak information` (prevod: Znižajte nastavitev za preprečitev rezanja vrhov), če je kateri koli del glasbe glasnejši od 98 db (to pomeni izrezovanje), bo program samodejno znižal glasnost glasbe pod izbrano `Target volume level:`, vendar če ni označeno, preglasni deli bodo še vedno prisotni, vendar bo večina glasbenih predvajalnikov preprosto odrezala preglasne dele.

{{< /collapse >}}   <!-- (prevod: ) -->

## Po normalizaciji

Zdaj lahko znova [analizirate](#analizirajte-več-glasbenih-datotek-mp3-za-ogled-glasnosti-če-želite-vedeti-glasnosti "Kliknite/tapnite, da odprete razdelek!") datoteke, da preverite trenutno glasnost zvoka. Običajno je, da so zelo majhne razlike glasnosti po normalizaciji.

## Povezave, več info

- [foobar2000 site](https://www.foobar2000.org/ "Kliknite/tapnite, da odprete spletno stran!")
- [How to download and install foobar2000 - moj vodič](/foobar2000-namestitev-sl/ "Kliknite/tapnite, da odprete vodič!")
- [Perceived Volume vs Actual Volume](https://www.youtube.com/watch?v=5SQFV8fv0Ho "Kliknite/tapnite, da odprete spletno stran!") ![- YouTube](/images/social-logos/YouTube.png)
- [Perceived Loudness Explained](https://www.blackghostaudio.com/blog/perceived-loudness-explained "Kliknite/tapnite, da odprete spletno stran!")
- [Loudness](https://en.wikipedia.org/wiki/Loudness "Kliknite/tapnite, da odprete spletno stran!") ![- Wikipedia](/images/social-logos/logo_Wikipedia_20x20px.png)
- [LOUDNESS Explained](https://www.youtube.com/watch?v=rRsxwDd59kc "Kliknite/tapnite, da odprete spletno stran!") ![- YouTube](/images/social-logos/YouTube.png)

## Video verzija

{{< youtube "RCFniFPvrng" >}}