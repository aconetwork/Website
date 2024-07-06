---
title: "Kako spremeniti velikost teksta ter ikono mape zaznamkov v Mozilla Firefox"
date: 2018-08-15T18:00:00+02:00
url: /firefox-tekst-velikost-ikona-mape/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - kako
tags: 
  - Windows
  - Mozilla Firefox
showtoc: true  # Seznam vsebine: Skriti (false) ali prikazati (true)
draft: false  # Prikaz na javni strani: Prikaz (false) ali skriti (true)
---

Pa nastavimo velikost pisave Firefoxa in spremenimo ikone map z zaznamki. **Preden** to storite, se prepričajte:

- da znotraj `about:config` in nastavite `toolkit.legacyUserProfileCustomizations.stylesheets` (hiter dvoklik s levo miškino tipko) na `true`, hiter vodič najdete tukaj: [Popravite Mozilla Firefox da ne ignorira userChrome.css](https://www.youtube.com/watch?v=rVJnEDhHXdQ&list=PLbvZxzmdNckxgR98xK9iSVsO4bySit-q2 "Kliknite/tapnite za obisk vodiča!"),
- da znotraj vašega raziskovalca datotek lahko vidite končnice datotek, kot so `.exe`, `.txt`, `.msi`, `.docx`, ... kot je na primer `file.exe` in ne samo imena datoteke kot `file`. Kako to naredite, si lahko ogledate v [video vodiču ob času 01:59](https://youtu.be/wWs_UwVntFU?si=jACAf5M_ZNkZE4MJ&t=119 "Kliknite/tapnite za skok na ta del videoposnetka!").

## Odprite mapo profila Firefox

1. Z levim gumbom miške kliknite gumb menija ![](/images/Mozilla-Firefox/mfirefox_menu_button.jpeg) in nato z levim gumbom miške kliknite `Pomoč`.

 ![](/images/Mozilla-Firefox/mfirefox_menu_help.sl.jpeg)

1. Z levim gumbom miške kliknite `Reševanje težav ...`.

 ![](/images/Mozilla-Firefox/mfirefox_menu_troubleshooting_info.sl.jpeg)

1. Levi gumb miške kliknite na gumb `Odpri mapo` v isti vrstici `Mapa s profilom`.

 ![](/images/Mozilla-Firefox/mfirefox_troubleshooting_info.sl.jpeg)

Lahko tudi odprete svoj raziskovalec datotek in odprete mapo profila brskalnika, podobno tej:

    C:\Users\WINDOWS_PROFILE\AppData\Roaming\Mozilla\Firefox\Profiles\FIREFOX_PROFILE.default

Zamenjajte `WINDOWS_PROFILE` z imenom svojega profila Windows in `FIREFOX_PROFILE` z oznako profila Firefox.

## Ustvarite potrebno datoteko in jo pripravite

Preden naredite karkoli se prepričajte, da so prikazane končnice datotek v vašem raziskovalcu datotek, preverite [video vodič ob času 01:35](https://www.youtube.com/watch?v=U-uOC7PB4uE&t=119 "Kliknite/tapnite za skok na ta čas videa!"). Mapo in datoteko ki bomo naredili v spodnjih korakih mora biti **ENAKO** kot je napisano tukaj!

1. V mapi profila Firefox ustvarite mapo z imenom `chrome` in jo odprite.
2. Ustvarite navadno besedilno datoteko in jo preimenujte v `userChrome.css`.
3. Zdaj odprite novo ustvarjeno datoteko `userChrome.css` z želenim besedilnim urejevalnikom kot naprimer [Notepad++](https://notepad-plus-plus.org/ "Kliknite/tapnite za obisk Notepad++!") ali kaj drugega.
4. Na samem začetku datoteke se prepričajte, da vpišete oz. kopirate ter prilepite točno tako:
   
       @namespace url(http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul);

5. Shranite spremembe, ki ste jih naredili. Vsi programi nimajo enakega načina shranjevanja datoteke, vendar običajno lahko to storite tako, da z levim gumbom miške kliknete `Datoteka` v zgornjem glavnem meniju in z levim gumbom miške kliknete `Shrani`, bližnjica na tipkovnici za shranjevanje je `CTRL + S` (kliknite `CTRL` in med držanjem kliknite `S`, nato spustite obe tipki).

## Izvajanje sprememb v userChrome.css

Znotraj `userChrome.css` mora biti tako:

    @namespace url(http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul);

    /* Spremenimo vse ikone map zaznamkov */
    .bookmark-item[container] {
        list-style-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAjklEQVR42mNkAIIfx2xbgVQWAwHw//9/hh9cVgxX7ny5aBs6zQEkxgg1YD2QCiBkAAgwCdowXH0u8cHQKV9w1ICBNODaC4kvH24vUHVIO/+CLANuvhJnUGVdu4PD6rAnJQYcABrgOMIN2A00wI3MaBT/+vHOQl371PP3YQYQn505rRgu3/180S50ugNIDACEZogRw/LarAAAAABJRU5ErkJggg==') !important;
    }

    /* Globalna velikost pisave brskalnika */
    * { font-size: 12pt !important; }

Ko naredite spremembe **VEDNO** shranite spremembe v datoteko, sicer jih Firefox ne bo videl. Karkoli je med `/*` in `*/`, to je komentar ter Firefox bo to besedilo prezrl. 

Dekonstruirajmo zgornjo kodo v nadaljevanju... .

### Prvi del je izbira ikone map zaznamkov:

    /* Mapa z zaznamki uporabniškega vmesnika */
    .bookmark-item[container] {
        list-style-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAjklEQVR42mNkAIIfx2xbgVQWAwHw//9/hh9cVgxX7ny5aBs6zQEkxgg1YD2QCiBkAAgwCdowXH0u8cHQKV9w1ICBNODaC4kvH24vUHVIO/+CLANuvhJnUGVdu4PD6rAnJQYcABrgOMIN2A00wI3MaBT/+vHOQl371PP3YQYQn505rRgu3/180S50ugNIDACEZogRw/LarAAAAABJRU5ErkJggg==') !important;
    }

Katero ikono želite postaviti med apostrofe v `url`, kot je naprimer `icon.png`, kjer je dejanska datoteka ikone v mapi `chrome`, ki smo jo ustvarili prej:

 slika v slogu seznama: url('ikona.png') !pomembno;

Uporabite lahko `base64`, `svg`, `png`, `jpg`, `jpeg`, `bmp`, ... odvisno od vaših potreb.

Ta koda spremeni vse mape zaznamkov s enako ikono vendar v primeru, če želite spremeniti ikono posamezne mape, morate spremeniti `.bookmark-item[container]` v `.bookmark-item[container][label="Ime mape"]`, kjer je `Ime mape` ime vaše mape v brskalniku. Za naslednjo mapo pa samo duplirajte `.bookmark-item[containe...}` in spremenite `Ime mape` ter ikono.

    /* Spremenimo ikono prve mape zaznamkov */
    .bookmark-item[container][label="Ime mape"] {
        list-style-image: url('Ikona prve mape.png') !important;
    }

    /* Spremenimo ikono prve mape zaznamkov */
    .bookmark-item[container][label="Drugo ime mape"] {
        list-style-image: url('Ikona druge mape.png') !important;
    }

### Drugi del je nastavitev globalne velikosti besedila Firefox:

    /* Globalna pisava uporabniškega vmesnika */
    * { font-size: 12pt !important; }

Spremenite številko `12pt` na poljubno velikost, na primer `16pt` in shranite spremembo v datoteko. Spremenite samo številko ampak `pt` ostane enak.

## Vodič v drugih jezikih

- [Srbski (srpski)](https://www.youtube.com/watch?v=qgD5EVDq4uo&list=PLbvZxzmdNckxgR98xK9iSVsO4bySit-q2 "Kliknite/tapnite da otvorite! Kliknite/tapnite da odprete!")
- [English (angleški)](https://www.youtube.com/watch?v=wWs_UwVntFU&list=PLbvZxzmdNckw4vDyB8cQtRTp2kn_fHtuI "Click/tap to open! Kliknite/tapnite da odprete!")

## Video vodič

{{< youtube "U-uOC7PB4uE" >}}