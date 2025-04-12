---
title: "Set the same volume to multiple MP3 files with foobar2000"
date: 2022-06-17T18:00:00+02:00
url: /foobar2000-mp3-volume-en/
# image: images/2022-thumbs/0617_foobar2000.jpg
categories:
    - how to
tags:
    - Windows
    - how to
    - foobar2000
showtoc: true
draft: false
language: "English"
---

Remember that this program is setting the volume according the Perceived volume and not the actual volume!

## Briefly about the music volume

Music contains the sinus like waves and the volume is the average volume between quietest and the loudest part. We know 2 volume types where first is actual volume and second is percived volume. Perceived volume is what human ears can hear which is not the same as the actual volume. In the section [links more info](#links-more-info "Click/tap to go to that section!"), you can get way more info about music volumes etc..

## First program launch and music files import

When the program `foobar2000` if opened for the first time in the `quick Apperance Setup` window you can select prefered program looks `Main layout`, `Colors` and `Playlist Layout`. Now import the music MP3 by dragging the music files from a folder on your computer into a `foobar2000` playlist OR in the program menu click `File` and `Add files...`. (check the [Video version](#video-version "Click/tap to go to that section!") for more details)

![](/images/foobar2000/En-foobar2000-first-run.jpeg)

## Analyse/scan volumes of multiple MP3 files (if you want to know the individual file volumes)

{{< collapse summary="**Step 1:** Select all the music from the playlist you want to analyse and right mouse button click on the selected" openByDefault=true >}}

   ![](/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb.jpeg)

{{< /collapse >}}

{{< collapse summary="**Step 2:** Go over the `ReplayGain` and left mouse button click on the `Scan per-file track gain`" openByDefault=true >}}

   ![](/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb-scan.jpeg)

   In the new window you see list of music files, under the `Track gain` column you see how much louder (+) or quieter (-) volumes are from 89db (**d**eci**b**els). If you want to insert current `ReplayGain` values into MP3 file info click `Update File Tags` button othervise left mouse button click on the `Cancel` button.

{{< /collapse >}}

## Normalize volumes of multiple MP3 music files

**BEFORE you do anything to your audio files first do a backup. For example duplicate folder with your music files so when you edit original you have copy in case anything goes wrong!!!!**

{{< collapse summary="**Step 1:** Select all the music from the playlist you want to modify and right mouse button click the selected" openByDefault=true >}}

   ![](/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb.jpeg)

{{< /collapse >}}

{{< collapse summary="**Step 2:** Go over the `ReplayGain` and left mouse button click on the `Apply gain to file content...`" openByDefault=true >}}

   ![](/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb-apply.jpeg)

{{< /collapse >}}

{{< collapse summary="**Step 3:** You can use default settings (like on picture bellow) and left mouse button click on the `Start` button" openByDefault=true >}}

   ![](/images/foobar2000/En-foobar2000-playlist-select-mp3-lmb-apply-start.jpeg)

   In the `Apply Gain to File Contents - Setup` window you can set ton of stuff but I suggest you select:
   - Select the checkbox near the `Apply track ReplayGain` with left mouse button click.
   - Set `Target volume level:` to `89db`. 
   - Select the checkbox near the `Make files louder or quieter` with left mouse button click.
   - Select the checkbox near the `Lower adjustment to prevent clipping according to peak information` in case if any part of the music is louder than 98db (that means clipping) program will automatically lower the music volume bellow the selected `Target volume level:` but if unchecked too loud parts will be still there but I think most of music players will just cut off too loud parts.

{{< /collapse >}}

## After the normalize

Now you can [Analyse/scan](#analysescan-volumes-of-multiple-mp3-files-if-you-want-to-know-the-volumes "Click/tap to go to that section") the files again to check current sound volumes. It is normal to have slight volume differences between normalized audio files but that is normal.

## links more info

- [foobar2000 site](https://www.foobar2000.org/ "Click/tap to open the web page!")
- [How to download and install foobar2000 - my guide](/foobar2000-install-en/ "Click/tap to open the guide!")
- [Perceived Volume vs Actual Volume](https://www.youtube.com/watch?v=5SQFV8fv0Ho "Click/tap to open the web page!") ![- YouTube](/images/social-logos/YouTube.png)
- [Perceived Loudness Explained](https://www.blackghostaudio.com/blog/perceived-loudness-explained "Click/tap to open the web page!")
- [Loudness](https://en.wikipedia.org/wiki/Loudness "Click/tap to open the web page!") ![- Wikipedia](/images/social-logos/logo_Wikipedia_20x20px.png)
- [LOUDNESS Explained](https://www.youtube.com/watch?v=rRsxwDd59kc "Click/tap to open the web page!") ![- YouTube](/images/social-logos/YouTube.png)

## Video version

{{< youtube "jHT9IGQFsmI" >}}