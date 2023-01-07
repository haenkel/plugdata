---
title: metronome~

description: Metronome clicks

categories:
- object

pdcategory: Control

arguments:
- type: list
  description: low, mid, high frequencies
  default: 600, 1000, 1700

inlets:
  1st:
  - type: list
    description: count ouput from [metronome]

outlets:
  1st:
  - type: signal
    description: metronome clicks

flags:
 - name: -mode <float>
   description: sets mode (0, 1, 2)

methods:
  - type: set <list>
    description: sets click frequencies (low, mid, high)

draft: false
---

[metronome~] works in conjunction with [metronome] and outputs metronome clicks.