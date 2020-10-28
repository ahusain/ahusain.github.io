---
title: 'Useful Calculator for the Diffraction Kinematics of Relativistic Electrons'
date: 2020-10-12
permalink: /posts/2020/10/relativistic-electron-kinematics/
tags:
  - electron beam 
  - widget
  - calculator
---

When dealing with electron diffraction within an electron microscope, it is often useful to have a quick converter to convert between the beam energy, angles, and reciprocal lattice units (r.l.u.). Below is a simple calculator that converts between electron beam energies, angles, and momentum transfer. For added benefit, there is also a lattice parameter option to present the momentum transfer in reciprocal lattice units where $1\textrm{ r.l.u.} = 2\pi/a$ and $a$ is the lattice parameter.

Some notes
- $k_i$ is the incident electron wavevector 
- $q$ is the momentum transfer. The small angle approximation is *not* assumed, so the momentum transfer is given by $q = 2k_i \sin(\theta/2)$ where $\theta$ is the scattering angle. 
- Momentum (or more accurately the wavevector) is presented according to two different conventions. 
    * The *physicist* convention which uses the reduced Planck's constant $\hbar$, such that $p=\hbar k_i$ and $\textrm{KE}=\frac{\hbar^2 k^2}{2m}$. Denoted in the table as $k_i = 2\pi/\lambda$ (or $q = 2\pi/\lambda$). 
    * The *crystallographer* convention which uses the ordinary Planck's constant $h$ so that $p=h k$. Denoted in the table as $k_i = 1/\lambda$ (or $q = 1/\lambda$).

{% include electron-conversion-table.html %} 