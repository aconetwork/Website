---
title: "Izrada novog Linux koristnika"
date: 2026-09-09T17:00:00+02:00
# publishDate: 2026-08-20T17:28:04+02:00
url: /linux-nov-koristnik-sr/
# image: images/2024-thumbs/20220408-AnyDesk-quick.jpg
categories: 
  - Kako
tags:  
  - Kako
  - Linux
  - Mint
showtoc: true  # Tabela sadržaja: Sakriti (false) ili pokazati (true).
draft: false   # Prikaz na javnoj stranici: Prikaz (false) ili sakriti (true).
language: "Srpski"
---

Dakle ovo je praktično moj prvi Linux tutorijal. Pravimo novog Linux korisnika iz Linux podešavanja i na dva načina u Terminal-u. Pravljenje novog korisnika nije isto na svim Linux sistemima. Ako imate neko pitanje možete da pitate internet ili napišete svoje pitanje u komentarima ispod YouTube videa gde će drugi i/ili ja pokušamo, da vam pomognemo.

<a id="koristnik-ime-lozinka"></a>
{{< notice warning >}}
  - **Korisničko ime** može da ima najviše 32 karaktera. Najbolja praksa je koristiti kratko korisničko ime, prvi karakter mora bude SAMO malo slovo `a-z` ili donja crta `_`, nakon čega slede mala slova `a-z` i/ili brojevi `0-9` i/ili donje crte `_` i/ili minus `-`. Može se koriste i nelatinski znakovi (ćirilica, kineski, grčki, ...), ali se to stvarno nije preporučljivo jer može izazvati nekompaktibilnost i druge probleme, pa koristite samo one iz najbolje prakse.
  - **Lozinka** može da sadrži mala i velika slova `a–z`, brojevi `0-9` i/ili znakove `!@#$%^&*()_+-=[]{}|;:',.<>/?`, razmaci i unikod znakovi su generalno prihvaćeni ako vaš Linux sistem koristi UTF-8 kodiranje. Minimalna dužina je 8 karaktera.
  - **Zadržite barem jednog administratorskog korisnika** jer ako obrišete sve administratorske naloge i ostanete samo sa standardnim nalozima, više ne možete da upravljate svojim Linux-om i samo ponovna instalacija Linux-a pomaže.
{{< /notice >}}

<a id="koristnik-grupe"></a>
{{< notice info >}}
  Evo liste uobičajenih grupa u popularnim Linux distribucijama kojima korisnici mogu da se pridruže radi različitih funkcionalnosti:
    
  - **sudo** je neophodan za administratorske privilegije, da korisniku omoguči izvršavanje komandi sa root pristupom.
  - **adm** se često koristi za omogućavanje pristupa sistemskim zapisima i administrativnim zadacima.
  - **cdrom** se obično koristi za omogućavanje pristupa korisnika optičkim uređajima.
  - **plugdev** daje dozvolu za pristup eksternim uređajima sa podacima kao što su eksterni disk i USB uređaji.
  - **sambashare** daje dozvolu za izradu i upravljanje Samba (Microsoft Windows) mrežnim deljenjem datoteka.
  - **dip** dozvoljava pristup dial-up modemskim vezama.
  - **lpadmin** daje pristup upravljanja štampača i zadataka štampanja.
  - **audio** pruža pristup audio uređajima.
  - **video** omogućava pristup snimanju videa i GPU hardveru.
  - **users** je osnovna grupa za sistemske korisnike.
  - **dialout** je obično potreban za pristup modemu i serijskim uređajima.
  - **games** se ponekad se koristi za omogućavanje pristupa softveru za igre.
{{< /notice >}}

{{< notice tip >}}
  - Terminal prečica na tastaturi `CTRL + ALT + T`.
  - Pritisnite `Enter` dugme tastature za potvrdu svake komande!
{{< /notice >}}

{{< notice note >}}
  Ovaj tutorijal je napravljen u 64-bitnoj Linux Mint distribuciji, verzija 22.3 Zena - Cinnamon.
{{< /notice >}}

## Terminal metode

