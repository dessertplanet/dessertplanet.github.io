---
title: "Blackbird"
weight: 99
summary: "A scriptable, live-codable, USB-serial-to-CV device implementing monome crow's protocol"
tags: [Music Thing Modular, WS Computer, monome, rp2040, firmware]
lead:
  video: "V9HAspnpEWU"
links:
  - name: "Docs & Download"
    url: "https://computer.musicthing.co.uk/programs/41-blackbird/"
  - name: "View code"
    url: "https://github.com/TomWhitwell/Workshop_Computer/tree/781949a1bd44e65cf23c2a333bb8ac5b1fd5dc38/releases/41_blackbird"
date: 2025-12-25
# The one image or video that represents this project. Optional. Uncomment one:
#
# lead:
#   video: "VIDEO_ID"          # a YouTube id -- works in a plain .md file
#   caption: ""                # optional
#
# lead:
#   image: "shot.jpg"          # a file sitting beside this index.md
#   alt: ""                    # required: describe what the picture shows
#   caption: ""                # optional
#
# Anyone who worked on this with you. Optional -- leave it out entirely for a
# solo project. A collaborator with no url renders as plain text, so someone
# without a profile to link can still be credited:
#
# collaborators:
#   - name: ""
#     url: ""                  # optional
#
# How the work is licensed. Optional. Either spelling works:
#
# license: "MIT"
#
# license:
#   name: "CC BY-SA 4.0"
#   url: "https://creativecommons.org/licenses/by-sa/4.0/"
#
# A video lead needs nothing else. An IMAGE lead needs this page to be a leaf
# bundle, because the file has to live next to it:
#
#     content/projects/<name>/index.md   <- this file
#     content/projects/<name>/shot.jpg
#
# Start one with `hugo new projects/<name>/index.md`, or move an existing
# `<name>.md` to `<name>/index.md` when you add its first image. Setting
# lead.image without doing so fails the build with a message saying as much.
---

Blackbird is the answer to the question "If the Workshop Computer is a codeable computer and it has inputs and outputs capable of CV... could it pretend to be a monome crow?" Which was a particularly interesting question at the time because there was no live coding environment for the Workshop Computer yet, and because the original crow was going out of print- which announced around October of 2025. 

I had learned from Zack ([@infinitedigits](https://infinitedigits.co)) that running a whole lua environment on an rp2040 was possible. He had done this for his [miditocv](https://github.com/schollz/miditocv) project, and that planted the seed that it might be possible- but boy was it hard to optimize.

My goal was to get all of the original [bowery](https://github.com/monome/bowery) scripts running on it and I was able to get maybe three quarters of the way there before getting stuck on specific things. Thankfully most of the failures were interesting in themselves (for example `lorenz.lua` runs but extreeeeeeemely slowwwwwly in a way that I found interesting). And thankfully **Ben Regnier (aka Q\*Ben)** from the Workshop discord got engaged to help me test and tweak certain bowery scripts so that they were compatible in a collection of scripts that ulimately became the "bbbowery" with the additions of my turing script and **Chris Johnson**'s script that plays McCartney's Blackbird when connected to oscillators etc.

The largest challenge here by far: original crow runs on an STM32F* with it's own FPU and floating point math throughout, and the Workshop Computer runs on the rp2040 with no FPU. Any Float/Double operations are outrageously slow so there was a huge amount of adapting to fixed point arithmetic to be done here.
<!--
The lead goes in the front matter above, not here -- this body is for anything
that comes after it. Embeds available in this body:

  {{</* youtube id="VIDEO_ID" class="embed embed-video" */>}}
      Hugo's built-in, for a SECOND video further down the page. Pass the class:
      given one, it emits that wrapper instead of its own inline aspect-ratio
      box, which is what `.embed` spacing and the 16:9 rule in style.css hook
      onto. It also takes start=, end=, title=, loop=, mute=, controls= and
      loading=.
  {{</* bandcamp album="123456789" */>}}
  {{</* bandcamp track="123456789" */>}}

Body images are capped at the 62ch reading measure. Anything that wants to be
wider than the text belongs in the lead.

For a WebMIDI/WebAudio widget, drop the module in static/js/ and add:

  <script type="module" src="/js/your-widget.js"></script>
-->
