---
title: pimp~
description: Phasor~ + imp~

categories:
 - object

pdcategory: General

arguments:
- type: float
  description: frequency in hertz
  default:
- type: float
  description: initial phase offset
  default:

inlets:
  1st:
  - type: float/signal
    description: frequency in hz
  2nd:
  - type: float/signal
    description: phase sync (ressets internal phase)
  3rd:
  - type: float/signal
    description: phase offset (modulation input)

outlets:
  1st:
  - type: signal
    description: phase signal
  2nd:
  - type: signal
    description: impulse signal (at period transitions)

---

[pimp~] is a combination of [phasor~] and [imp~] (alias of [impulse~]). It's [imp~] with an extra phase output (left outlet). The impulse happens at every phase period start (in both negative or positive frequencies/directions). It also has inlets for phase sync and phase modulation like [imp~].
