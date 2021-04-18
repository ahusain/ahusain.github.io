---
title: 'Chemical Mass Fractions'
date: 2021-04-17
permalink: /posts/2021/04/mass-fraction-calculator/
tags:
  - mass
  - fraction
  - molar
  - calculator
---

It is common when growing single crystals to use compounds which contain an element of interest, rather than using the pure element on its own. For example, copper in the form of CuO is often used instead of pure elemental copper, and fluorine is often used in the form of FeF<sub>2</sub> rather than dangerous fluorine gas. When using compounds rather than elements, it is useful to know the relative mass fraction of each element to calculate the mixing ratios needed to grow a particular crystal. 

Below is a calculator that takes a chemical formula as an input and returns the mass fraction of its elemental and binary components. The calculator allows one to change the weight of any component and see what total weight of the compound is needed as well as the relative weights of the other components. For example La<sub>2</sub>CuO<sub>4</sub> contains the elements La, Cu, O and binary components La<sub>2</sub>Cu, La<sub>2</sub>O<sub>4</sub>, and CuO<sub>4</sub>. Using this calculator, one can easily answer the question of how many grams of La<sub>2</sub>CuO<sub>4</sub> are needed to subply a certain number of grams of Cu metal. This type of calculation is completely trivial of course, but a making a simple arithmetic mistake in these sorts of calculations could completely ruin a reaction.

Some notes about the calculator:
- Elements in the chemical formula must be separated by spaces. So, enter BaFe<sub>2</sub>As<sub>2</sub> as "*Ba Fe2 As2*", not "*BaFe2As2*".
- Parentheses cannot be parsed. So, enter (H<sub>2</sub>O)<sub>2</sub> as "*H4O2*", not "*(H2O)2*". 
- Both integer and non-integer subscripts are valid, which means non-stoichometric compounds are acceptable.
- Repeated elements are acceptable, but they will be added together.

This calculator was requested by my good friend and crystal grower Mohamed Oudah.

{% include massfrac-calculator.html %}