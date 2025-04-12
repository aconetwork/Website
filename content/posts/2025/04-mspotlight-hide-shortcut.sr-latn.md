---
title: "Sakrijte prečicu Spotlight sa radne površine"
date: 2025-04-09T11:01:00+02:00
publishDate: 2025-04-17T12:00:00+02:00
url: /mspotlight-sakriti-precicu-sr/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - kako
tags: 
  - Windows
showtoc: true  # Tabela sadržaja: Sakriti (false) ili pokazati (true).
draft: true   # Prikaz na javnoj stranici: Prikaz (false) ili sakriti (true).
language: "Srpski"
---

Microsoft Spotlight je alat koji menja pozadinu vaše Windows radne površine preuzimanjem slika sa interneta. U ovom tutorijalu naučiću vas da sakrijete prečicu `Saznajte više o ovoj slici`  sa radne površine i sa time zadržite Spotlight slika na 2 načina.

## Definišite sopstvenu pozadinu, projekciju slajdova, boju, ...

*(Kliknite na pojedinačni naslov koraka ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Desnim dugmetom miša kliknite na praznu površinu Windows radne površine a zatim levim dugmetom miša kliknite na `Personalizuj`" openByDefault=true >}}

 

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Ispod `Pozadina` levim dugmetom miša kliknite na `Windows Spotlight` da izaberete šta želite" openByDefault=true >}}

 Možete potvrditi željenu opciju `Slika`, `Čvrsta boja`, `Slideshov` ili `Windows Spotlight` sa klikom levog dugmeta miša na nju. Sada samo podesite šta želite i uživajte.

{{< /collapse >}}

## Sakrijte prečicu na radnoj površini `Saznajte više o ovoj slici` sa pripremljenom datotekom registra (lakša metoda)

Da SAMO sakrijete prečicu `Saznajte više o ovoj slici` na radnoj površini, potrebno je da dodate nov ili izmenite postoječi ključ registra u Windows registru. Prvi način je samo da preuzmete reg datoteku koju sam pripremio za vas i upotrebite je. Ove datoteke u nastavku sam ja generisao ali ako im ne verujete, možete da koristite [teži način](#ručno-sakrijte-prečicu-saznajte-više-o-ovoj-slici-u-windows-registru-teža-metoda "Kliknite/tapnite da biste prešli na sledeći odeljak!") ispod! Dakle:

*(Kliknite na pojedinačni naslov koraka ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Presnimajte si registar datoteku" openByDefault=true >}}

 Da sakrijete prečicu upotrebite [spotlight-desktop-icon-hide.reg](/scripts/spotlight-desktop-icon-hide.reg "Kliknite/tapnite za prenos datoteke!") ili da sa pokažete sakrivenu prečicu upotrebite [spotlight-desktop-icon-show.reg](/scripts/spotlight-desktop-icon-show.reg "Kliknite/tapnite za prenos datoteke!").

 1. Da je presnimate, kliknite desnim dugmetom miša na link do datoteke i levim dugmetom miša kliknite na `Sačuvaj vezu kao`.

    

 2. Otvorite željenu fasciklu u koju želite da je sačuvate i kliknite levim dugmetom miša na dugme `Sačuvaj`.



{{< /collapse >}}

{{< collapse summary="**Korak 2:** Otvorite fasciklu u koju ste presnimali datoteku i otvorite je sa levim dugmetom miša" openByDefault=true >}}

  Ako se `Kontrola korisničkog naloga` ili bilo koji drugi sigurnosni prozor otvori levim dugmetom miša kliknite na dugme `Da` da bi dozvolili otvaranje.

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Levim dugmetom miša kliknite dugme `Yes` u prozoru `Uređivač registra`" openByDefault=true >}}



{{< /collapse >}}

{{< collapse summary="**Korak 4:** Kada je datoteka registra uspešno uvezena, levim dugmetom miša kliknite na dugme `OK`" openByDefault=true >}}

  

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Osvežite radnu površinu za prikaz promene" openByDefault=true >}}

  To je to.

{{< /collapse >}}


## Ručno sakrijte prečicu `Saznajte više o ovoj slici` u Windows registru (teža metoda)

*(Kliknite na pojedinačni naslov koraka ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Levim dugmetom miša kliknite na dugme Start menija" openByDefault=true >}}



{{< /collapse >}}

{{< collapse summary="**Korak 2:** Počnite da kucate na tastaturi `Registri Editor` i na levim dugmetom miša kliknite na `Registri Editor`" openByDefault=true >}}

  Ako se `Kontrola korisničkog naloga` ili bilo koji drugi sigurnosni prozor otvori levim dugmetom miša kliknite na dugme `Da` da dozvoljavate otvaranje.

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Levim dugmetom miša kliknite na dugme `Da` u prozoru `Registry Editor`" openByDefault=true >}}

  Ako se `Kontrola korisničkog naloga` ili bilo koji drugi sigurnosni prozor otvori levim dugmetom miša kliknite na dugme `Da` da dozvoljavate otvaranje.

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Uđite u `NewStartPanel`" openByDefault=true >}}

  Lokacija: `Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\HideDesktopIcons\NewStartPanel`

  Kopirajte/nalepite ili napišite lokaciju u gornjem polju za unos teksta i pritisnite dugme `Enter` na tastaturi ILI samo otvorite unose dok ne budete unutar `NewStartPanel`.

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Napravite `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` ključ ali ako postoji preskočite ovaj korak i idite na `Korak 6`" openByDefault=true >}}

  1. Uverite se da ste unutar `NewStartPanel` i kliknite desnim dugmetom miša u prazno područje.
  2. Pređite preko `Novo` i kliknite levim dugmetom miša na `DWORD (32-bitna) vrednost`.
  3. Otkucajte `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` (ili kopirajte i nalepite) i pritisnite dugme Enter na tastaturi.

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Desnim dugmetom miša kliknite `{2cc5ca98-6485-489a-920e-b3e88a6ccce3}` i onda sa levim dugmetom miša kliknite na `Uredite`" openByDefault=true >}}

 

{{< /collapse >}}

{{< collapse summary="**Korak 7:** Izpod `Value data` budite sigurni da je `1` i ne `0` i levim dugmetom miša potvrdite na klik dugmeta `Ok`" openByDefault=true >}}

  Da se sakrije prečica je `1` ili da se pokaže prečica je `0`

{{< /collapse >}}

{{< collapse summary="**Korak 8:** Osvežite radnu površinu za prikaz promene" openByDefault=true >}}

  To je to.

{{< /collapse >}}

<!--*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** TEXTHERE" openByDefault=true >}}

   

{{< /collapse >}}

[]( "Click/tap to open the site!")
![](/images/social-logos/X.png)

## Video verzija

{{< youtube "" >}}-->