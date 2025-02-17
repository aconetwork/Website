---
title: "Setup Samba Linux share"
date: 2024-09-05T22:02:09+02:00
# publishDate: 2024-09-05T22:02:09+02:00
url: /Linux-share-smb/
# image: images/2024-thumbs/Linux-share.jpg
categories: 
  - how to
tags: 
  - Linux
showtoc: false  # Table of content: Hide (false) or show (true)
draft: true  # Draft: Show (false) or hide (true)
language: "English"
---

1. **Install Samba**

    Open terminal window and run:

        sudo apt update
        sudo apt install samba

2. **Stop Samba daemon**
    
    Check if Samba service is running:

        sudo systemctl status smbd
    
    If it is running, stop the Samba daemon:

        sudo systemctl stop smbd
    
3. **Back up Samba config file**
    
    Go to a Samba folder:

        cd /etc/samba/

    All Samba configurations are saved in smb.conf file so lets backup or in this case rename the config file first so we have original config file backed up in case we need something from it:
    
        sudo mv smb.conf smb.conf.bak
    
    Now make sure Samba service is stopped `sudo systemctl stop smbd` (like we did before and you can check if stopped).

4. **Create and edit new Samba config file**
    
    We will spend most of the time setting up that config file so let's create new Samba config file with `nano` text editor (you can use whatever text editor you want!):
    
        sudo nano smb.conf
    
    Insert next lines inside:

        [global]
        server string = File Server
        workgroup = Workgroup
        security = user
        map to guest = Bad User
        name resolve order = bcast host
        include = /etc/samba/shares.conf

5. **Create Samba shares config file**

        sudo nano /etc/samba/shares.conf
    
    Insert next lines inside:

        [Public Files]
        path = /share/public_files
        force user = smbuser
        force group = smbgroup
        create mask = 0664
        force create mode = 0664
        directory mask = 0775
        force directory mode = 0775
        public = yes
        writable = yes
    
        [Protected Files]
        path = /share/private_files
        force user = smbuser
        force group = smbgroup
        create mask = 0664
        force create mode = 0664
        directory mask = 0775
        force directory mode = 0775
        public = yes
        writable = no
        Create samba user and group

6. **Create group**

        sudo groupadd --system smbgroup

7. **Create user**

        sudo useradd --system --no-create-home --group smbgroup -s /bin/false smbuser

8. **Create shared directories**

    Create directories:

        sudo mkdir -p /share/public_files
        sudo mkdir /share/private_files
    
    Change ownership/permissions:
    
        sudo chown -R smbuser:smbgroup /share
        sudo chmod -R g+w /share

https://www.learnlinux.tv/setting-up-simple-samba-file-shares/

https://www.youtube.com/watch?v=675p5fuEQa4

https://www.youtube.com/watch?v=Df1MwI9jaPc

## This guide in other languages

- [Slovenski (Slovenian)](// "Kliknite/tapnite da odprete! Click/tap to open!")
- [Srbski (Serbian)](// "Kliknite/tapnite da otvorite! Click/tap to open!")

## Walkthrough Video
<!--
{{< youtube "" >}}
-->