---
title: "Kako namestiti in uporabiti Bulk Crap Uninstaller (osnove)"
date: 2025-08-22T00:00:00+02:00
# publishDate: 2025-08-08T22:00:40+02:00
url: /bcu-sl/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - kako
tags: 
  - Windows
  - Bulk Crap Uninstaller
showtoc: true  # Seznam vsebine: Skriti (false) ali prikazati (true)
draft: false  # Prikaz na javni strani: Prikaz (false) ali skriti (true)
language: "Slovenski"
---

[Bulk Crap Uninstaller](https://www.bcuninstaller.com/ "Kliknite/tapnite, da odprete spletno stran!") (tudi poznan kot BCUninstaller ali kratko BCU) je brezplačen odprtokodni program za izbris programov za [Windows](https://www.microsoft.com/sl-si/windows "Kliknite/tapnite, da odprete spletno stran!") operacijski sistem, pravtako je možen prenos programa za operacijske sisteme [Linux](https://www.linux.org/ "Kliknite/tapnite, da odprete spletno stran!"), [Mac](https://www.apple.com/si/mac/ "Kliknite/tapnite, da odprete spletno stran!"), ... in kot kateri koli drug odstranjevalec ([Revo Uninstaller](https://www.revouninstaller.com/ "Kliknite/tapnite, da odprete spletno stran!"), [GEEK UNINSTALLER](https://geekuninstaller.com/ "Kliknite/tapnite, da odprete spletno stran!"), [IObit Uninstaller](https://www.iobit.com/en/advanceduninstaller.php "Kliknite/tapnite, da odprete spletno stran!"), [Uninstalr](https://uninstalr.com/ "Kliknite/tapnite, da odprete spletno stran!") in drugi) poiskušajo odstraniti ostanke (datoteke, mape ter vnose v register), ki jih je odstranjeni program (z njegovim uradnim odstranjevalcom), pustil za seboj. BCU ima veliko možnosti in vas vodi skozi vsak korak. Noben program za odstranjevanje ne bo vsakič izbrisal vsake sledi zaradi različnih imen map itd..

{{< notice warning >}}
  V redkih primerih (majhna verjetnost) lahko ostanki programa za odstranitev vsebujejo neželene elemente, ki lahko ob izbrisu povzročijo težave v sistemu. Noben program za odstranitev ni popoln in ne odgovarjam za morebitno škodo! Če kaj ne deluje več pravilno pojdite na komentarje videoposnetkov na YouTubu in napišite svoje vprašanje.
{{< /notice >}}

{{< notice note >}}
  Ta vodič je bil narejen na Windows 11 24H2 64-bit
{{< /notice >}}

## Namestitev BCU s winget

{{< notice info >}}
  V primeru da nimate WINGET ali pa ste prejeli neko drugo napako v oknu instalacije programa ga namestite na [ročni način](#namestite-bulk-crap-uninstaller-ročno-s-prej-presneto-datoteko "Kliknite/tapnite da posetite sekciju!").
{{< /notice >}}

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** Z desno miškino tipko kliknite na tipko `Start` menija in nato s levo miškino tipko kliknite na `Windows PowerShell` ali `Terminal` kot Administrator" openByDefault=true >}}

  {{< figure align=center src="/images/other/win10/Win10sl_-_start_btn.jpeg" title="Windows 10 Start" >}}
  {{< figure align=center src="/images/other/win11/Win11sl_-_start_btn_zacetek.jpeg" title="Windows 11 Start" >}}
  {{< figure align=center src="/images/other/win10/Win10sl_-_start_btn_-_windows_powershell_skrbnik_btn.jpeg" >}}
  {{< figure align=center src="/images/other/win11/Win11sl_-_start_btn_-_terminal_windows_skrbnik_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** V novem oknu napišite winget komando (poglejte malo niže) in nato pritisnite tipko `Enter` na tipkovnici za namestitev BCU" openByDefault=true >}}

  Winget komanda:

    winget install -e --id Klocman.BulkCrapUninstaller

  `Enter` tipka na tipkovnici:

  {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
  {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}

  Vodič o `Winget` bom naredil v prihodnosti!

  V prihodnosti planiram narediti `Winget` vodič.

{{< /collapse >}}

## Prenos namestitvene in prenosne različice Bulk Crap Uninstaller 

{{< notice tip >}}
  Setup datoteka je namenjena namestitvi BCU programa medtem ko portable datoteka ne in je samo zagnate. Prenosno različico samo presnamete, odpakirate s arhivnim programom kot je [7zip](https://www.7-zip.org/ "Kliknite/tapnite, da odprete spletno stran!") ali integriranega v Windows 10 in 11 (preverite [prenosni odsek](#portable-bcu-unpack-and-run "Kliknite/tapnite za obisk odseka!")] kako ga odpakirati in zagnati) in ga zaženete. 
{{< /notice >}}

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** Z levo miškino tipko odprite željen spletni brskalnik in obiščite BCU spletno stran" openByDefault=true >}}

  V URL oz. naslovno polje želenega spletnega brskalnika (Google Chrome, Mozilla Firefox, Brave, ...) vnesite ali kopirajte in prilepite naslov spletne strani BCU in pritisnite tipko Enter na tipkovnici.

  Če je v polju URL že obstoječi spletni naslov kliknite z levo miškino tipko v prazno območje URL za izbor trenutnega naslova in začnete tipkati svoj naslov. Če je območje URL prazno, lahko preprosto kliknete z levo tipko miške nekam v notranjost in začnete pisati.
  
  BCU spletna stran:

    https://www.bcuninstaller.com/

  Naslovno polje oz. URL za spletno stran:

  {{< figure align=center src="/images/Mozilla-Firefox/mfirefoxsl_-_url_area.jpeg" title="Naslovno polje oz. URL" >}}

  Tipka Enter na tipkovnici:

  {{< figure align=center src="/images/other/Keyboard_-_enter_l.jpeg" >}}
  {{< figure align=center src="/images/other/Keyboard_-_enter_r.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Na spletni strani BCU z levo miškino tipko kliknite zeleno tipko `Download on dAppCDN` ali `Download on SourceForge` za prenos programa" openByDefault=true >}}

  Lahko presnamete s `dAppCDN` ali `SourceForge`. Za ta vodič sem izbral `SourceForge`.

  {{< figure align=center src="/images/bcu/bcu_-_website_download_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Z levo miškino tipko kliknite na `Files`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcu_-_website_download_-_files.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Z levo miškino tipko kliknite na najnovejšo različico" openByDefault=true >}}

  Ob izdelavi tega vodiča je najnovejša različica `v5.9`.

  {{< figure align=center src="/images/bcu/bcu_-_website_download_-_files_-_ver5.9.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Z levo miškino tipko kliknite kaj želite prenesti in počakajte, da se presname" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcu_-_website_download_-_files_-_ver5.9_-_setup.jpeg" title="Setup/installation" >}}
  {{< figure align=center src="/images/bcu/bcu_-_website_download_-_files_-_ver5.9_-_portable.jpeg" title="Portable" >}}

{{< /collapse >}}


## Namestite Bulk Crap Uninstaller ročno s prej presneto datoteko

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** Z levo miškino tipko odprite setup datoteko (v mojem primeru je `BCUninstaller_5.9.0_setup.exe`)" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcu_-_file_setup_5.9_mouse_hover.jpeg" title="Setup for the installation" >}}

  Če se prikaže okno za obveščanje o Microsoft Defender SmartScreen z levo miškino tipko kliknite na `Več informacij` in nato kliknite `Vseeno zaženi`.

  {{< figure align=center src="/images/bcu/bcu_-_fajl_setup_-_win11sl_smartscreen_-_vec_informacij_btn.jpeg" title="Tipka: Več informacij" >}}
  {{< figure align=center src="/images/bcu/bcu_-_fajl_setup_-_win11sl_smartscreen_-_vseeno_zazeni_btn.jpeg" title="Tipka: Vseeno zaženi" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Z levo miškino tipko kliknite na tipko `V redu` in po želji lahko spremenite namestitveni jezik z levo miškino tipko" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_namestitev_-_1_-_jezik_-_v_redu_btn.jpeg" title="Setup language" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Z levo miškino tipko kliknite na krogec potrditveno polje `Da, sprejemam vse pogoje licenčne pogodbe` za izbor in nato kliknite na tipko `Naprej`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_namestitev_-_2_-_licenca_-_da_sprejemam.jpeg" title="Program license agreement" >}}

  Če želite si lahko preberete licenčno pogodbo.

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Z levo miškino tipko kliknite na tipko `Naprej`,opcijsko lahko spremenite kam da se program namesti z klikom leve miškine tipke na tipko `Prebrskaj...`" openByDefault=true >}}

  Če kliknete tipko `Prebrskaj...` v novem oknu s levo miškino tipko kliknite na željeno mapo in nato kliknete tipko `V redu`.

  {{< figure align=center src="/images/bcu/bcusl_-_namestitev_-_3_-_destinacija_-_naprej_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Z levo miškino tipko kliknite na tipko `Naprej`, po želji lahko označite/odznačite potrditvena polja za komponente z levo miškino tipko" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_namestitev_-_4_-_izbira_komponent_-_naprej_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Z levo miškino tipko kliknite na tipko `Naprej`, opcijsko lahko spremenite ime in lokacijo za v Start meni s klikom na tipko `Prebrskaj...` z levo miškino tipko ali pa mape sploh ne izdelamo" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_namestitev_-_5_-_start_menu_bljiznica_-_naprej_btn.jpeg" >}}

  `Ne ustvari mapo v meniju Start` Če mape ne želite, z levo miškino tipko kliknite na potrditveno polje za izbor!

{{< /collapse >}}

{{< collapse summary="**Korak 7:** Z levo miškino tipko kliknite na tipko `Naprej`, opcionalno lahko označite potrditveno polje zraven `Ustvarite ikono na namizju` da bo bljižnica BCU narejena na namizju Windows-a" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_namestitev_-_6_-_win_namizje_bljiznica_-_naprej_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 8:** Preverite svoje nastavitve in nato z levo miškino tipko kliknite na tipko `Namesti`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_namestitev_-_7_-_pripravljen_za_namestitev_-_namesti_btn.jpeg" >}}

 Če z levo miškino tipko kliknete tipko `Nazaj`, lahko spremenite predhodno definirane nastavitve v tem namestitvenem oknu.

{{< /collapse >}}

{{< collapse summary="**Korak 9:** Z levo miškino tipko kliknite na tipko `Končaj`, opcionalno, če je potrditveno polje zraven `Odpri BCUninstaller` označeno, BCU program se bo odprl po kliku leve miškine tipke na tipko `Končaj`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_namestitev_-_8_-_koncano_-_koncaj_btn.jpeg">}}

  Če ste označili zagon programa BCU po končani namestitvi in dobite varnostno opozorilo `Nadzor uporabniškega računa` samo kar s levo miškino tipko kliknite na tipko `Da` za potrditev zagona.

  {{< figure align=center src="/images/bcu/bcu_-_bcuninstaller_exe_-_win11sl_UAC_-_da_btn.jpeg" >}}

{{< /collapse >}}

## Prenosna različica BCU - odpakiranje in zagon

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** Odprite mapo, kjer se nahaja prej presneta portable arhivna datoteka" openByDefault=true >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2** Da odpakirate z desno miškino tipko kliknite na portable arhivno datoteko (v mojem primeru je `BCUninstaller_5.9.0_portable.zip`) jn nato z levo miškino tipko kliknite na `Ekstrahiraj vse...`" openByDefault=true >}}

  Lahko odpakirate arhivno datoteko s programom kot [7zip](https://www.7-zip.org/ "Kliknite/tapnite, da odprete spletno stran!"), [WinRAR](https://www.win-rar.com/ "Kliknite/tapnite, da odprete spletno stran!"), ... ampak za tale vodič bom uporabil integriran arhivski ekstraktor integriran v Windows 11 (je tudi na voljo v Windows 10). 

  {{< figure align=center src="/images/bcu/bcu_-_fajl_portable_5.9_-_win11sl_-_ekstrahiraj_vse_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Z levo miškino tipko kliknite na tipko `Ekstrahiraj` in počakajte, da bo odpakirano, opcionalno lahko spremenite kam se bo odpakiralo z klikom leve miškine tipke na tipko `Prebrskaj ...`" openByDefault=true >}}

  Če je zraven `Na koncu pokaži ekstrahirane datoteke` potrditveno polje izbrano se bo po končanem odpakiranju prikazal raziskovalec v odpakirani mapi.

  {{< figure align=center src="/images/bcu/bcu_-_fajl_portable_5.9_-_win11sl_-_ekstrahiraj_okno_-_ekstrahiraj_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** V odpakirani mapi z levo miškino tipko odprite `BCUninstaller.exe` za zagon programa" openByDefault=true >}}

  `.exe` datotečna končnica je lahko prikazana ali ne je odvisno od vaših nastavitev Windows-a. 

  {{< figure align=center src="/images/bcu/bcu_-_fajl_portable_5.9_-_win11sl_odpakirano_BCUninstaller.exe_hover.jpeg" >}}

  Če vas `Nadzor uporabniškega računa` vpraša, če želite zagnati`BCUninstaller.exe` kar z levo miškino tipko kliknite na tipko `Da` da potrdite.

  {{< figure align=center src="/images/bcu/bcu_-_bcuninstaller_exe_-_win11sl_UAC_-_da_btn.jpeg" >}}

  Zdaj lahko začnete uporabljati BCU.

{{< /collapse >}}

## BCU prvi zagon in prvotne nastavitve

Vsakič, ko se BCU odpre bo skeniral vaš sistem za programe v vašem sistemu in dodal v seznam BCU. Ko se BCU prvič odpre greste skozi začetne nastavitve (spodaj).

{{< figure align=center src="/images/bcu/bcusl_-_okno_-_skeniranje.jpeg" >}}

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** Z levo miškino tipko kliknite na tipko `Nadaljuj`, opcionalno lahko spremenite jezik programa s levo miškino tipko" openByDefault=true >}}

  Če želite spremeniti jezik programa z levo miškino tipko kliknite na tipko `Privzeto` in kliknite na željeni jezik z levo miškino tipko in nato kliknite na tipko `Uporabi` za potrditev izbire.

  {{< figure align=center src="/images/bcu/bcusl_-_dobrodosli_nastavitve_-_1_-_jezik_-_nadaljuj_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Nastavite si opcije prikaza seznama in nato z levo miškino tipko kliknite na tipko `Nadaljuj`" openByDefault=true >}}

  Z levo miškino tipko kliknite potrditvena polja da označite/odznačite željene opcije:

  - `Prikaži odstranjevalce v skupinah` Odstranjevalci bodo grupirani po prvem znaku naziva programa.
  - `Izberi s pomočjo potrditvenih polj` Če želite naenkrat odstraniti več programov naenkrat vendar raje odmešščam en program na enkrat, tako da sem odznačil.
  - `Označi overjene odstranjevalce` Označiti overjene odstranjevalce verificirani s strani pomembnih organov.

  {{< figure align=center src="/images/bcu/bcusl_-_dobrodosli_nastavitve_-_2_-_seznam_odstranjevalcev_-_nadaljuj_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** Pustite odznačena potrditvena polja in z levo miškino tipko kliknite na tipko `Nadaljuj`, če pa ste napreden uporabnik, pa označite kaj želite" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_dobrodosli_nastavitve_-_3_-_napredni_uporabniki_-_nadaljuj_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Z desno miškino tipko označite željene opcije in kliknite na tipko `Nadaljuj`" openByDefault=true >}}

  Z levo miškino tipko označite/odznačite željene opcije:

  - `Označi neveljavne odstranjevalce` označiti poškodovane/neveljavne odstranjalce.
  - `Prikaži neregistrirano aplikacije na seznamu` Prikaz programov neregistrirani v sistemu Windows, vendar je del glavnega programa.

  {{< figure align=center src="/images/bcu/bcusl_-_dobrodosli_nastavitve_-_4_-_poskodovani_odstr_-_nadaljuj_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Z levo miškino tipko označite/odznačite opcije in nato kliknite na tipko `Nadaljuj`" openByDefault=true >}}

  Z levo miškino tipko kliknite označite/odznačite potrditvena polja naslednjih opcij:

  - `Ob zagonu aplikacije, samodejno preveri obstoj posodobitev` Vsakič ko se BCU odpre preveri če obstajajo posodobitve programa.
  - `Samodejno pošlji anonimno statistiko` Če BCU dovolite, da pošlje statistiko uporabe lastniku programa.
  - `Omogoči uporabnikovo ocenjevanje aplikacije` Uporabno je vedeti ali je program na dobrem ali slabem stanju. Mislim, da če program ni ocenjen BCU ga bo označil kot eno zvezdico.

  {{< figure align=center src="/images/bcu/bcusl_-_dobrodosli_nastavitve_-_5_-_omrezni_dostop_-_nadaljuj_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Za zaključitev nastavitev z levo miškino tipko kliknite na tipko `Končaj namestitev`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_dobrodosli_nastavitve_-_6_-_namestitev_koncana_-_koncaj_namestitev_btn.jpeg" >}}

{{< /collapse >}}

## Odstranjevanje programa s BCU

Za izbris bom uporabil  `VLC media player`.

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** Z desno miškino tipko kliknite na program, ki želite odstraniti nato pa z levo miškino tipko kliknite na tipko `Odstrani`" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_1_-_vlc_-_odstrani_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** Označite svoje opcije in nato z levo miškino tipko kliknite na tipko `Nadaljuj`" openByDefault=true >}}

  Z levo miškino tipko kliknite označite/odznačite potrditvena polja naslednjih opcij:

  - `Odstrani` Če želite odstranitev programa s njegovim uradim odstranjevalcem.
  - `Tiho` Odstraniti program brez uporabniškega vnosa uradnega odstranjevalca.

  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_2_-_potrdite_vlc_-_nadaljuj_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** If BCU detects uninstaling program or program connected to it is running BCU will whow this step to stop the program othervise will jump to next step" openByDefault=true >}}

  Z levo miškino tipko kliknite na program na seznamu in kliknite tipko `Uniči`. V primeru, da je več programov na spisku lahko vse na enkrat zaprete s klikom leve miškine tipke na tipko `Uniči vse`. Ko je program zaprt z levo miškino tipko kliknite na tipko `Nadaljuj`.

  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_3a_-_zapri_vlc_-_unici_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** Z levo miškino tipko kliknite na tipko `Nadaljuj`, opcionalno lahko označite/odznačite opcije ampak lahko pustite označeno kot je privzetoy" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_4_-_nastavitve_odstranitve_-_nadaljuj_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** Z levo miškino tipko kliknite na tipko `ZAČETEK ODSTRANITVE` za začetek odstranitve programa" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_5_-_vlc_-_zacetek_odstranitve_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 6:** Tukaj prvo odstranite s uradnim odstranjevalcom (kot na sliki levo) dokler BCU okno (desno na sliki) čaka v ozadju za zaključek" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_6_-_vlc_odstranjevalec_-_naprej_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 7:** Na koncu odstranitve z levo miškino tipko kliknite na tipko `Zapri`" openByDefault=true >}}

  Ko je odstranitev končana BCU bo prikazal kljukico. V nekaterih primerih bodo nekateri odstranjevalci odprli nekakšno okno kot je spletna stran, zaprite to okno ali okna in nato kliknete tipko `Zapri` z levo miškino tipko.

  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_7_-_bcu_ugotovil_vlc_koncal_-_zapri_btn.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 8:** Z levo miškino tipko kliknite na tipko `Da` za iskanje ostankov in počakajte, da je iskanje dokončano" openByDefault=true >}}

  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_8_-_vprasa_za_iskanje_ostankov_-_da_btn.jpeg" >}}
  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_9_-_iskanje_ostankov.jpeg" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 9:** Z desno miškino tipko označite elemente za odstranitev in nato kliknite tipko `Izbriši izbrano`, lahko pa tudi izberete drugi nivo zaupanja spodaj..." openByDefault=true >}}

  Z levo miškino tipko kliknite tipko `Izbriši izbrano` ampak pred tem lahko naredite nekaj zadev:

  - Ostanki s označenm potrditvenim poljem bodo izbrisani mednem neoznačeni pa nebodo.
  - Izberete lahko različne stopnje zaupanja, `Dobro` in `Zelo dobro` so v skoraj vseh primerih v redu za izbris, medtem ko pri `Vprašljivo` ali `Slabo` bodite previdni! Vsi rezultati nižje stopnje zaupanja od izbrane so prezrti.Možnost je, da ostankov sploh ne bo v vašem primeru.Če izberete `Slabo` boste dobili obvestilo, če jih resnično želite pokazati, ker je lahko nevarno! Da potrdite z levo miškino tipko kliknite na tipko `Da`.

  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_10c_-_ostanki_vlc_-_izbrisi_izbrano_btn_window.jpeg" title="Seznam ostankov" >}}
  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_10a_-_ostanki_vlc_-_zaupanje_izbira_-_slabo_btn.jpeg" title="Nivoji zaupanja" >}}
  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_10b_-_ostanki_vlc_-_zaupanje_izbira_-_slabo_-_da_btn.jpeg" title="Obvestilo izbire slabega nivoja zaupanja" >}}

{{< /collapse >}}

{{< collapse summary="**Korak 10:** Če obstajajo registrski ostanki, BCU vas bo vprašal ali želite ustvariti varnostno kopijo teh vnosov v registru. Z levo miškino tipko kliknite na tipko `Ustvari`, Z levo miškino tipko izberite mapo za shraniti varnostno kopijo in nato kliknite tipko `Izberite mapo`" openByDefault=true >}}

  V tem vodiču sem uporabil sem namizje, da shranim kopijo registrskih ostankov.

  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_10d_-_ostanki_vlc_-_reg_varn_kopija_-_ustvari_btn.jpeg" >}}
  {{< figure align=center src="/images/bcu/bcusl_-_odstrani_program_-_10e_-_ostanki_vlc_-_reg_varn_kopija_-_win11sl_-_izberite_mapo.jpeg" title="Izberite mapo, kam shraniti arhiv registrkih ostankov" >}}
  
  Sedaj bi moral program in njeni ostanki izbrisani.

{{< /collapse >}}

## Nekaj elementov BCU

*(Kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**BCU glavno okno**" openByDefault=false >}}

  {{< figure align=center src="/images/bcu/bcusl_-_okno_-_hitre_nastavitve_levo.jpeg" title="Hitre nastavitve levo" >}}
  {{< figure align=center src="/images/bcu/bcusl_-_okno_-_glaven_meni.jpeg" title="Glaven meni na vrhu" >}}

{{< /collapse >}}

{{< collapse summary="**Znova skenirati sistem za programi** manually" openByDefault=false >}}

   {{< figure align=center src="/images/bcu/bcusl_-_glaven_meni_datoteka_-_znova_nalozi_odstr_btn.jpeg" title="Ponovno skeniranje odstranjevalcev" >}}
   {{< figure align=center src="/images/bcu/bcusl_-_okno_-_skeniranje.jpeg" title="Skeniranje za odstranjevalce" >}}

{{< /collapse >}}

{{< collapse summary="**Orodje: Upravitelj zagona** za Windows" openByDefault=false >}}

   {{< figure align=center src="/images/bcu/bcusl_-_glaven_meni_orodja_-_odpri_upravitelja_zagona_btn.jpeg" title="" >}}
   {{< figure align=center src="/images/bcu/bcusl_-_upravitelj_zagona_da_-_omogocen_btn.jpeg" title="Onemogočiti ob zagonu" >}}
   {{< figure align=center src="/images/bcu/bcusl_-_upravitelj_zagona_ne_-_omogocen_btn.jpeg" title="Omogočiti ob zagonu" >}}

{{< /collapse >}}


## Povezave

- Spletna stran [Bulk Crap Uninstaller](https://www.bcuninstaller.com/ "Kliknite/tapnite, da odprete spletno stran!")

## Video verzija

*PREMIERA (23.08.2025, 18:00 / 06:00 PM, vremenska zona: CEST / UTC+2 / GMT+2)*

{{< youtube "3E0yShCEXGc" >}}