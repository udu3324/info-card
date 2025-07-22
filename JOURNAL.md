---
title: "info card pcb"
author: "@Danny"
description: "A pcb in the shape of a standard size credit card with rfid, contact information, and useful references/tools."
created_at: "2025-07-21"
---

# July 21st: Getting all the resources + schematic

I am following [this](https://jams.hackclub.com/jam/hacker-card) tutorial loosely and choosing to use KiCad instead because I love it.

Ultralibrarian was used to get the symbol & footprint of the NFC IC onto KiCad.

For the NFC antenna, I found a KiCad [forum](https://forum.kicad.info/t/where-to-find-nfc-class-6-antenna-pcb-schematic-for-kicad/30212/5) post which a kind person has made some footprints.

Okay, it is a bit small, so I went ahead and generated my own nfc antenna with a [script](https://github.com/nideri/nfc_antenna_generator) I found.

```
python antGen.py -f card_nfc -n 5 -l 45 -w 30 -c 0.5 -s 0.5 -d 0 -m 0.5 -t 3
```

**Total time spent: ~5 hours**