---
title: "Izdelava novega Linux uporabnika"
date: 2026-09-09T17:00:00+02:00
# publishDate: 2026-08-20T17:25:10+02:00
url: /linux-nov-uporabnik-sl/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - Kako
tags: 
  - Kako
  - Linux
  - Mint
showtoc: true  # Seznam vsebine: Skriti (false) ali prikazati (true)
draft: false  # Prikaz na javni strani: Prikaz (false) ali skriti (true)
language: "Slovenski"
---

Torej, to je praktično moj prvi Linux vodič. Novega Linux uporabnika bomo ustvarili iz nastavitev Linux-a ter na dva načina v Terminalu. Ustvarjanje novega uporabnika ni enako na vseh Linux sistemih. Če imaste kakšno vprašanje lahko pa vprašate internet ali napišete svoje vprašanje v komentarjih pod videom na YouTubu, kjer vam bomo drugi in/ali jaz poskušali pomagati.

<a id="uporabnik-ime-geslo"></a>
{{< notice warning >}}
  - **Uporabniško ime** je lahko dolgo največ 32 znakov. Najboljša praksa je kratko uporabniško ime, prvi znak mora biti SAMO mala črka `a-z` ali črtica spodaj `_`, ki mu sledijo male črke `a-z`, številke `0-9`, črtice spodaj `_` in/ali vezaji `-`. Uporabljate lahko tudi nelatinske znake (cirilica, kitajščina, grščina ...) vendar to ni priporočljivo, ker lahko povzroči težave s kompaktibilnostjo ter druge težave zato uporabite le tiste s najboljšo prakso.
  - **Geslo** lahko vsebuje male ali velike črke `a–z`, številke `0-9` ter znake `!@#$%^&*()_+-=[]{}|;:',.<>/?`, presledke in unikodne znake so na splošno sprejeti če vaše okolje Linux uporablja kodiranje UTF-8. Najmanjša dolžina je 8 znakov.
  - **Ohranite vsaj enega skrbniškega uporabnika**, ker če izbrišete vse skrbniške račune in vam ostanejo samo standardni računi, ne morete več upravljati Linuxa in vam bo pomagala le ponovna namestitev Linuxa.
{{< /notice >}}

<a id="uporabnik-skupine"></a>
{{< notice info >}}
  Tukaj je seznam pogostih skupin v priljubljenih distribucijah Linuxa, v katere se lahko uporabniki vključijo za različne funkcionalnosti:

  - **sudo** je bistvenega pomena za skrbniške pravice, ki uporabniku omogočajo izvajanje ukazov z dostopom na ravni root.
  - **adm** se pogosto uporablja za omogočanje dostopa do sistemskih dnevnikov in skrbniških opravil.
  - **cdrom** se običajno uporablja za omogočanje dostopa uporabnikov do optičnih pogonov.
  - **plugdev** dovoljuje dostop do zunanjih pomnilniških naprav, kot so zunanji diskovni pogoni in pogoni USB.
  - **sambashare** dovoljuje ustvarjanje in upravljanje Samba (Microsoft Windows) mrežne skupne rabe.
  - **dip** omogoča dostop do  modemskih povezav na klic.
  - **lpadmin** dovoljuje dostop do upravljanja tiskalnika in tiskalniških opravil.
  - **audio** omogoča dostop do zvočnih naprav.
  - **video** omogoča dostop do strojne opreme za zajemanje videa in grafične kartice.
  - **users** je osnovna skupina za sistemske uporabnike.
  - **dialout** je običajno potreben za dostop do modema in serijskih naprav.
  - **igre** se včasih uporablja za dostop do programske opreme za igre.
{{< /notice >}}

{{< notice tip >}}
  - Terminal bljižnica na tipkovnici `CTRL + ALT + T`.
  - Pritisnite `Enter` tipko na tipkovnici za potrdilo vsake komande!
{{< /notice >}}

{{< notice note >}}
  Ta vodič je bil narejen v 64-bitni distribuciji Linux Mint, različice 22.3 Zena - Cinnamon.
{{< /notice >}}

