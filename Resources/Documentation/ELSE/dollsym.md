---
title: dollsym

description: Expand dollar symbols

categories:
 - object

pdcategory: General

arguments:
- type: float
  description: (optional) depth
  default: 0
- type: symbol
  description: symbol to be expanded

inlets:
  1st:
  - type: symbol
    description: a symbol to be expanded if it contains dollar args
  - type: anything
    description: a one element symbol is also expanded
  - type: bang
    description: output expanded dollar symbol

outlets:
  1st:
  - type: symbol
    description: the expanded symbol

---

[dollsym] gets and expands the value of dollar symbols ("$0-x", "$1-y", and so on). It can also get and expand according to the the values of a parent patch with the 'depth' argument. Symbols without dollar arguments are passed through unchanged.
