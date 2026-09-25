---
title: "MLRws"
weight: 2
summary: "A remix of monome's classic grid-based MLR sample cutting platform that runs on the Workshop Computer right in your eurorack"
tags: ["Music Thing Modular", "WS Computer", "monome", "RP2040", "Firmware"]
links:
  - name: "Docs & download"
    url: "https://computer.musicthing.co.uk/programs/15-mlrws/"
  - name: "Launch sample manager web app"
    url: "/MLRws-web"
  - name: "View code"
    url: "https://github.com/TomWhitwell/Workshop_Computer/tree/781949a1bd44e65cf23c2a333bb8ac5b1fd5dc38/releases/15_MLRws"
lead:
  video: "fhHJykM1GWk"          # a YouTube id -- works in a plain .md file

license: "GPL-3.0"
date: 2026-06-15
---

MLRws was a big undertaking, it allowed me to mess around with my new understanding of how the monome serial protocol works, thanks to my work on [diii](/projects/diii) and [viii](/projects/viii). Originally I actually thought of [viii](/projects/viii) as a sibling project to MLRws since both are based on a similar minimal version of the gesture-to-serial-messages translation available in [libmonome](https://github.com/monome/libmonome/).

I also seized the opportunity to learn about and try out some additional approaches in the world of the Workshop Computer. [Brian Dorsey](https://github.com/briandorsey) showed with one of his excellent early cards Backyard Rain, that streaming ADPCM encoded audio from the flash on the physical program card was possible (this was necessary for Backyard Rain to play rain samples longer than a few seconds). And [RYK](https://www.thonk.co.uk/wp-content/uploads/2026/01/MTM-Music-Thing-Modular-cards-Manual_01_FINAL-THONK_V2.pdf) showed with their powerful tape card that not only reading but **writing and recalling** audio from flash was possible (a closed-source demonstration but enough to get me thinking). 

The idea for MLRws came from the exciting possibility that combining these two techniques with the monome protocol stuff would be sufficient to build out a version of MLR if I could make it fit in the performance constraints of the rp2040. And it did!
