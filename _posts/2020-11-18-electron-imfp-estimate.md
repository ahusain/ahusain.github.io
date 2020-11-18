---
title: 'Electron Inelastic Mean Free Path'
date: 2020-11-18
permalink: /posts/2020/11/electron-imfp-estimate/
tags:
  - inelastic
  - imfp
  - widget
  - calculator
  - egerton
---

Unlike x-ray and neutron scattering, electron scattering in a solid is often so strong that the first Born approximation is not enough to describe the distribution of scattered electrons. To understand when higher order (or multiple) scattering occurs, it is useful to have an estimate for the inelastic mean free path (IMFP) for the probe electron. Estimates for the IMFP based on material parameters is therefore a useful metric when performing Electron Energy Loss Spectroscopy (EELS). Indeed, many formulas for estimating the IMFP have been studied in the literature and are nicely compiled in [Electron Energy-Loss Spectroscopy in the Electron Microscope](https://link.springer.com/book/10.1007/978-1-4419-9583-4) by R. Egerton.

Below is a simple calculator based on the [Matlab code](https://sites.google.com/site/temsemeels/home/matlab-programs-from-eels-in-the-electron-microscope-3rd-edition) of R. Egerton to estimate the electron IMFP. To do this calculation, one inputs the chemical formula of the material of interest (written with spaces between elements), the unit cell volume, and the number of formula units of the compound in a single unit cell. Alternatively, there is the option to directly input the mass density instead of the unit cell volume and formula units per cell to perform this calculation.



{% include imfp-calculator.html %}