## Terminal metode

{{< notice info >}}
  `sudo` služi za dvig privilegijev ukazov, kot so `adduser`, `useradd`, ... z administratorskimi pravicami.
{{< /notice >}}

Odprite okno `Terminal` in ustvarite novega uporabnika z želenim ukazom spodaj ter vedno potrjajte s tipko `Enter` na tipkovnici.

*(kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**adduser** metoda " openByDefault=true >}}

  `adduser` je ovoj/skripta za lažjo uporabo, ki vsebuje ukaze `useradd`. Obstaja v več distribucijah ali distrojih, ki temeljijo na Ubuntuju, kot je v našem primeru Linux Mint. Preverite [začetek tega vodiča](#uporabnik-ime-geslo "kliknemo/tapnite za skok na ta del!") za dovoljene znake.

  Za ustvarjanje standardnega uporabnika (kasneje ga bom pretvoril v administrator-sudo):

    sudo adduser paradajzkista

  Z dvigom pooblastil `sudo` za skripto `adduser` za izdelavo novega uporabnika, ki je v našem primeru `paradajzkista` vendar vi izberete svoje uporabniško ime, ki želite izdelati. Primer rezultata in vpisa dodatnih informacij:

    [sudo] password for testbox:          
    info: Adding user `paradajzkista' ...
    info: Selecting UID/GID from range 1000 to 59999 ...
    info: Adding new group `paradajzkista' (1001) ...
    info: Adding new user `paradajzkista' (1001) with group `paradajzkista (1001)' ...
    info: Creating home directory `/home/paradajzkista' ...
    info: Copying files from `/etc/skel' ...
    New password: 
    Retype new password: 
    passwd: password updated successfully
    Changing the user information for paradajzkista
    Enter the new value, or press ENTER for the default
    Full Name []: paradajzkista
    Room Number []: 
    Work Phone []: 
    Home Phone []: 
    Other []: 
    Is the information correct? [Y/n] y
    info: Adding new user `paradajzkista' to supplemental / extra groups `users' ...
    info: Adding user `paradajzkista' to group `users' ...

  Po vsakem vnosu potrdite s tipko `Enter` na tipkovnici.

  - **[sudo] password for testbox:** vnesite geslo trenutno prijavljenega uporabnika (v našem primeru `testbox`), če vas sistem vpraša.
  - **New password:** vnesite novo geslo za novega uporabnika (preverite [začetek tega vodiča](#uporabnik-ime-geslo "kliknemo/tapnite za skok na ta del!") za kateri znaki so dovoljeni). Normalno je, da Linux ne prikaže kaj tipkate zato pa ostane prazno.
  - **Retype new password:** ponovno vnesite novo geslo. Normalno je, da Linux ne prikaže kaj tipkate zato pa ostane prazno.
  - **Full Name []:** tukaj vnesite ime profila, kot na primer `Paradajz Kista`, kjer lahko uporabimo presledke in druge znake.
  - **Room Number []:** / **Work Phone []:** / **Home Phone []:** / **Other []:**  (številka sobe / službeni telefon / domači telefon / drugo) te lahko pustite prazne ali vnesete karkoli želimo.
  - **Is the information correct? [Y/n]** (ali so podatki pravilni? [D/n]) tukaj uporabite tipko `Y` ali `y` za potrditev vseh vnešenih podatkov, če jih pa želimo spremeniti uporabimo `N` ali `n`. Potrdimo vnose s `Enter` tipko na tipkovnici.

  Sedaj je ustvarjen nov standarden uporabnik z domačo mapo novega uporabnika `/home/paradajzkista` dodan na novo ustvarjeni uporabniški skupini `paradajzkista`. Zdaj pa pridružimo novega uporabnika skupinam kot je `sudo` za administratorske pravice ter drugim skupinam za večji dostop in funkcionalnost, seveda pa spremenite `paradajzkista` v svoje novo uporabniško ime ter željene skupine. Primer dodajanja skupin uporabniku:

    sudo usermod -aG sudo,adm,cdrom,plugdev,sambashare,dip,audio,video,dialout,games,bluetooth paradajzkista

  `sudo` dvigne skripto `usermod`, da pridruži uporabnika `paradajzkista` novim skupinam ločenim z vejico `,` z zastavico `-aG` ALI `-a -G`. Preverite [začetek tega vodiča](#uporabnik-skupine "kliknemo/pritisnite za skok na ta del!") za pomen vsake skupine!

  Zdaj je ustvarjen nov uporabnik. Pred prijavo v novi profil predlagam, da znova zaženete računalnik, niže spodaj pa sem vam zapisal kako.

{{< /collapse >}}

{{< collapse summary="**useradd** metoda" openByDefault=true >}}
  
  Za izdelavo novega uporabnika (preverite [začetek tega vodiča](#uporabnik-ime-geslo "kliknemo/tapnite za skok na ta del!") za kateri znaki so dovoljeni) uporabite:

    sudo useradd -m -s /bin/bash paradajzkista2

  - **-m** je zastavica za samodejno ustvarjanje domače mape z novim uporabniškim imenom (naš primer `/home/paradajzkista2`).
  - **-s /bin/bash** `-s` je zastavica, ki določa pot do uporabnikove privzete prijavne lupine, sledi ji pot kot je v našem primeru `/bin/bash`. Če ne uporabite `-s /bin/bash` bo vaš novi uporabnik dobil `/bin/sh`. `bash` in `sh` sta dve različni lupini kjer je `bash` podoben `sh` vendar z več funkcijami, boljšo sintakso, kjer večina ukazov deluje enako vendar nista enaki.
  
  Za nastavitev gesla (preverite [začetek tega vodiča](#uporabnik-ime-geslo "kliknemo/tapnite za skok na ta del!") za kateri znaki so dovoljeni) novega uporabnika uporabite:

    sudo passwd paradajzkista2

  Rezultat je:

    [sudo] password for testbox:          
    New password: 
    Retype new password: 
    passwd: password updated successfully

  - **[sudo] password for testbox:** vnesite geslo trenutno prijavljenega uporabnika (v našem primeru `testbox`), če vas sistem vpraša.
  - **New password:** vpišite novo geslo za novega uporabnika.
  - **Retype new password:** ponovno vnesite novo geslo. Normalno je, da Linux ne prikaže kaj tipkate zato pa ostane prazno.

  Za nastavitev polnega imena (Full name) za novega uporabnika uporabite:

    sudo usermod -c "Paradajz Kista2" paradajzkista2

  Med narekovaje napišete kar želimo, vendar narekovaje pustite pri miru! Polno ime lahko vsebuje presledke in druge znake.

  Sedaj je izdelan nov standarden uporabnik z domačo mapo novega uporabnika `/home/paradajzkista2`, ki je dodan novo ustvarjeni uporabniški skupini `paradajzkista2`. Zdaj pa pridružimo novega uporabnika skupinam kot je `sudo` za administratorske pravice in drugim skupinam za večji dostop in funkcionalnost, seveda spremenite `paradajzkista2` v svoje novo uporabniško ime. Primer dodajanja skupin uporabniku:

    sudo usermod -aG sudo,adm,cdrom,plugdev,sambashare,dip,audio,video,dialout,games,bluetooth paradajzkista2
  
  `sudo` poviša skript `usermod` za pridružitev uporabnika `paradajzkista2` novim skupinam, ločenim z vejico `,` z zastavico `-aG` ALI `-a -G`. Preverite [začetek tega vodiča](#uporabnik-skupine "kliknemo/tapnite za skok na ta del!") za pomen posameznih skupin!

{{< /collapse >}}

Ko je nov uporabnik ustvarjen znova zaženite računalnik, da se spremembe uporabijo, nato pa se prijavite v nov uporabniški račun.

1. Z levo miškino tipko kliknemo tipko menija `LM`.

   {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_btn_hover.jpeg">}}

2. Z levo miškino tipko kliknemo tipko `Shut down` (zaustavitev).

   {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_power_btn_hover.jpeg">}}

3. Z levo miškino tipko kliknemo tipko `Restart` (ponoven zagon) v oknu `Shut down` (zaustavitev).

   {{< figure align=center src="/images/LinuxMint/en_-_shut_down_window_-_restart_btn_hover.jpeg">}}

{{< collapse summary="Seznam vseh uporabnikov s domačimi mapami" openByDefault=false >}}

    cat /etc/passwd | grep '/home'

  Ukaz `cat` prikaže vsebino datoteke, lahko združuje ter ustvarja nove datoteke. Z našim ukazom pregledamo datoteko `passwd`, ki se nahaja v mapi `/etc` in ji ukažemo, da prikaže vrstice, ki vsebujejo samo `/home`. Tukaj je primer rezultata:
  
    testbox:x:1000:1000:Test Box,,,:/home/testbox:/bin/bash
    paradajzkista:x:1001:1001:Paradajz Kista,,,:/home/paradajzkista:/bin/bash
    paradajzkista2:x:1002:1002:Paradajz Kista2:/home/paradajzkista2:/bin/bash

  Posamezni elementi v vsaki vrstici so ločeni z dvopičjem `:`.

  - **testbox** je porabniško ime ali prijavno ime.
  - **x** šifrirano geslo je shranjeno v datoteki `/etc/shadow`.
  - **1000** UID (identifikacijska številka uporabnika).
  - **1000** je primarni GID (identifikacijska številka primarne skupine).
  - **Test Box,,,** lahko vključuje polno ime uporabnika, številko stavbe in sobe, kontaktno osebo ali katere koli druge podatke o uporabniku ločene z vejico `,`.
  - **/home/testbox** domača mapa uporabnika.
  - **/bin/bash** prijavna lupina za uporabnika. Poti veljavnih prijavnih lupin se nahajajo v `/etc/shells`.

{{< /collapse >}}

{{< collapse summary="**deluser** za brisanje določenega uporabnika in njegove domače mape" openByDefault=false >}}

    sudo deluser --remove-home paradajzkista2

  - **deluser** je ukaz za brisanje uporabnika.
  - **--remove-home** je zastavica za trajno brisanje domače mape tega uporabnika.
  - **paradajzkista2** je uporabniško ime za izbris. Vi vpišite vaše uporabniško ime, ki ga želimo izbrisati

**Brisanje uporabnika potrdite s tipko Enter in ko izbrišete sta uporabnik in njegova mapa profila za vedno izbrisana, zato se prepričajte, da to želimo storiti!**

{{< /collapse >}}

## Metoda v Linux nastavitvah: Users and Groups oz. Uporabniki in Skupine

*(kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** Odprite okno `Users and Groups` (uporabniki in skupine) in uporabite geslo trenutno prijavljenega uporabnika za prikaz okna" openByDefault=true >}}

  Lahko odpremo okno na nekaj načinov:

  1. Z levo miškino tipko kliknemo na `LM` meni, napišite `users` in nato z levo miškino tipko kliknemo na rezultat `Users and Groups` (uporabniki in skupine).
     
     {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_search_res_-_users_groups_btn_hover.jpeg">}}

  2. Z levo miškino tipko kliknemo na `LM` meni in nato kliknemo na `System settings` (sistemske nastavitve),
   
     {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_sys_settings_btn_hover.jpeg">}}

     1. Z levo miškino tipko kliknemo v iskalno polje, napišite `users` in nato z levo miškino tipko kliknemo na rezultat `Users and Groups` (uporabniki in skupine). 
     
        {{< figure align=center src="/images/LinuxMint/En_-_sys_settings_-_searchbox_user.jpeg" title="Iskalno polje">}}
        {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_sys_settings_-_search_res_-_users_groups_btn_hover.jpeg" title="Rezultat">}}
     
        **ALI**
     
     2. premotajte navzdol in z levo miškino tipko kliknemo na `Users and Groups` (uporabniki in skupine).
       
        {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_sys_settings_-_scrool_-_users_groups_btn_hover.jpeg">}}

  V novem oknu vnesite geslo prijavljenega uporabnika in nato z levo miškino tipko kliknemo na tipko `Authenticate` (preveri pristnost).

  {{< figure align=center src="/images/LinuxMint/en_-_auth_req_-_users_groups_-_authenticate_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** z levo miškino tipko kliknemo na tipko `Add` (dodaj) da dodamo novega uporabnika" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_add_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** izpolnite podatke in nato z levo miškino tipko kliknemo na tipko `Add` (dodaj)" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_new_user_form_sl_-_add_btn_hover.jpeg">}}

  - **Account Type** (tip računa), v našem primeru je `Administrator` vendar lahko spremenite v `Standard` (sandarden) z omejeno funkcionalnostjo.
  - **Full Name** (polno ime) na primer `Paradajz Kista2`,`Franc` ali karkoli želimo.
  - **Username** (uporabniško ime) (preverite [začetek tega vodiča](#uporabnik-ime-geslo "kliknemo/tapnite za skok na ta del!") za kateri znaki so dovoljeni).

{{< /collapse >}}

{{< collapse summary="**Korak 4:** v prejšnjem oknu z levo miškino tipko kliknemo na novega uporabnika za nastavitev njegovih podrobnosti" openByDefault=true >}}
  
  {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_user_paradajz_kista2_btn_hover.jpeg">}}

  Z levo miškino tipko kliknemo na željeni element za spremembo.
  
  {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_user_paradajz_kista2_elements.jpeg">}}

  - **Account Type** (tip računa), v našem primeru je `Administrator` vendar lahko spremenite v `Standard` (sandarden) z omejeno funkcionalnostjo.
  - **Full Name** (polno ime) na primer `Paradajz Kista2`,`Franc` ali karkoli želimo.
  - **Username** (uporabniško ime) (preverite [začetek tega vodiča](#uporabnik-ime-geslo "kliknemo/tapnite za skok na ta del!") za kateri znaki so dovoljeni).
  - **Groups** katerim skupinam je uporabnik pridružen in s nekaj kliki spremenite.

{{< /collapse >}}

{{< collapse summary="**Korak 5:** nastavite novo uporabniško geslo" openByDefault=true >}}
  
  1. Z levo miškino tipko kliknemo na tipko `No password set` (geslo ni nastavljeno).

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_no_pass_set_btn_hover.jpeg">}}

  2. V obeh poljih novega okna vnesite isto novo geslo nato pa z levo miškino tipko kliknemo na tipko `Change` (spremeni).

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_change_pass_-_window_change_btn_hover.jpeg">}}

     - **New password** je vaše novo željeno geslo (preverite [začetek tega vodiča](#uporabnik-ime-geslo "kliknemo/tapnite za skok na ta del!") za kateri znaki so dovoljeni).
     - **Confirm password** tukaj ponovno vpišete novo geslo, da potrdite pravilen vpis.
     - **Show password** (pokaži geslo) potrditveno polje za prikaz obeh gesel za morebitno spremembo.

{{< /collapse >}}

{{< collapse summary="**Korak 6:** nastavite skupine za novega uporabnika" openByDefault=true >}}
  
  1. Z levo miškino tipko kliknemo na spisek skupin zraven `Groups` (skupine).

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_user_paradajzkista2_groups_list_btn_hover.jpeg">}}

  2. Z levo miškino tipko označite potrditvena polja zraven skupin, ki želite pridružiti uporabniku in nato z levo miškino tipko kliknemo na tipko `OK` (v redu).

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_groups_-_window_OK_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="Brisanje izbranega uporabnika" openByDefault=true >}}
  
  UV glavnem oknu `Users and Groups` (uporabniki in skupine):

  1. V levem stolpcu z levo miškino tipko kliknemo uporabniško ime, ki ga želimo izbrisati.

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_user_paradajz_kista2_btn_hover.jpeg">}}

  2. Z levo miškino tipko kliknemo na dnu na tipko `Delete` (izbris).

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_delete_btn_hover.jpeg">}}

  3. Z levo miškino tipko kliknemo tipko `Yes` (da).

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_delete_-_yes_btn_hover.jpeg">}}

  Zdaj sta uporabniški račun in njegova domača mapa izbrisana.

{{< /collapse >}}

## Ponoven zagon računalnika v nov uporabniški račun

Ko je nov uporabnik ustvarjen ponovno zaženite računalnik za uveljavitev sprememb, nato pa se prijavite v nov uporabniški račun.

*(kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** z levo miškino tipko kliknemo na tipko `LM` menija" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** z levo miškino tipko kliknemo na tipko `Shut down` (zaustavitev)" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_power_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** z levo miškino tipko kliknemo na tipko `Restart` (ponoven zagon) v oknu `Shut down` (zaustavitev)" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_shut_down_window_-_restart_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** ko se prikaže prijavni ekran Linux-a kliknemo z levo miškino tipko na novega uporabnika" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_login_-_user_paradajz_kista_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** vnesite geslo in da se prijavite uporabite tipko `Enter` na tipkovnici za prijavo" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_login_-_user_paradajz_kista_pass_enter.jpeg">}}

{{< /collapse >}}

## Po prijavi v novega uporavnika

*(kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="Najprej vidite pozdravno `Welcoma` okno, raziščite si ga" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_welcome_window.jpeg">}}

  Če ne želimo, da se to okno ponovno prikaže ob vklopu računalnika, preprosto z levo miškino tipko odkljukajte spodnje potrditveno polje poleg možnosti `Show this dialogue at startup` (prikaži to pogovorno okno ob zagonu).

  {{< figure align=center src="/images/LinuxMint/en_-_welcome_-_checkbox_checked_hover.jpeg">}}

  {{< figure align=center src="/images/LinuxMint/en_-_welcome_-_checkbox_unchecked_hover.jpeg">}}

  Sedaj zaprite tole okno s klikom leve miškine tipke na tipko ![X](/images/LinuxMint/en_-_close_x_btn_hover.jpeg) v zgornjem desnem kotu.

{{< /collapse >}}

{{< collapse summary="Po potrebi spremenite ločljivost zaslona" openByDefault=false >}}

  1. Na praznem prostoru namizja kliknemo z desno miškino tipko in nato z levo miškino tipko kliknemo na `Display settings` (nastavitve zaslona).
  
     {{< figure align=center src="/images/LinuxMint/en_-_desktop_-_rmb_-_display_settings_btn_hover.jpeg">}}

  2. Z levo miškino tipko kliknemo na izbirno polje zraven `Resolution` (ločljivost).
  
     {{< figure align=center src="/images/LinuxMint/en_-_display_-_resolution_selection_hover.jpeg">}}

  3. Z levo miškino tipko kliknemo na želeno ločljivost, v mojem primeru je to 1080p ali 1920 x 1080 slikovnih pik.
  
     {{< figure align=center src="/images/LinuxMint/en_-_display_-_resolution_-_1080p_select_hover.jpeg">}}

  4. Lahko spremenite tudi ostale elemente in ko ste končali z levo miškino tipko kliknemo na tipko `Apply` (uporabi).
  
     {{< figure align=center src="/images/LinuxMint/en_-_display_-_apply_btn_hover.jpeg">}}

  5. Linux nas sprašuje ali želimo ohraniti spremembe nastavitev in z levo miškino tipko kliknemo na tipko  `Keep changes` (ohrani spremembe).
  
     {{< figure align=center src="/images/LinuxMint/en_-_display_-_keep_settings_-_keep_changes_btn_hover.jpeg">}}

  Sedaj zaprite tole okno s klikom leve miškine tipke na tipko ![X](/images/LinuxMint/en_-_close_x_btn_hover.jpeg) v zgornjem desnem kotu.

{{< /collapse >}}

{{< collapse summary="**System Reports** obvestilo sistemskih poročil" openByDefault=false >}}

  1. Z levo miškino tipko kliknemo na tipko `System Reports` (sistemska poročila).
  
     {{< figure align=center src="/images/LinuxMint/en_-_panel_-_notification_system_btn_hover.jpeg">}}

  2. Počakajte, da se sistemski pregledi zaključijo.
  
     {{< figure align=center src="/images/LinuxMint/en_-_system_informations_-_system_reports_-_running_checks.jpeg">}}

  3. Funkcijo `Timeshift` lahko nastavite tako, da z levo miškino tipko kliknemo tipko `Launch Timeshift` (zaženi Timeshift) vendar ker to ni predmet tega vodiča bomo preprosto kliknili z levo miškino tipko na tipko `Ignore this report` (prezri to poročilo). Timeshift je zelo pomemben in bi ga morali uporabljati, o tem pa v enem prihodnjem vodiču.
  
     {{< figure align=center src="/images/LinuxMint/en_-_system_informations_-_system_reports_-_timeshift_ignore_btn_hover.jpeg">}}

  4. Linux nas sprašuje ali res želimo prezreti to poročilo, samo kliknemo z levo miškino tipko na tipko `OK` (v redu).
  
     {{< figure align=center src="/images/LinuxMint/en_-_system_informations_-_system_reports_-_want_to_ignore_-_ok_btn_hover.jpeg">}}

  Sedaj zaprite tole okno s klikom leve miškine tipke na tipko ![X](/images/LinuxMint/en_-_close_x_btn_hover.jpeg) v zgornjem desnem kotu.

{{< /collapse >}}

{{< collapse summary="**Update Manager** obvestilo upravitelja posodobitev" openByDefault=false >}}

  1. Z levo miškino tipko kliknemo na tipko obvestila `Update Manager` (upravitelj posodobitev).
  
     {{< figure align=center src="/images/LinuxMint/en_-_panel_-_update_manager_btn_hover.jpeg">}}

  2. V oknu `Welcome to the Update Manager` (dobrodošli v upravitelju posodobitev) z levo miškino tipko kliknemo na tipko `OK` (v redu) da potrdimo.
  
     {{< figure align=center src="/images/LinuxMint/en_-_update_manager_-_welcome_-_ok_btn_hover.jpeg">}}

  Sedaj lahko zaprete okno s klikom leve miškine tipke na tipko ![X](/images/LinuxMint/en_-_close_x_btn_hover.jpeg) v zgornjem desnem kotu.

{{< /collapse >}}



<!--*(kliknite/tapnite na posamezni korak ali trikotnik za skriti ali prikazati podrobnosti (slika, informacije, ...))*

{{< collapse summary="**Korak 1:** TEXTHERE" openByDefault=true >}}

  PODATKI

{{< /collapse >}}

*(Ta vodič je bil narejen na 64-bitnem Windows 11 24H2)*

[]( "kliknemo/tapnite, da odprete spletno stran!")
![](/images/social-logos/X.png)

{{< figure align=center src="/images/Brave/PICTURE.jpeg" title="" float=left >}}
{{< figure align=center src="/images/Brave/PICTURE.jpeg">}}

Pika: &#46;


{{< recipe-header >}}

  {{< figure align=center src="/images/Recipes/Pancakes_rolled.jpeg" float=left >}}

  PODATKI

{{< /recipe-header >}}

## Sestavine (za 2 osebi in 3 serviranja)

- 

## Proces

1. 

Dober tek :).




## Video verzija

*(..2025, 18:00 / 06:00 PM, časovni pas: CET / UTC+1 / GMT+1)*
*(..2025, 18:00 / 06:00 PM, časovni pas: CEST / UTC+2 / GMT+2)*

{{< youtube "O1DA0HpFK-4" >}}

{{< rawhtml >}}
<p style="color:green;text-align:center;">Hello World!</p>
{{< /rawhtml >}}

{{< notice info >}}
  TEXT
{{< /notice >}}

{{< notice note >}}
  TEXT
{{< /notice >}}

{{< notice tip >}}
  TEXT
{{< /notice >}}

{{< notice warning >}}
  TEXT
{{< /notice >}}

-->