{{< notice info >}}
  `sudo` služi za podizanje prava komandama kao što su `adduser`, `useradd`, ... sa administratorskim privilegijama.
{{< /notice >}}

Otvorite prozor `Terminal` i napravite novog korisnika pomoću željene komande ispod i uvek potvrdite dugmetom `Enter` na tastaturi.

*(kliknemo na pojedinačni korak ili trougao da sakrijete ili pokažete detalje (slike, informacije, ...))*

{{< collapse summary="**adduser** metoda " openByDefault=true >}}

  `adduser` je omotač/skripta za lakšu upotrebu koja sadrži `useradd` komande. Postoji u nekoliko Ubuntu distribucija ili distroa, kao što je u našem slučaju Linux Mint. Proverite [početak ovog tutorijala](#koristnik-ime-lozinka "kliknemo/tapnite, da skoknete na taj deo!") da vidite, koji su znakovi dozvoljeni.

  Da napravite standardnog korisnika (kasnije će ga pretvorimo u administrator-sudo):

    sudo adduser paradajzkutija

  Podizanje nivoa skripte `adduser` pomoću `sudo` da se napravi novi korisnik što je u našem slučaju `paradajzkutija`, ali vi izaberite bilo koje korisničko ime da napravite. Primer rezultata i upisa dodatnih informacija:

    [sudo] password for testbox:          
    info: Adding user `paradajzkutija' ...
    info: Selecting UID/GID from range 1000 to 59999 ...
    info: Adding new group `paradajzkutija' (1001) ...
    info: Adding new user `paradajzkutija' (1001) with group `paradajzkutija (1001)' ...
    info: Creating home directory `/home/paradajzkutija' ...
    info: Copying files from `/etc/skel' ...
    New password: 
    Retype new password: 
    passwd: password updated successfully
    Changing the user information for paradajzkutija
    Enter the new value, or press ENTER for the default
    Full Name []: paradajzkutija
    Room Number []: 
    Work Phone []: 
    Home Phone []: 
    Other []: 
    Is the information correct? [Y/n] y
    info: Adding new user `paradajzkutija' to supplemental / extra groups `users' ...
    info: Adding user `paradajzkutija' to group `users' ...

  Posle svakok unosa potvrdite sa `Enter` dugmetom tastature.

  - **[sudo] password for testbox:** unesite vašu lozinku trenutno prijavljenog korisnika (u našem slučaju je `testbox`) ako vas to pita.
  - **New password:** unesite novu lozinku za novog korisnika (pogledajte [početak ovog tutorijala](#koristnik-ime-lozinka "kliknemo/tapnite, da skoknete na taj deo!") za dozvoljene znakove). Normalno je da vam Linux ne prikazuje kada pišete pa ostaje prazno.
  - **Retype new password:** ponovo unesite tu novu lozinku. Normalno je da vam Linux ne prikazuje kada pišete pa ostaje prazno.
  - **Full Name []:** ovde unesite ime za profil kao na primer `Paradajz Kutija` gde možemo da koristimo razmake i druge znakove.
  - **Room Number []:** / **Work Phone []:** / **Home Phone []:** / **Other []:** (broj sobe / poslovni telefon / kućni telefon / ostalo) ovo možete pustite prazno ili upišite šta god želite.
  - **Is the information correct? [Y/n]** (da li su informacije tačne? [D/n]) ovde upišite `Y` ili `y` da potvrdite, da su svi uneti podaci ispravni ako pa želite da popravite nešto upotrebite `N` ili `n`. Potvrdite sve sa dugmetom `Enter` na tastaturi.

  Sada je napravljen nov standardni korisnik sa kučnim fasciklom novog korisnika `/home/paradajzkutija`, dodat novo-napravljenoj korisničkoj grupi `paradajzkutija`. Sada ajde da pridružimo novog korisnika grupama kao što je `sudo` za administratorske privilegije i drugim grupama za veći pristup i funkcionalnost, naravno promenimo `paradajzkutija` u vaše novo korisničko ime i odaberite željene grupe. Primer dodavanja grupa korisniku:

    sudo usermod -aG sudo,adm,cdrom,plugdev,sambashare,dip,audio,video,dialout,games,bluetooth paradajzkutija
  
  `sudo` podiže nivo skripte `usermod` da bi dodali korisnika `paradajzkutija` novim grupama odvojenim zarezom `,` sa zastavicom `-aG` ILI `-a -G`. Proverite [početak ovog tutorijala](#koristnik-grupe "kliknemo/tapnite, da skočite na taj deo!") za značenje individualnih grupa!

  Sada je nov koristnik napravljen. Predlažem vam, da ponovno pokrenete računar pre kao što se prijavite u nov profil a niže dole sam vam napisao kako to da napravite.

{{< /collapse >}}

{{< collapse summary="**useradd** metoda" openByDefault=true >}}
  
  Da napravite novog koristnika (pogledajte [početak ovog tutorijala](#koristnik-ime-lozinka "kliknemo/tapnite, da skoknete na taj deo!") za koji znakovi su dozvoljeni) upotrebite:

    sudo useradd -m -s /bin/bash paradajzkutija2

  - **-m** je zastavica za automatsku izradu početne fascikle sa novim korisničkim imenom (naš primer `/home/paradajzkutija2`).
  - **-s /bin/bash** `-s` je zastavica koja definiše put do podrazumevane školjke za prijavu korisnika, nakon čega mora bude put do njega kao što je u našem slučaju `/bin/bash`. Ako ne upotrebite `-s /bin/bash` vaš novi korisnik će dobije `/bin/sh`. `bash` i `sh` su dve različite školjke gde je `bash` kao `sh` ali sa više funkcija, boljom sintaksom gde većina komandi radi isto, ali nisu ista stvar.
  
  Da podesite lozinku (pogledajte [početak ovog tutorijala](#koristnik-ime-lozinka "kliknemo/tapnite, da skoknete na taj deo!") za dozvoljene znakove) za novog koristnika upotrebite:

    sudo passwd paradajzkutija2

  Rezultat je:

    [sudo] password for testbox:          
    New password: 
    Retype new password: 
    passwd: password updated successfully
    
  - **[sudo] password for testbox:** unesite vašu lozinku trenutno prijavljenog korisnika (u našem slučaju je `testbox`) ako vas to pita.
  - **New password:** unesite novu lozinku za novog korisnika (pogledajte [početak ovog tutorijala](#koristnik-ime-lozinka "kliknemo/tapnite, da skoknete na taj deo!") za dozvoljene znakove). Normalno je da vam Linux ne prikazuje kada pišete pa ostaje prazno.
  - **Retype new password:** ponovo unesite tu novu lozinku. Normalno je da vam Linux ne prikazuje kada pišete pa ostaje prazno.

  Da upišete puno ime (Full name) novog koristnika upotrebite:

    sudo usermod -c "Paradajz Kutija2" paradajzkutija2

  Između navodnika upišete šta želimo, ali pustite navodnike na miru! Puno ime može da sadrži razmake i druge znakove.

  Sada je napravljen nov standardni korisnik sa kućnom fasciklom novog korisnika `/home/paradajzkutija2`, dodat na novo napravljenoj korisničkoj grupi `paradajzkutija2`. Sada ajde da pridružimo novog korisnika grupama kao što je `sudo` za administratorske privilegije i drugim grupama za veći pristup i funkcionalnost, naravno promenite `paradajzkutija2` u vaše novo korisničko ime i unesite željene grupe. Primer dodavanja grupa korisniku:

    sudo usermod -aG sudo,adm,cdrom,plugdev,sambashare,dip,audio,video,dialout,games,bluetooth paradajzkutija2

  `sudo` podiže skriptu `usermod`, da bi pridružila korisnika `paradajzkutija2` novim grupama odvojenim zarezom `,` sa zastavicom `-aG` ILI `-a -G`. Proverite [početak ovog tutorijala](#koristnik-grupe "kliknemo/tapnite, da skočite na taj deo!") za značenje individualnih grupa!

{{< /collapse >}}

Sada kada je nov koristnik napravljen ponovno pokrenite računar, da potvrdite promene i onda se prijavite u nov koristnički profil.

1. Sa levim dugmetom miša kliknemo na meni dugme `LM`.

   {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_btn_hover.jpeg">}}

2. Sa levim dugmetom miša kliknemo na dugme `Shut down` (izključenje).

   {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_power_btn_hover.jpeg">}}

3. Sa levim dugmetom miša kliknemo na dugme `Restart` (ponovno pokretanje) u prozoru `Shut down` (izključenje).

   {{< figure align=center src="/images/LinuxMint/en_-_shut_down_window_-_restart_btn_hover.jpeg">}}

{{< collapse summary="Prikazati sve koristnike sa home fasciklom" openByDefault=false >}}

    cat /etc/passwd | grep '/home'

  Komanda `cat` pokaže sadržaj datoteke, može je kombinovati datoteke, a takođe i napraviti nove datoteke. Sa našom komandom pretražimo datoteku `passwd` koja se nalazi u fascikli `/etc` i komandujemo je da pokaže linije koje sadrže samo `/home` i evo primera rezultata:
  
    testbox:x:1000:1000:Test Box,,,:/home/testbox:/bin/bash
    paradajzkutija:x:1001:1001:Paradajz Kutija,,,:/home/paradajzkutija:/bin/bash
    paradajzkutija2:x:1002:1002:Paradajz Kutija2:/home/paradajzkutija2:/bin/bash

  Pojedinačni elementi u svakom redu su odvojeni dvotačkom `:`.

  - **testbox** je korisničko ime ili prijavno ime.
  - **x** je šifrovana lozinka je sačuvana u datoteci `/etc/shadow`.
  - **1000** je UID (identifikacijski broj korisnika).
  - **1000** je primarni GID (identifikacijski broj primarne grupe).
  - **Test Box,,,** može da sadrži puno ime korisnika, broj zgrade i sobe, kontakt osobu ili bilo koje druge korisničke informacije odvojene zarezom `,`.
  - **/home/testbox** je početna fascikla za korisnika.
  - **/bin/bash** je prijavna školjka za korisnika. Lokacije važećih prijavnih školjki su u datoteci `/etc/shells`.

{{< /collapse >}}

{{< collapse summary="**deluser** za brisanje određenog korisnika i njegove kučne fascikle" openByDefault=false >}}

    sudo deluser --remove-home paradajzkutija2

  - **deluser** je komanda za brisanje korisnika.
  - **--remove-home** je zastavica za trajno brisanje kučne fascikle korisnika.
  - **paradajzkutija2** je korisničko ime za brisanje, upotrebite korisničko ime koje vi želite da izbrišete.

  **Potvrdite brisanje korisnika sa Enter dugmetom na tastaturi i kada ga obrišete, fascikla profila i taj korisnik će zauvek nestati zato budite sigurni da to želite!**

{{< /collapse >}}

## methoda u Linux podešavanjima: Users and Groups (koristnici i grupe)

*(kliknemo na pojedinačni korak ili trougao da sakrijete ili pokažete detalje (slike, informacije, ...))*

  {{< collapse summary="**Korak 1:** otvorite prozor `Users and Groups` (koristnici i grupe) i koristite trenutno prijavljenu lozinku korisnika Linux-a da pokažete prozor" openByDefault=true >}}

  Prozor možemo otvoriti na nekoliko različitih načina:

  1. Levim dugmetom miša kliknemo na meni `LM`, pišite `users` i kliknemo levim dugmetom miša na rezultat `Users and Groups` (koristnici i grupe).
     
     {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_search_res_-_users_groups_btn_hover.jpeg">}}

  2. Levim dugmetom miša kliknemo na meni `LM` a onda kliknemo na `System Settings` (sistemska podešavanja),

     {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_sys_settings_btn_hover.jpeg">}}

     1. kliknemo levim dugmetom miša u polje za traženje, počnite napišite `users` i kliknemo levim dugmetom miša na rezultat `Users and Groups` (koristnici i grupe).
     
        {{< figure align=center src="/images/LinuxMint/En_-_sys_settings_-_searchbox_user.jpeg" title="Polje za traženje">}}
        {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_sys_settings_-_search_res_-_users_groups_btn_hover.jpeg" title="Rezultat">}}

        **ILI**

     2. premotajte nadole do dna i kliknemo levim dugmetom miša na `Users and Groups` (koristnici i grupe).

        {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_sys_settings_-_scrool_-_users_groups_btn_hover.jpeg">}}

  U novom prozoru upišite lozinku trenutačno prijavljenog korisnika i kliknemo levim dugmetom miša na dugme `Authenticate` (autentifikuj).

  {{< figure align=center src="/images/LinuxMint/en_-_auth_req_-_users_groups_-_authenticate_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** sa levim dugmetom miša kliknemo na dugme `Add` (dodaj) da dodamo novog koristnika" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_add_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** popunite polja i onda levim dugmetom miša kliknemo na dugme `Add` (dodaj)" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_new_user_form_sr_-_add_btn_hover.jpeg">}}

  - **Account Type** (tip računa) u našem slučaju je `Administrator` ali možete da promenite u `Standard` (standardan) sa ograničenoj funkcionalnosti.
  - **Full Name** je puno ime novog korisnika, na primer `Paradajz Kutija`, `Marko` ili šta god želimo.
  - **Username** (koristniško ime) (proverite [početak ovog tutorijala](#koristnik-ime-lozinka "kliknemo/tapnite, da skoknete na taj deo!") za koji su znakovi dozvoljeni).

{{< /collapse >}}

{{< collapse summary="**Korak 4:** u prethodnom prozoru kliknite levim dugmetom miša na novog korisnika gde možemo da podesimo podatke korisnika" openByDefault=true >}}
  
  {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_user_paradajz_kutija2_btn_hover.jpeg">}}

  Sa levim dugmetom miša kliknemo na željen elemenat za promenu.
  
  {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_user_paradajz_kutija2_elements.jpeg">}}

  - **Account Type** (tip računa) u našem slučaju je `Administrator` ali možete da promenite u `Standard` (standardan: ograničena funkcionalnost).
  - **Full Name** je puno ime novog korisnika, na primer `Paradajz Kutija2`, `Marko` ili šta god želimo.
  - **Username** (koristniško ime) (proverite [početak ovog tutorijala](#koristnik-ime-lozinka "kliknemo/tapnite, da skoknete na taj deo!") za koji su znakovi dozvoljeni).
  - **Groups** kojim grupama je koristnik pridružen i sa nekoliko klika promenite..

{{< /collapse >}}

{{< collapse summary="**Korak 5:** podesite novu lozinku za novog koristnika" openByDefault=true >}}
  
  1. Kliknemo levim dugmetom miša na dugme `No password set` (lozinka nije podešena).

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_no_pass_set_btn_hover.jpeg">}}

  2. Unesemo istu novu lozinku u oba tekstualna polja a onda kliknemo levim tasterom miša na dugme `Change` (promeni).

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_change_pass_-_window_change_btn_hover.jpeg">}}

     - **New password** je nova željena lozinka (proverite [početak ovog tutorijala](#koristnik-ime-lozinka "kliknemo/tapnite, da skoknete na taj deo!") za koji znakovi su dozvoljeni).
     - **Confirm password** ovde ponovno upišete novu lozinku da potvrdite, da ste upisali dobro.
     - **Show password** (pokaži lozinku) možete da kliknete da pokažete lozinke, a posle ih popravite.

{{< /collapse >}}

{{< collapse summary="**Korak 6:** podesite grupe za novog koristnika" openByDefault=true >}}
  
  1. kliknemo levim dugmetom miša na listu grupa pored `Groups` (grupe).

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_user_paradajzkutija2_groups_list_btn_hover.jpeg">}}

  2. Označite polja za potvrdu grupa sa kojima želimo da se taj korisnik poveže, a onda kliknemo levim dugmetom miša na dugme `OK` (u redu).

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_groups_-_window_OK_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="Brisanje odabranog koristnika" openByDefault=true >}}
  
  U glavnom prozoru `Users and Groups` (koristnici i grupe):

  1. U levoj koloni kliknemo levim dugmetom miša na korisničko ime, koje želimo da izbrišete.

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_user_paradajz_kutija2_btn_hover.jpeg">}}

  2. Levim dugmetom miša kliknemo na dugme `Delete` (Izbriši) na dnu.

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_delete_btn_hover.jpeg">}}

  3. Levim dugmetom miša kliknemo na dugme `Yes` (da).

     {{< figure align=center src="/images/LinuxMint/en_-_users_groups_-_delete_-_yes_btn_hover.jpeg">}}

  Sada su korisnički nalog i njegova početna fascikla izbrisani.

{{< /collapse >}}

## Ponovo pokrenite računar i prijavite se u novo koristničko ime

Sada kada je novi korisnik kreiran, ponovo pokrenite računar da potvrdite promene a onda se prijavite u novi korisnički nalog.

*(kliknemo na pojedinačni korak ili trougao da sakrijete ili pokažete detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** levim dugmetom miša kliknemo na dugme `LM` menija" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 2:** levim dugmetom miša kliknemo na dugme `Shut down` (izključenje)" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_lm_menu_-_power_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 3:** levim dugmetom miša kliknemo na dugme `Restart` (ponovno pokretanje) u prozoru `Shut down` (izključenje)" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_shut_down_window_-_restart_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 4:** kada se pokaže prijavni ekran Linux-a levim dugmetom miša kliknemo na novog koristnika" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_login_-_user_paradajz_kutija_btn_hover.jpeg">}}

{{< /collapse >}}

{{< collapse summary="**Korak 5:** upišite lozinku i da se prijavite upotrebite `Enter` dugme na tastaturi" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_login_-_user_paradajz_kutija_pass_enter.jpeg">}}

{{< /collapse >}}

## Posle prijave u novog koristnika

*(kliknemo na pojedinačni korak ili trougao da sakrijete ili pokažete detalje (slike, informacije, ...))*

{{< collapse summary="Prvo vidimo prozor dobrodošlice `Welcome`, slobodno ga pregledajte" openByDefault=true >}}

  {{< figure align=center src="/images/LinuxMint/en_-_welcome_window.jpeg">}}

  Ako ne želimo da se ovaj prozor ponovo pojavi kada uključimo računar, samo kliknemo levim dugmetom miša odčekirajte polje za potvrdu pored opcije `Show this dialogue at startup` (prikaži ovaj dijalog kod pokretanja).

  {{< figure align=center src="/images/LinuxMint/en_-_welcome_-_checkbox_checked_hover.jpeg">}}

  {{< figure align=center src="/images/LinuxMint/en_-_welcome_-_checkbox_unchecked_hover.jpeg">}}

  Sada možete, da zatvorite ovaj prozor klikom levog dugmeta miša na dugme ![X](/images/LinuxMint/en_-_close_x_btn_hover.jpeg) u gornjem desnom uglu.

{{< /collapse >}}

{{< collapse summary="Promenite rezoluciju ekrana ako je potrebno" openByDefault=false >}}

  1. U praznom delu radne površine kliknemo desnim dugmetom miša a onda levim dugmetom miša kliknemo na `Display settings` (podešavanja ekrana)
  
     {{< figure align=center src="/images/LinuxMint/en_-_desktop_-_rmb_-_display_settings_btn_hover.jpeg">}}

  2. kliknemo levim dugmetom miša na polje za izbor pored `Resolution` (rezolucija).
  
     {{< figure align=center src="/images/LinuxMint/en_-_display_-_resolution_selection_hover.jpeg">}}

  3. kliknemo levim dugmetom miša na željenu rezoluciju, u našem slučaju je to 1080p ili 1920 x 1080 piksela.
  
     {{< figure align=center src="/images/LinuxMint/en_-_display_-_resolution_-_1080p_select_hover.jpeg">}}

  4. Možete da promenite i druge elemente i kada je sve završeno kliknemo levim dugmetom miša na dugme `Apply` (primeni).
  
     {{< figure align=center src="/images/LinuxMint/en_-_display_-_apply_btn_hover.jpeg">}}

  5. Linux nas pita, da li želimo da zadržimo podešavanja koje ste podesili i kliknemo levim dugmetom miša na dugme `Keep changes` (zadrži promene).
  
     {{< figure align=center src="/images/LinuxMint/en_-_display_-_keep_settings_-_keep_changes_btn_hover.jpeg">}}

  Sada možete, da zatvorite ovaj prozor klikom levog dugmeta miša na dugme ![X](/images/LinuxMint/en_-_close_x_btn_hover.jpeg) u gornjem desnom uglu.

{{< /collapse >}}

{{< collapse summary="**System Reports** obaveštenje sistemskih izveštaja" openByDefault=false >}}

  1. Levim dugmetom miša kliknemo na dugme `System Reports` (sistemski izveštaji).
  
     {{< figure align=center src="/images/LinuxMint/en_-_panel_-_notification_system_btn_hover.jpeg">}}

  2. Sačekajte da se sistemske provere završe.
  
     {{< figure align=center src="/images/LinuxMint/en_-_system_informations_-_system_reports_-_running_checks.jpeg">}}

  3. Ako želite možete da podesite `Timeshift` sa klikom levog dugmeta miša na dugme `Launch Timeshift` (pokreni Timeshift) ali pošto to nije tema ovog tutorijala samo kliknemo levim dugmetom miša na dugme `Ignore this report` (ignoriši ovaj izveštaj). Timeshift je veoma važan i trebalo bi, da ga koristite a o tome če pričam u nekom budućem tutorijalu.
  
     {{< figure align=center src="/images/LinuxMint/en_-_system_informations_-_system_reports_-_timeshift_ignore_btn_hover.jpeg">}}

  4. Linux nas pita, da li stvarno želimo da ignorišemo taj izveštaj, samo kliknemo levim dugmetom miša na dugme `OK` (u redu).
  
     {{< figure align=center src="/images/LinuxMint/en_-_system_informations_-_system_reports_-_want_to_ignore_-_ok_btn_hover.jpeg">}}

  Sada možete da zatvorite ovaj prozor klikom levog dugmeta miša na dugme ![X](/images/LinuxMint/en_-_close_x_btn_hover.jpeg) u gornjem desnom uglu.

{{< /collapse >}}

{{< collapse summary="**Update Manager** obaveštenje upravljača ažuriranja" openByDefault=false >}}

  1. Levim dugmetom miša kliknemo na dugme obaveštenja `Update Manager` (upravljač ažuriranja).
  
     {{< figure align=center src="/images/LinuxMint/en_-_panel_-_update_manager_btn_hover.jpeg">}}

  2. U prozoru `Welcome to the Update Manager` (dobrodošli u upravljač ažuriranja) levim dugmetom miša kliknemo na dugme `OK` (u redu) da potvrdimo.
  
     {{< figure align=center src="/images/LinuxMint/en_-_update_manager_-_welcome_-_ok_btn_hover.jpeg">}}

  Sada možete da zatvorite ovaj prozor klikom levog dugmeta miša na dugme ![X](/images/LinuxMint/en_-_close_x_btn_hover.jpeg) u gornjem desnom uglu.

{{< /collapse >}}



<!--*(kliknemo na pojedinačni korak ili trougao da sakrijete ili pokažete detalje (slike, informacije, ...))*

{{< collapse summary="**Korak 1:** TEKST_OVDE" openByDefault=true >}}

  UNUTRAŠNJI PODACI

{{< /collapse >}}

*(Ovaj tutorijal je napravljen sa 64-bitnim Windows 11 24H2)*

[]( "kliknemo/tapnite, da otvorite veb stranicu!")
![](/images/social-logos/X.png)

{{< figure align=center src="/images/Brave/PICTURE.jpeg" title="" float=left >}}
{{< figure align=center src="/images/Brave/PICTURE.jpeg">}}


{{< recipe-header >}}

  {{< figure align=center src="/images/Recipes/Pancakes_rolled.jpeg" float=left >}}

  PODACI

{{< /recipe-header >}}

## Sastojci (za 2 osobe i 3 serviranja)

- 

## Postupak

1.

Prijatno =).



## Video verzija

*(..2025, 18:00 / 06:00 PM, vremenska zona: CET / UTC+1 / GMT+1)*
*(..2025, 18:00 / 06:00 PM, vremenska zona: CEST / UTC+2 / GMT+2)*

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