---
title: envelope~

description: Envelope waveforms

categories:
- object

pdcategory:

arguments:
- description: envelope symbol and optional arguments: sin, hann, tri, vsaw <float>, gauss <float>, and trapezoid <float, float>
  type: anything
  default: sin

inlets:
  1st:
  - type: float/signal
    description: phase input
  2nd:
  - type: float
    description: phase offset

outlets:
  1st:
  - type: signal
    description: envelope waveform

flags:
  - name: phase <float>
    description: phase offset (default 0)

methods:
  - type: phase <float>
    description: phase offset (from 0 to 1)
  - type: anything
    description: set envelope type and arguments: <sin>, <hann>, <tri>, <vsaw, float>, <gauss float>, and <trap float float>

draft: false
---

[envelope~] provides 6 different envelopes, which are generated via a phase input.
