---
title: "Kako promeniti veličinu teksta i ikonu fascikle obeleživača u Mozilla Firefox"
date: 2018-08-16T18:00:00+02:00
url: /firefox-velicina-teksta-ikona-fascikle/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - kako
tags: 
  - Windows
  - Mozilla Firefox
showtoc: true  # Tabela sadržaja: Sakriti (false) ili pokazati (true).
draft: false   # Prikaz na javnoj stranici: Prikaz (false) ili sakriti (true).
language: "Srpski"
---

Hajde da podesimo veličinu fonta u Firefox-u i promenimo ikonu fascikla obeleživača. **Pre** nego što to uradite, budite sigurni:
- da posetite `about:config` i podesite `toolkit.legacyUserProfileCustomizations.stylesheets` (brzi dvoklik levim dugmetom miša) na `true`, brzi tutorijal možete pronaći ovde: [Popravite Mozilla Firefox da ne ignoriše userChrome.css](https://www.youtube.com/watch?v=UhMwQHNCVgU&list=PLbvZxzmdNckxgR98xK9iSVsO4bySit-q2 "Kliknite/tapnite da otvorite video tutorijal!"),
- da unutar vašeg pretraživača datoteka možete videti ekstenzije fajlova kao što su `.exe`, `.txt`, `.msi`, `.docx`, ... kao na primer `fajl.exe`, a ne samo ime datoteke kao `fajl`. Možete da vidite kako to da uradite u [video tutorijalu na 02:12](https://www.youtube.com/watch?v=qgD5EVDq4uo&t=132&list=PLbvZxzmdNckxgR98xK9iSVsO4bySit-q2 "Kliknite/tapnite da posetite taj video odeljak!").

## Otvorite fasciklu profila Firefok-a

1. Kliknite levim dugmetom miša na dugme menija {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_menu_button.jpeg" >}}, a zatim levim dugmetom miša kliknite na `Pomoć`.
   
   {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_menu_help.sr-cyr.jpeg" >}}

2. Kliknite levim dugmetom miša na `Podaci o rešavanju problema`.
   
   {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_menu_troubleshooting_info.sr-cyr.jpeg" >}}

3. Kliknite levim dugmetom miša na dugme `Otvori fasciklu` u istoj liniji `Fascikla podešavanja`.
   
   {{< figure align=center src="/images/Mozilla-Firefox/mfirefox_troubleshooting_info.sr-cyr.jpeg" >}}

Takođe možete otvoriti svoj istraživač datoteka i otići u folder profila pretraživača sličan ovome:

    C:\Users\WINDOWS_PROFILE\AppData\Roaming\Mozilla\Firefox\Profiles\FIREFOX_PROFILE.default

Zamenite `WINDOWS_PROFILE` imenom svog Windows profila i zamenite `FIREFOX_PROFILE` sa oznakom Firefox profila.

## Napravite potrebnu datoteku i pripremite je

Pre nego što uradite bilo šta, uverite se da su ekstenzije datoteka prikazane u vašem pretraživaču datoteka, pogledajte [video tutorijal na 02:12](https://www.youtube.com/watch?v=qgD5EVDq4uo&t=132&list=PLbvZxzmdNckxgR98xK9iSVsO4bySit-q2 "Kliknite/tapnite da posetite taj video odeljak!"). Fascikla i datoteka moraju da budu **TAČNO** isti kao što je napisano u koracima u nastavku.

1. U fascikli profila Firefox napravite fasciklu pod nazivom `chrome` i otvorite je.
2. Napravite običnu tekstualnu datoteku i preimenujte je u `userChrome.css`.
3. Sada otvorite novu datoteku `userChrome.css` pomoću željenog uređivača teksta.
4. Na samom početku obavezno ukucajte ili kopirajte i nalepite tačno ovako: 
   
       @namespace url(http://www.mozilla.org/keimaster/gatekeeper/there.is.onli.kul);

5. Sačuvajte promene koje ste napravili. Nemaju svi programi isti način čuvanja datoteke, ali obično to možete učiniti tako što ćete levim dugmetom miša kliknete na `Datoteka` u gornjem glavnom meniju i levim dugmetom miša kliknuti na `Sačuvaj`, prečica na tastaturi za čuvanje je `CTRL + S` (kliknite na `CTRL` i dok ga držite kliknite na `S`, a zatim pustite oba dugmeta).

## Promene u userChrome.css

Unutar `userChrome.css` bi trebalo da izgleda ovako:

    @namespace url(http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul);
    
    /* Promena svih ikona fascikla obeleživača */
    .bookmark-item[container] {
        list-style-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAjklEQVR42mNkAIIfx2xbgVQWAwHw//9/hh9cVgxX7ny5aBs6zQEkxgg1YD2QCiBkAAgwCdowXH0u8cHQKV9w1ICBNODaC4kvH24vUHVIO/+CLANuvhJnUGVdu4PD6rAnJQYcABrgOMIN2A00wI3MaBT/+vHOQl371PP3YQYQn505rRgu3/180S50ugNIDACEZogRw/LarAAAAABJRU5ErkJggg==') !important;
    }

    /* Veličina fonta globalnog korisničkog interfejsa */
    * { font-size: 12pt !important; }

Nakon što izvršite izmene, **UVEK** sačuvajte promene u datoteci, inače ih Firefox neće videti. Šta god da je između `/*` i `*/` je komentar i firefox će ignorisati taj tekst. 

Hajde da dekonstruišemo gornji kod ispod... .

### Prvi deo: da izaberete ikonu fascikle sa obeleživačima:

    /* Promena svih ikona fascikla obeleživača */
    .bookmark-item[container] {
        list-style-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAjklEQVR42mNkAIIfx2xbgVQWAwHw//9/hh9cVgxX7ny5aBs6zQEkxgg1YD2QCiBkAAgwCdowXH0u8cHQKV9w1ICBNODaC4kvH24vUHVIO/+CLANuvhJnUGVdu4PD6rAnJQYcABrgOMIN2A00wI3MaBT/+vHOQl371PP3YQYQn505rRgu3/180S50ugNIDACEZogRw/LarAAAAABJRU5ErkJggg==') !important;
    }

Stavite svoju ikonu između apostrofa u `url` kao za primer što je `ikona.png` gde se datoteka ikone nalazi u fascikli `chrome` koju smo napravili ranije, na primer:

    list-stile-image: url('ikona.png') !important;

Možete koristiti `base64`, `svg`, `png`, `jpg`, `jpeg`, `bmp`, ... zavisi od vaših potreba.

Ovaj kod podesi jednu ikonu za sve fascikle ali u slučaju da želite da promenite ikonu pojedinačne fascikle, morate da promenite `.bookmark-item[container]` u `.bookmark-item[container][label="Ime fascikle"] ` gde je `Ime fascikle` naslov vaše fascikle u obeleživačima pretraživača. Za sledeću fascicklu samo duplirajte `.bookmark-item[containe...}` i promenite `ime fascikle` sa ikonom, evo primer:

    /* Promena ikone obeleživača prve fascikle */
    .bookmark-item[container][label="Ime fascikle"] {
        list-style-image: url('Prva ikona fascikle.png') !important;
    }

    /* Promena ikone obeleživača druge fascikle */
    .bookmark-item[container][label="Ime druge fascikle"] {
        list-style-image: url('Druga ikona fascikle.png') !important;
    }

### Drugi deo: podešavanje globalne veličine teksta za Firefox:

    /* Globalna veličina teksta Firefox-a */
    * { font-size: 12pt !important; }

Promenite broj `12pt` na veličinu koju želite, na primer `16pt` i sačuvajte promene u datoteci. Promenite samo broj, `pt` uvek ostaje.

## Video version

{{< youtube "qgD5EVDq4uo" >}}

## Plejlista

[Mozilla Firefox tutorijali - SRPSKI](https://www.youtube.com/playlist?list=PLbvZxzmdNckxgR98xK9iSVsO4bySit-q2 "Kliknite/tapnite da otvorite plejlistu!")