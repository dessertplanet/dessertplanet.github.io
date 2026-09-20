---
title: "Program Cards site"
weight: 1
summary: "computer.musicthing.co.uk is a documentation, curation, and discovery website for Workshop Computer program cards"
tags: ["Music Thing Modular", "WS Computer", "Web"]
links:
  - name: "Launch site"
    url: "https://computer.musicthing.co.uk"
  - name: "View code"
    url: "https://github.com/TomWhitwell/Workshop_Computer/tree/f74ab1577fefb4088cf6b538afdcf0deee3b62e3/tools/sitegen"
lead:
  image: "site-screenshot.png"
  alt: "The computer.musicthing.co.uk front page, showing Tom Whitwell's weekly curated selection of program cards above the full searchable card index"
collaborators:
  - name: "Tom Whitwell"
    url: "https://musicthing.co.uk"
  - name: "Phil Miller"
    url: "https://github.com/philmillman"
  - name: "Chris Johnson"
    url: "https://github.com/chrisgjohnson"
  - name: "Jason Moore"
    url: "https://github.com/casconed"
---

**Finally a scalable home for the 100+ computer cards out there!** 

This project was born out of the realization that because the number of [Music Thing Modular Workshop Computer](https://www.musicthing.co.uk/workshopsystem/) program cards was growing exponentially (accelerated at least in part by the community leveraging new AI tools), the system for discovery/entry to the community had to change.

In my mind, the risk here was existential to the community (that I care so much about) in that new people are arriving in the discord and building their Computer modules all the time, but where do they start? The only ways for newcomers to approach what cards to try first or how to get started were for them to:
1. Peruse the [GitHub](https://github.com/TomWhitwell/Workshop_Computer) directly (not ideal!)

2. Leverage the old "green" metadata site built out of the main repo that was excellent when there was a manageable number of cards but only supported sort-by-latest and sort-by-card-number (also not ideal)

3. Reading the Workshop discord for several weeks in order to begin to understand all the chatter going on there (not ideal!)

My biggest concern was this issue at the top of the community funnel would discourage newcomers and ultimately starve the ecosystem of the (IMO) necessary oxygen that is fresh eyes and fresh ideas for new cool cards.

So this site is born out of that. It is kind of a bespoke Static Site Generator that includes a data pipeline from each card author's release folder all the way to a public docs site (on the musicthing.co.uk domain, no less!) with consistent documentation for card authors who adopt the schema and crucially, a front page curated (weekly as of writing!) by Tom Whitwell himself so that there can be intention behind the landing place where newcomers are sent without overwhelming them with 1,000,000 cards all of which are rad but not all of which are great starting places.

It wouldn't have been possible without a massive amount of brainstorming in the Workshop Discord, a prototype from **Tom Whitwell**, many many code/UX/Accessibility reviews from **Phil Miller**, UX polish contributions from **Chris Johnson**, and test bootstrapping from **Jason Moore**.
