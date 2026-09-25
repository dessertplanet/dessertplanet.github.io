---
title: "diii"
weight: 3
summary: "Commissioned by tehn at monome, a web based programming and file management interface for iii-capable devices"
tags: [monome, iii, lua, Web Serial, MIDI]
links:
  - name: "Launch web app"
    url: "https://monome.org/diii"
  - name: "View code"
    url: "https://github.com/monome/web-diii"
lead:
  image: "diii.png"          # a file sitting beside this index.md
  alt: "a screenshot of the diii web app"                    # required: describe what the picture shows
collaborators:
  - name: "@tehn (Brian Crabtree)"
    url: "https://nnnnnnnn.co"                  # optional
license: "GPL-3.0"
date: 2026-03-28
---

Brian (@tehn) at monome reached out about commissioning an adaptation of [web-druid](/projects/web-druid) that would work with monome's new [iii](https://monome.org/docs/iii) framework. I was super excited to get to work on something official for monome, considering I had been a fan of their work for many many years. Working with Brian on this was an absolute pleasure- and the result has been pretty well received, with new iii scripts being released regularly and no issues on the web-diii github since launch.

For those who are into instrument design, iii really is special and I strongly encourage you to give iii script development a try. Imagine basically being able to develop your own custom midi control gestures on hardware that supports it, then being able to plug that custom controller into any MIDI host and interact with that instrument using your custom interface. I have had a huge amount of fun with my grid plugged directly into my Workshop System doing this, or even just plugged into my laptop with some of the built-in synthesizers included with Ableton Live.

diii is similar to [web-druid](/projects/web-druid) in that it communicates via utf-8 encoded string literals containing lua that the iii firmwares understand, but diii is different in that it also allows interaction with the [littlefs](https://github.com/littlefs-project/littlefs) filesystem that exists on iii devices. So you can upload new scripts or presets, download scripts that are stored on the device, and more.
