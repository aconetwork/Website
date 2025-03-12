---
title: "Weird Symptoms Fixed"
date: 2024-07-12T14:23:28+02:00
# publishDate: 2024-07-12T14:23:28+02:00
url: /Weird-pc-symptoms-fixed/
# image: images/2024-thumbs/Weird-symptoms-fixed.jpg
categories: 
  - how to
  - AST
tags: 
  - hardware
showtoc: false  # Table of content: Hide (false) or show (true)
draft: true  # Draft: Show (false) or hide (true)
language: "English"
---

Couple years ago had weird symptoms with 4. GEN i5 computer where suddently it would not post. So what I did:

1. Checked and reconnected power and other connectors, no post. 
2. Reseted CMOS chip (BIOS) by removing CMOS battery for few minutes, no post.
3. There was one 4GB stick RAM on A1 slot (second slot from the left), so I slotted at A2 (forth slot the left), no post.
4. Took one of my working RAM and putted in A2 slot, no post.
5. Replaced graphic card for another working one, no post.
6. Replaced with working power supply (PSU), no post.
7. Disconnected all except most basic to run the computer but... NO POST damn.
8. I did not have any other CPU on hand so I took original RAM stick and putted it into B2 (third slot the left) and it POSTED YES!!!

Because it worked I wanted to check if it still works when I turned off and back on the computer... no post! Then I putted RAM stick from B2 to A1, computer posted but when restarted, no post. So back to B2, it posted, went quickly in to the BIOS and it became frozen, unresponsive. On my laptop downloaded BIOS firmware upgrade file, copyed it to some FAT32 formated USB stick inserted it into the problematic computer. Turned on the computer, went into the BIOS, opened QFLASH (i think that was the name of BIOS flashing option). After succesfull flashing the computer turned off and back on by it self and everything started working normally, YEEY 😋. Now I restarted, powered off and on the computer and every time it worked like a charm. So I was lucky I had a post enough to flash the newer Firmware.

I do not have CMOS chip programmer and never desoldered any chip before (I plan to learn & train the microsoldering in the future 😎). So that kind of issue... couple of hours I needed to do all this loool. It looks like CMOS in the computer got corrupted where even CMOS reset did not work but I got new experience 😋. 

Sometimes computer can give you very strange issues, important is to diagnose according the symptoms and go step by step to figure out, what is wrong. Hope you learned something today and I wish you to have an amazing day 😁👍️.

## Walkthrough Video

<!-- {{< youtube "" >}} -->