---
title: "viii"
weight: 4
summary: "iii and lua compiled to WASM, basically the web as an iii target. This allows users with older or incompatible hardware to join in the iii fun"
tags: [monome, iii, lua, Web Serial, midi, WASM]
links:
  - name: "GitHub"
    url: ""
lead:
  image: "viii.png"
license: "GPL-3.0"
date: 2026-04-07
---

viii came about because I was super excited about [diii](/projects/diii) but I was super cognizant of the fact that there were many folks already engaged with the monome community who would be unable to leverage [iii](https://monome.org/docs/iii) or [diii](/projects/diii) because their grid or arc devices were old enough that they weren't built with the rp2040 processor necessary for iii compatibility. 

I messed around with a branch of [diii](/projects/diii) at one point that did something similar, sending serial magic bytes in the monome mext protocol over web serial to my modern grid in "serialosc" mode instead of iii mode, translating lua to serial at the browser layer instead of the firmware layer... That ended up not making sense to indlude in the core diii implementation but it didn't stop me from wanting to put a version out there that could do this. 

I also had a fortuitous conversation with [Phil Miller](https://github.com/philmillman) while at the Dyski retreat in Toronto, where he mentioned WASM to me and how it seemed like it enabled the possibility of doing a lot more via web apps. 

For viii I then went down this WASM path- effectively building "the browser as an iii device" with the iii framework compiled to WASM along with all the necessary normally device-side dependencies like lua. Instead of a file-system, viii uses your browser cache. It works, in theory, with any grid generation back to the "series" versions, and there have already been super cool examples of folks leveraging this to use iii scripts with their 15-year-old grid hardware, which I was super excited to see.

A big shoutout to Zack ([@infinitedigits](https://infinitedigits.co)) for trading grids with me for a bit so I could test older FTDI-based grid models with viii- since all I have usually is my KB2040-based 16x8 Neotrellis DIY grid, and my 16x16 monome zero modern RP2040 grid.