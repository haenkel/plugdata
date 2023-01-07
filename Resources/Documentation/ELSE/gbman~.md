---
title: gbman~
description: Gingerbread man chaotic generator

categories:
 - object

pdcategory: General

arguments:
- type: float
  description: sets frequency in hertz
  default: nyquist
- type: float
  description: sets initial feedback value of y[n-1]
  default: 1.2
- type: float
  description: initial feedback value of y[n-2]
  default: 2.1

inlets:
  1st:
  - type: float/signal
    description: frequency in hertz (negative values accepted)
  - type: list
    description: 2 floats set y[n-1] and y[n-2], respectively

outlets:
  1st:
  - type: signal
    description: gingerbread man map chaotic signal

---

[gbman~] is a gingerbread man map chaotic generator, the output is from the difference equation => y[n] = 1 + abs(y[n-1]) - y[n-2].