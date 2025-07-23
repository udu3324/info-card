---
title: "info card pcb"
author: "@Danny"
description: "A pcb in the shape of a standard size credit card with rfid, contact information, and useful references/tools."
created_at: "2025-07-21"
---

**Total time taken: 9 hours**

# July 21st: Getting all the resources + schematic

<img width="390" height="589" alt="image" src="https://github.com/user-attachments/assets/e92c7ae0-f273-453c-ba38-1bdc0248dd6d" />

I am following [this](https://jams.hackclub.com/jam/hacker-card) tutorial loosely and choosing to use KiCad instead because I love it.

Ultralibrarian was used to get the symbol & footprint of the NFC IC onto KiCad.

For the NFC antenna, I found a KiCad [forum](https://forum.kicad.info/t/where-to-find-nfc-class-6-antenna-pcb-schematic-for-kicad/30212/5) post which a kind person has made some footprints.

<img width="839" height="682" alt="image" src="https://github.com/user-attachments/assets/42556a87-bac5-42ef-ad54-23d79bbfffae" />

Okay, it is a bit small, so I went ahead and generated my own nfc antenna with a [script](https://github.com/nideri/nfc_antenna_generator) I found.

```
python antGen.py -f card_nfc -n 5 -l 45 -w 30 -c 0.5 -s 0.5 -d 0 -m 0.5 -t 3
```

**Total time spent: ~5 hours**

# July 22nd: Footprints and Custom Silkscreen

<img width="836" height="513" alt="kicad_r1oFACaeyi" src="https://github.com/user-attachments/assets/1faef982-e6d2-4999-8051-d0c5bea923f9" />

I decided that my info card was going to look a little diy ish. I would be using Krita and handwriting 99% of my graphics for my pcb. It turned out okay.

<img width="663" height="429" alt="kicad_KLNXh5hD4w" src="https://github.com/user-attachments/assets/9c506b5e-ad27-437e-907c-f04492cb9c6e" />

On the back side, i put some useful/common footprints for me to reference to later on when designing more pcbs. I don't think copper pads on top of an nfc antenna would be great, so i made sure to avoid placing any directly on its path. I also hand drew some graphics on the back too.

My info card should be done now, and is ready for fabrication!

**Total time spent: ~4 hours**

# July 23rd: Price Shortening

I am importing my fabricated files from KiCad into JLCPCB to see how much it costs. This is also technically july 22nd but time flies :shrug:

Tariffs are also really a pain.

I changed the PCBA quantity from 5 to 2.

I realized i have an unnecessary extended part, so i will go ahead and use a smaller LED.

**Total time spent: ~1 hour**