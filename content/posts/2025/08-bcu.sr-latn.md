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

[Bulk Crap Uninstaller](https://www.bcuninstaller.com/ "Kliknite/tapnite, da otvorite stranicu!") (isto poznat kao BCUninstaller ili kratko BCU) je besplatni program otvorenog koda za deinstalaciju programa u [Windows](https://www.microsoft.com/en-us/windows "Kliknite/tapnite, da otvorite stranicu!") ima i mogučnost, da presnimate program za operativne sisteme [Linux](https://www.linux.org/ "Kliknite/tapnite, da otvorite stranicu!"), [Mac](https://www.apple.com/mac/ "Kliknite/tapnite, da otvorite stranicu!"), ... i kao bilo koj drugi deinstalacijski program ([Revo Uninstaller](https://www.revouninstaller.com/ "Kliknite/tapnite, da otvorite stranicu!"), [GEEK UNINSTALLER](https://geekuninstaller.com/ "Kliknite/tapnite, da otvorite stranicu!"), [IObit Uninstaller](https://www.iobit.com/en/advanceduninstaller.php "Kliknite/tapnite, da otvorite stranicu!"), [Uninstalr](https://uninstalr.com/ "Kliknite/tapnite, da otvorite stranicu!") i ostali) probaju da izbrišu ostatke (fajlove/datoteke, fascikle i unose registra) koje je pustila deinstalacija željenog programa (oficielni deinstalacijski program) iza. BCU ima puno opcija i vodiče vas korak po korak. Ni jedan deinstalacijski program neče izbriše sve ostatke više puta zbog drugačijeg imena fascikla, i tako dalje.

{{< notice warning >}}
  U nekim slučajevima (mala verovatnoća) preostali rezultati deinstalacije MOGU sadržati neželjene elemente i ako se obrišu nešto drugo u vašem sistemu može početi da se ponaša pogrešno. Nijedan program za deinstalaciju nije savršen i ja ne snosim odgovornost za eventualnu štetu! U slučaju da nešto više ne radi kako treba, idite na komentare na YouTube video i napišite svoje pitanje.
{{< /notice >}}

{{< notice note >}}
  Ovaj tutorijal je bio napravljen na 64-bitnom Windows 11 24H2!
{{< /notice >}}

## Instalirajte BCU sa winget

{{< notice info >}}
  U primeru da nemate WINGET ili ste dobili neku drugu grešku u prozoru gde instalirate BCU instalirajte ga na [ručni način](#instalirajte-bcu-sa-pre-presnimanom-setup-datotekom "Kliknite/tapnite da posetite sekciju!").
{{< /notice >}}

*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Desnim dugmetom miša kliknite na `Start` meni dugme i onda levim dugmetom miša kliknite na `Windows PowerShell` ILI `Terminal` kao Administrator" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Win10en_-_start_btn_start.jpeg" title="Windows 10 Start" >}}
  {{< figure align=center src="/images/other/win11/Win11en_-_start_btn_start.jpeg" title="Windows 11 Start" >}}
  {{< figure align=center src="/images/other/win10/Win10en_-_start_btn_-_windows_powershell_admin_btn.jpeg" >}}
  {{< figure align=center src="/images/other/win11/Win11en_-_start_btn_-_terminal_admin_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** U novom prozoru upišite winget komandu (pogledajte malo niže) i onda pritisnite dugme `Enter` na tastaturi za instalaciju BCU" openByDefault=true >}}

  Winget komanda:

    winget install -e --id Klocman.BulkCrapUninstaller

  Dugme `Enter` na tastaturi:

  {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
  {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}

  Tutorijal oko `Winget` če napravim u budučnosti!

{{< /collapse >}}

## Preuzmite BCU instalaciju i prenosivu verziju

{{< notice tip >}}
  Setup datoteka je za instaliranje BCU-a, ali prenosiva verzija nije i je samo pokrenete. Prenosivu verziju samo preuzmete, raspakujete pomoću programa za arhiviranje kao što je [7zip](https://www.7-zip.org/ "Kliknite/tapnite, da otvorite stranicu!") ili integrisani ekstraktor arhiva uključen u Windows 10 i 11 (proverite [odpakiranje i otvaranje prenosive verzije](#prenosiva-verzija-bcu---odpakiranje-i-pokretanje "Kliknite/tapnite, da skoknete na sekciju!")) i pokrenete ga. 
{{< /notice >}}

*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Levim dugmetom miša otvorite željeni veb pregledač i posetite veb stranicu BCU" openByDefault=true >}}

  U polje za adresu željenog veb pregledača (Google Chrome, Mozilla Firefox, Brave, ...) unesite ili kopirajte i nalepite adresu veb stranice BCU i pritisnite dugme Enter na tastaturi.

  Ako u polju za URL adresu već postoji neka veb adresa kliknite levim dugmetom miša na prazan deo polja za URL adresu kako bi izabrali trenutnu adresu i mogli da počnete da kucate svoju adresu. Ako je polje za URL adresu prazno, možete jednostavno kliknuti levim dugmetom miša negde unutra i početi da kucate.

  BCU veb-sajt adresa:

    https://www.bcuninstaller.com/

  Dugme `Enter` na tastaturi:

  {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
  {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Na BCU veb-sajtu levim dugmetom miša kliknite na zeleno dugme `Download on dAppCDN` ili `Download on SourceForge` da presnimate program" openByDefault=true >}}

  Može presnimate sa `dAppCDN` ili `SourceForge`. Za ovaj tutorial sam odabrao `SourceForge`.

  {{< figure align=center src="/images/bcu/bcu_-_website_download_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Levim dugmetom miša kliknite na `Files`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcu_-_website_download_-_files.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Levim dugmetom miša kliknite na najnoviju verziju" openByDefault=true >}}

  U vremenu snimanja ovog tutorijala je zadnja verzija `v5.9`.

  {{< figure align=center src="/images/bcu/bcu_-_website_download_-_files_-_ver5.9.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Levim dugmetom miša kliknite na potreban instalacioni fajl/datoteku i sačekajte, da se fajl presnima" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcu_-_website_download_-_files_-_ver5.9_-_setup.jpeg" title="Za instalaciju" >}}
  {{< figure align=center src="/images/bcu/bcu_-_website_download_-_files_-_ver5.9_-_portable.jpeg" title="Prenosiva verzija" >}}

{{< /collapse >}}

## Instalirajte BCU sa pre presnimanom setup datotekom

*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Levim dugmetom miša otvorite datoteku `setup` (u mom primeru je `BCUninstaller_5.9.0_setup.exe`)" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcu_-_file_setup_5.9_mouse_hover.jpeg" title="Setup za instalaciju" >}}

  Ako se Microsoft Defender SmartScreen obaveštenje pokaže, levim dugmetom miša prvo kliknite `Više informacija` i posle kliknite `Ipak pokreni`.

  {{< figure align=center src="/images/bcu/bcu_-_fajl_setup_-_win11sr_smartscreen_-_vise_informacija_btn.jpeg" title="Dugme: Više informacija" >}}
  {{< figure align=center src="/images/bcu/bcu_-_fajl_setup_-_win11sr_smartscreen_-_ipak_pokreni_btn.jpeg" title="Dugme: Ipak pokreni" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Levim dugmetom miša kliknite dugme `OK`, opcijsko možete promenite jezik sa levim dugmetom miša" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_1_-_language_-_ok_btn.jpeg" title="Jezik instalacije" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Levim dugmetom miša kliknite u krugič polje za potvrdu `I accept the licence agreement` da izberete i onda kliknete dugme `Next`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_2_-_license_-_next_btn.jpeg" title="Program license agreement" >}}

  Možete pročitati ugovor o licenci ako želite.

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Levim dugmetom miša kliknite na dugme `Next`, opcijsko možete promeniti fasciklu instalacije sa klikom levog dugmeta miša na dugme `Browse`" openByDefault=true >}}

  Ako kliknete dugme `Browse` u novom prozoru levim dugmetom miša kliknite na željenu fasciklu i potvrdite sa dugmetom `U redu`.

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_3_-_destination_-_next_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Levim dugmetom miša kliknite na dugme `Next`, opcijsko možete čekirati/odčekirati polja za potvrdu sa levim dugmetom miša za komponente" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_4_-_components_-_next_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Levim dugmetom miša kliknite na dugme `Next`, opcijsko možete da promenite ime i lokaciju u Start meniju sa klikom levog dugmeta miša na dugme `Browse` ili ga uopšte ne napraviti" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_5_-_start_menu_shortcut_-_next_btn.jpeg" >}}

  Ako ne želite prečicu u Start meniju, levim dugmetom miša kliknite na polje za potvrdu pored `Don't create Start Menu folder`!

{{< /collapse >}}

{{< collapse summary="**Korak 7:** Levim dugmetom miša kliknite na dugme `Next`, opcijski ako je polje za potvrdu pored `Create a desktop shortcut` označeno, prečica BCU če se napravi na radnoj površini Windows" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_6_-_win_desktop_shortcut_-_next_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 8:** Proverite vaša podešavanja i onda sa levim dugmetom miša kliknite na dugme `Install`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_7_-_ready_to_install_-_install_btn.jpeg" >}}

  Ako sa levim dugmetom miša kliknite na dugme `Back` možete da promenite pre definisana podešavanja ovog prozora instalacije.

{{< /collapse >}}

{{< collapse summary="**Korak 9:** Levim dugmetom miša kliknite na dugme `Finish`, opcijski ako je polje za potvrdu čekirano pored `Launch BCUninstaller` BCU program če se pokrene kad završite instalaciju sa klikom levog dugmeta miša na dugme `Finish`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_setup_-_8_-_finished_-_finish_next_btn.jpeg">}}

  Ukoliko ste izabrali da se BCU otvori nakon završetka instalacije, možda će da vidite obaveštenje `Kontrola koristničkog naloga` ako želite da otvorite `BCUninstaller.exe` samo sa levim dugmetom miša kliknite dugme `Da` na potvrdite.

  {{< figure align=center src="/images/bcu/bcu_-_bcuninstaller_exe_-_win11sr_UAC_-_da_btn.jpeg" >}}

{{< /collapse >}}

## Prenosiva verzija BCU - odpakiranje i pokretanje

*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Otvorite fasciklu sa prethodno preuzetu arhivnu portable datoteku" openByDefault=true >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2** Desnim dugmetom miša kliknite na arhivnu portable datoteku (u mom primeru je `BCUninstaller_5.9.0_portable.zip`) i onda levim dugmetom miša kliknite na `Izdvoji sve...`" openByDefault=true >}}

  Može otpakirate sa arhivnim programom kao [7zip](https://www.7-zip.org/ "Kliknite/tapnite, da otvorite stranicu!"), [WinRAR](https://www.win-rar.com/ "Kliknite/tapnite, da otvorite stranicu!"), ... ali za ovaj tutorijal koristim integrisani program za raspakivanje arhiva iz sistema Windows 11 (takođe dostupan u sistemu Windows 10). 

  {{< figure align=center src="/images/bcu/bcu_-_fajl_portable_5.9_-_win11sr_izdvoji_sve_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Levim dugmetom miša kliknite na dugme `Izdvoji` i sačekajte, da se otpakira, opcijski možete levim dugmetom miša kliknite na dugme `Potraži`" openByDefault=true >}}

  Ako je označeno polje za potvrdu pored `Show extracted folder when completed` kad otpakiranje je završeno, otvori če se Windows meneđer datoteka u otpakirani fascikli.

  {{< figure align=center src="/images/bcu/bcu_-_fajl_portable_5.9_-_win11sr_izdvoji_prozor_-_izdvoji_btn.jpeg" >}}

  Ako kliknete dugme `Potraži` u novom prozoru levim dugmetom miša kliknite na željenu fasciklu i potvrdite sa dugmetom `U redu`.

{{< /collapse >}}

{{< collapse summary="**Korak 4:** U otpakirani fascikli levim dugmetom miša kliknite na `BCUninstaller.exe`, da ga otvorite" openByDefault=true >}}

  `.exe` extension may be shown or not, it depends on your Windows settings. 

  {{< figure align=center src="/images/bcu/bcu_-_file_portable_5.9_-_win11en_extracted_BCUninstaller.exe_hover.jpeg" >}}

  Ako vas `Kontrola koristničkog naloga` pita dali želite da otvorite `BCUninstaller.exe` samo sa levim dugmetom miša kliknite na dugme `Da` da potvrdite.

  {{< figure align=center src="/images/bcu/bcu_-_bcuninstaller_exe_-_win11sr_UAC_-_da_btn.jpeg" >}}

  Sad može koristite program BCU.

{{< /collapse >}}

## Prvo pokretanje BCU i prva podešavanja

Svaki put kada se BCU otvori skeniraće vaš sistem u potrazi za deinstalaterskim programima kako bi ih prikazao na listi. Kada se BCU prvi put otvori proći će kroz početna podešavanja (ispod).

{{< notice tip >}}
  Jer program nije u našim jezicima koristim engleski jezik za ovaj tutorijal.
{{< /notice >}}

{{< figure align=center src="/images/bcu/bcuen_-_window_-_scanning.jpeg" >}}

*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Levim dugmetom miša kliknite na dugme `Continue`, opcijski možete promenite jezik programa levim dugmetom miša" openByDefault=true >}}

  Ako želite, da promenite jezik levim dugmetom miša kliknite na dugme `Default`, izaberite jezik i onda kliknete na dugme `Apply`, da potvrdite odabir.

  {{< figure align=center src="/images/bcu/bcuen_-_welcome_settings_-_1_-_language_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Podesite opcije izgleda spiska deinstalatera i onda levim dugmetom miša kliknite na dugme `Continue`" openByDefault=true >}}

  Levim dugmetom miša kliknite na polja za potvrdu da izaberete/uklonite izbor mogučnosti:

  - `Show uninstallers in groups` Deinstalatori če budu grupirani po prvom znaku njihohog naziva.
  - `Select using checkboxes` Ako želite mogučnost deinstalacije više programa od jedamput ali ja preferiram jedan po jedan program.
  - `Highlight certified uninstallers` Označite deinstalatere sertifikovane od strane nadležnih organa.

  {{< figure align=center src="/images/bcu/bcuen_-_welcome_settings_-_2_-_list_view_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Pustite polja za potvrdu neoznačene i levim dugmetom miša kliknite na dugme `Continue` ali ako se napredni koristnik odaberite šta želite" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_welcome_settings_-_3_-_advanced_users_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Sa levim dugmetom miša odaberite željene opcije i onda kliknite na dugme `Continue`" openByDefault=true >}}

  Levim dugmetom miša kliknite na polja za potvrdu da izaberete/uklonite izbor mogučnosti:

  - `Higlight invalid uninstallers` Da se označe oštečeni deinstalateri.
  - `Show unregistered applications in the list` Da se pokažu programi neregistrovani u Windows ali verovatno su deo nekog drugog programa.

  {{< figure align=center src="/images/bcu/bcuen_-_welcome_settings_-_4_-_corrupted_uninstallers_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Levim dugmetom miša odaberite željene opcije i onda kliknete na dugme `Continue`" openByDefault=true >}}

  Levim dugmetom miša kliknite na polja za potvrdu da izaberete/uklonite izbor mogučnosti:

  - `Automatically look for updates on aplication start` Uz svako pokretanje programa BCU automatski proveri na internetu ako postoji nova verzija.
  - `Automatically send anonymous usage statistics` Ako želite da pošaljete statistike korištenja proizvođaču programa anonimno.
  - `Enable user ratings of aplications` Korisno je da se utvrdi, da li je program u dobrom ili lošem stanju. Mislim da ako nema ocene za program BCU će dati mu jednu zvezdicu.

  {{< figure align=center src="/images/bcu/bcuen_-_welcome_settings_-_5_-_network_access_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Za završetak instalacije levim dugmetom miša kliknite na dugme `Finish setup`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_welcome_settings_-_6_-_setup_finished_-_finish_setup_btn.jpeg" >}}

{{< /collapse >}}

## Deinstalacija programa sa BCU

Ja koristim `VLC media player` za deinstalaciju.

*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** Desnim dugmetom miša kliknete na željen program za deinstalaciju i onda sa levim dugmetom miša kliknite na dugme `Uninstall`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_1_-_vlc_-_uninstall_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Odaberite željene opcije i onda sa levim dugmetom miša kliknite na dugme `Continue`" openByDefault=true >}}

  Levim dugmetom miša kliknite na polja za potvrdu da izaberete/uklonite izbor mogučnosti:

  - `Uninstall` Ako želite da deinstalirate željeni program pomoću njegovog zvaničnog programa za deinstalaciju.
  - `Quiet` Deinstalirajte program bez ikakvog korisničkog unosa zvaničnog programa za deinstalaciju.

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_2_-_confirm_vlc_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Ako BCU detektuje deinstalacijski program ili program povezan sa njim pokrenut, BCU će prikazati ovaj korak za zaustavljanje programa, u suprotnom će preskoči na sledeći korak" openByDefault=true >}}

  Levim dugmetom miša kliknite na program sa liste i onda kliknite dugme `Kill` (Zaustavi), da zaustavite program, da više nije pokrenut. Ako je na spisku više kao jedan program, možete levim dugmetom miša da kliknete dugme `Kill all` (Zaustavi sve). Kad je program zaustavljen levim dugmetom miša kliknite na dugme `Continue`. 

  {{< figure align=center src="/images/bcu/bcusr_-_deinstaliraj_program_-_3a_-_zatvori_vlc_-_kill_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Levim dugmetom miša kliknite na dugme `Continue`, opcijski možete odaberete željene opcije ali u redu su originalna podešavanja" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_4_-_settings_-_continue_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Levim dugmetom miša kliknite na dugme `BEGIN UNINSTALLATION` za početak deinstalacije" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_5_-_vlc_-_begin_uninstallation_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Deinstalirajte program pomoću zvaničnog programa za deinstalaciju (levo na slici) dok BCU prozor čeka u pozadini da se završi" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_6_-_vlc_uninstaller_start_-_ok_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 7:** Kad završi deinstalacija levim dugmetom miša kliknite na dugme `Close`" openByDefault=true >}}

  Kada se deinstalacija završi u BCU prozoru ćete videti potvrdu. U nekim slučajevima neki programi za deinstalaciju će otvoriti neku vrstu prozora poput veb stranice, zatvorite taj prozor ili prozore da bi se nastavilo sa levim dugmetom miša kliknite na dugme `Close`.

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_7_-_bcu_detected_vlc_finished_-_close_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 8:** Levim dugmetom miša kliknite na dugme `Da` ili `Yes` da potražite ostatke i sačekajte do kraja traženja" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_8_-_ask_leftovers_-_yes_btn.jpeg" >}}
  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_9_-_searching_for_leftovers.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 9:** Sa levim dugmetom miša odaberite željene opcije i onda kliknite na dugme `Delete selected` za brisanje odabranog, ali takođe možete koristiti padajući meni za poverenje (confidence)..." openByDefault=true >}}

  Levim dugmetom miša može kliknete na dugme `Delete selected` ali može napravite nekoliko stvari:

  - Čekirano polje za potvrdu znači brisanje tog ostatka inače pa neče.
  - Možete odabrati različite nivoe pouzdanosti `Dobro` (Good) ili `Vrlo dobro` (Very good) su u skoro svim slučajevima dozvoljeni za brisanje dok sa `Sumnjivo` (`Questionable`) ili `Loše` (`Bad`) budite oprezni. Svi rezultati ispod izabranog nivoa pouzdanosti biće ignorisani. Moguće je da nijedan ostatak neče ostane. Ako odaberete `Loše` (`Bad`), dobićete obaveštenje ako zaista želite da ih prikažete jer to može biti opasno! Da potvrdite kliknite levim dugmetom miša na `Da` (`Yes`)

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_10c_-_leftovers_vlc_-_delete_selected_btn.jpeg" title="Lista ostatka" >}}
  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_10a_-_leftovers_vlc_-_confidence_-_bad_sel.jpeg" title="Nivoji pouzdanosti" >}}
  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_10b_-_leftovers_vlc_-_confidence_-_bad_-_yes_btn.jpeg" title="Obaveštenje loše pouzdanosti" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 10:** Ako postoje ostaci registra, BCU će vas pita ako želite da napravite rezervnu kopiju tih unosa u registru. Levim dugmetom miša kliknite na dugme `Create`, odaberite fasciklu, gde želite da sačuvate arhivu sa levim dugmetom miša i onda kliknite levim dugmetom miša na dugme `Izaberite fasciklu`" openByDefault=true >}}

  I used Windows Desktop for registry leftovers backup in this tutorial.

  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_10d_-_leftovers_vlc_-_removal_reg_backup_-_create_btn.jpeg" >}}
  {{< figure align=center src="/images/bcu/bcuen_-_uninstall_progam_-_10e_-_leftovers_vlc_-_reg_backup_-_win11sr_-_izaberite_fasciklu_btn.jpeg" title="Odaberite gde da sačuvate registar ostatke" >}}
  
  Sada je program i njegovi tragovi izbrisani.

{{< /collapse >}}

## Nekoliko BCU elementa

*(Kliknite na pojedinačni korak ili trougao da bi sakrili ili prikazali detalje (slike, informacije, ...))*

{{< collapse summary="**BCU interfejs**" openByDefault=false >}}

  {{< figure align=center src="/images/bcu/bcuen_-_window_-_left_quick_select_settings.jpeg" title="Brza podešavanja levo" >}}
  {{< figure align=center src="/images/bcu/bcuen_-_window_-_main_menu.jpeg" title="Glavan meni na vrhu" >}}

{{< /collapse >}}

{{< collapse summary="**Osvežite listu deinstalatera** ručno" openByDefault=false >}}

   {{< figure align=center src="/images/bcu/bcuen_-_main_menu_file__-_reload_uninstallers_btn.jpeg" title="Osvežite listu deinstalatera" >}}
   {{< figure align=center src="/images/bcu/bcuen_-_window_-_scanning.jpeg" title="Skeniranje sistema za programe" >}}

{{< /collapse >}}

{{< collapse summary="**Alat: Meneđer pokretanja (Startup manager)** za Windows" openByDefault=false >}}

   {{< figure align=center src="/images/bcu/bcuen_-_main_menu_tools_-_open_startup_manager_btn.jpeg" title="Otvaranje meneđera" >}}
   {{< figure align=center src="/images/bcu/bcuen_-_startup_manager_yes_-_enabled_btn.jpeg" title="Onemogučite pokretanje sa Windows-om" >}}
   {{< figure align=center src="/images/bcu/bcuen_-_startup_manager_no_-_enabled_btn.jpeg" title="Omogučite pokretanje sa Windows-om" >}}

{{< /collapse >}}

## Linkovi

[Bulk Crap Uninstaller veb-sajt](https://www.bcuninstaller.com/ "Kliknite/tapnite, da otvorite stranicu!")

## Video verzija

*PREMIERA (24.08.2025, 18:00 / 06:00 PM, vremenska zona: CEST / UTC+2 / GMT+2)*

{{< youtube "i3CGzkc9JUQ" >}}