---
title: "Kako instalirati i upotrebiti Bulk Crap Uninstaller (osnove)"
date: 2025-08-22T00:00:00+02:00
# publishDate: 2025-08-09T15:26:43+02:00
url: /bcu-sr/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - kako
tags: 
  - Windows
  - Bulk Crap Uninstaller
showtoc: true  # Tabela sadržaja: Sakriti (false) ili pokazati (true).
draft: true   # Prikaz na javnoj stranici: Prikaz (false) ili sakriti (true).
language: "Srpski"
---

[Bulk Crap Uninstaller](https://www.bcuninstaller.com/ "Kliknite/tapnite, da otvorite stranicu!") (isto poznat kao BCUninstaller ili kratko BCU) je besplatni program otvorenog koda za deinstalaciju programa u [Windows](https://www.microsoft.com/en-us/windows "Kliknite/tapnite, da otvorite stranicu!") ima i mogučnost, da presnimate program za operativne sisteme [Linux](https://www.linux.org/ "Kliknite/tapnite, da otvorite stranicu!"), [Mac](https://www.apple.com/mac/ "Kliknite/tapnite, da otvorite stranicu!"), ... i kao bilo koj drugi deinstalacijski program ([Revo Uninstaller](https://www.revouninstaller.com/ "Kliknite/tapnite, da otvorite stranicu!"), [GEEK UNINSTALLER](https://geekuninstaller.com/ "Kliknite/tapnite, da otvorite stranicu!"), [IObit Uninstaller](https://www.iobit.com/en/advanceduninstaller.php "Kliknite/tapnite, da otvorite stranicu!"), [Uninstalr](https://uninstalr.com/ "Kliknite/tapnite, da otvorite stranicu!") i ostali) probaju da izbrišu ostatke (fajlove/datoteke, fascikle i unose registra) koje je pustila deinstalacija željenog programa (oficielni deinstalacijski program) iza. BCU ima puno opcija i vodiče vas korak po korak kao i ja. Ni jedan deinstalacijski program neče izbriše sve ostatke više puta zbog drugačijeg imena fascikla, i tako dalje.

{{< notice warning >}}
  U nekim slučajevima (mala verovatnoća) preostali rezultati deinstalacije MOGU sadržati neželjene elemente i ako se obrišu, nešto drugo u vašem sistemu može početi da se ponaša pogrešno. Nijedan program za deinstalaciju nije savršen i ja ne snosim odgovornost za eventualnu štetu! U slučaju da nešto više ne radi kako treba, idite na komentare na YouTube video i napišite svoje pitanje.
{{< /notice >}}

{{< notice note >}}
  Ovaj tutorijal je bio napravljen na 64 bitnom Windows 11 24H2!
{{< /notice >}}

## Instalirajte Bulk Crap Uninstaller sa winget

*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Desnim dugmetom miša kliknite na `Start` meni dugme" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Win10sr_-_start_btn_pocetak.jpeg" title="Windows 10 Start dugme" >}}
  {{< figure align=center src="/images/other/win11/Win11sr_-_start_btn_start.jpeg" title="Windows 11 Start dugme" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Levim dugmetom miša kliknite na `Windows PowerShell` ili `Terminal` kao administrator" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Win10sr_-_start_btn_rmb_-_windows_powershell_admin_btn.jpeg" >}}
  {{< figure align=center src="/images/other/win11/Win11sr_-_start_btn_-_terminal_administrator_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** U novom prozoru upišite winget komandu i onda pritisnite dugme `Enter` na tastaturi za instalaciju BCU" openByDefault=true >}}

  Winget komanda:

    winget install -e --id Klocman.BulkCrapUninstaller

  Dugme `Enter` na tastaturi:

  {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
  {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}

  Tutorijal oko `Winget` če napravim u budučnosti!

{{< /collapse >}}

## Preuzimanje i instaliranje Bulk Crap Uninstaller (ručno) (uključujući prenosivu verziju)

{{< notice tip >}}
  Da instalirate BCU preuzmite instalacionu datoteku ILI bez instalacije preuzmite prenosivu verziju. Pogledajte `Korak 6` za više informacija!
{{< /notice >}}

*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Levim dugmetom miša otvorite željeni veb pregledač (Google Chrome, Mozilla Firefox, Brave, ...)" openByDefault=true >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** U polje adrese veb-sajta (URL) upišite BCU adresu i pritisnite dugme `Enter` na tastaturi da je otvorite" openByDefault=true >}}

  BCU veb-sajt adresa:

    https://www.bcuninstaller.com/

  Dugme `Enter` na tastaturi:

  {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
  {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}

  Ako postoji neka veb adresa u polju za URL, levim dugmetom miša kliknite u prazan deo polja za URL da označite trenutnu adresu i počnete da kucate svoju adresu.

  Ako je URL polje prazno, možete jednostavno levim dugmetom miša da kliknete negde unutra i početi da kucate.

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Na BCU veb-sajtu levim dugmetom miša kliknite na zeleno dugme `Download on SourceForge` ili `Download on dAppCDN` da presnimate program" openByDefault=true >}}

  Može presnimate sa `SourceForge` ili `dAppCDN` (može da bude drugačije u budučnosti). Za ovaj tutorial sam odabrao `SourceForge`.

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Levim dugmetom miša kliknite na `Files`" openByDefault=true >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Levim dugmetom miša kliknite na `Latest version`" openByDefault=true >}}

  U vremenu snimanja ovog tutorijala je zadnja verzija `v5.9`.

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Levim dugmetom miša kliknite na potreban instalacioni fajl/datoteku i sačekajte, da se fajl presnima" openByDefault=true >}}

  U vremenu snimanja ovog tutorijala instalacioni fajl je `BCUninstaller_5.9.0_setup.exe` ali prenosiva verzija je `BCUninstaller_5.9.0_portable.zip`.

  Prenosivu verziju samo preuzmete, raspakujete je pomoću arhivnog programa kao što je [7zip](https://www.7-zip.org/ "Kliknite/tapnite, da otvorite stranicu!") ili integrirani arhiver u Windows 10 i 11. 
  
  Ako imate 64-bitni Windows, u raspakovanoj fascikli levim dugmetom miša otvorite `win-x64`, ali ako je Windows 32-bitni otvorite `win-x86` levim dugmetom miša, a nakon toga pokrenite program levim dugmetom miša na `BCUninstaller.exe`. 
  
  Na 32-bitnom Windowsu ne možete pokrenete 64-bitni program ali inače možete da pogledate ovaj tutorial: [Je vaš Windows 32 ili 64 bitni? 4. načina da ustanovite ](https://www.youtube.com/watch?v=hFldi8cEABU "Kliknite/tapnite, da otvorite YouTube tutorijal!")

{{< /collapse >}}

{{< collapse summary="**Korak 7:** " openByDefault=true >}}

{{< /collapse >}}

{{< collapse summary="**Korak 8:** " openByDefault=true >}}

{{< /collapse >}}

{{< collapse summary="**Korak 9:** " openByDefault=true >}}

{{< /collapse >}}

{{< collapse summary="**Korak 10:** " openByDefault=true >}}

{{< /collapse >}}

{{< collapse summary="**Korak 11:** " openByDefault=true >}}

{{< /collapse >}}

{{< collapse summary="**Korak 12:** " openByDefault=true >}}

{{< /collapse >}}

{{< collapse summary="**Korak 13:** " openByDefault=true >}}

{{< /collapse >}}

{{< collapse summary="**Korak 14:** " openByDefault=true >}}

{{< /collapse >}}

## Opening BCU for the first time



## BCU interface



## Uninstalling a program



## Links

- [Bulk Crap Uninstaller website](https://www.bcuninstaller.com/ "Kliknite/tapnite, da otvorite stranicu!")

## Video version

*(..2025, 18:00 / 06:00 PM, vremenska cona: CEST / UTC+2 / GMT+2)*

{{< youtube "O1DA0HpFK-4" >}}