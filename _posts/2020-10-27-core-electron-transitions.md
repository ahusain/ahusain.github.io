---
title: 'Core Electron Transition Energies'
date: 2020-10-27
permalink: /posts/2020/10/core-electron-transition-energies/
tags:
  - core states
  - widget
  - calculator
  - transition
---

It is useful when performing resonant x-ray scattering, x-ray absorption spectroscopy, or other core-level spectroscopies, to have a quick reference for the element-dependent electron binding energies in solids. These binding energies describe how deep the core electron levels are with respect to the Fermi level (or vacuum, top of valence band, etc.). Because chemical bonding in solids only involves valence electrons, the core levels of atoms in a solid are mostly unchanged compared to that of a free atom in space. Thus, the core level binding energies form a fingerprint uniquely identifying an element.

Values for the electron binding energies for each element are tabulated in [Section 1.1](https://xdb.lbl.gov/Section1/Sec_1-1.html) of the [X-Ray Data Booklet](https://xdb.lbl.gov/) published by the Advanced Light Source located at the Lawrence Berkeley National Laboratory. While this table lets one quickly look up binding energies, it is useful to have both the binding and transition energies in a straightforward and less congested format. Below is a simple calculator that does just that. Machine-readable tables of these binding energies are given at [this GitHub repo](https://github.com/ahusain/XDB-Electron-Binding-Energies).



{% include core-transitions-calculator.html %} 