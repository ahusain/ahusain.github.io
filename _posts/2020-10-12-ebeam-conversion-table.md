---
title: 'Relavistic Electron Momentum-Angle-Energy Conversion Table'
date: 2020-10-12
permalink: /posts/2020/10/blog-post-1/
tags:
  - electron
  - widget
---

Below is a simple calculator to go between electron beam energies, angles, and momentum transfer

Conversion Table
======

<html><body dir="ltr"><font face="arial">
<table style="border-width:1px" cellpadding="2" bordercolor="#CCCCCC" align="center">
<form name="conversion">
<tbody>
<tr>
<td colspan="1" class="label">Incident e-Beam</td> 
<td colspan="1" class="label">Momentum Transfer</td>
<td colspan="1" class="label">Lattice Parameter</td>
</tr>
<tr>
<td><span style="font-size:10pt"><input name="keV" onkeyup="keVconvert()" size="8" value="80.00"> keV </span></td>
<td><span style="font-size:10pt"><input name="mrad" onkeyup="mradconvert()" size="8" value="0.500"> mrad </span></td>
<td><span style="font-size:10pt"><input name="alatt" onkeyup="alattconvert()" size="8" value="3.81"> Å </span></td>
</tr>
<tr>
<td><span style="font-size:10pt"><input name="kPhys" onkeyup="kPhysconvert()" size="8" value="150.47"> Å<sup>-1</sup> (k<sub>i</sub> = 2π/λ) </span></td>
<td><span style="font-size:10pt"><input name="qPhys" onkeyup="qPhysconvert()" size="8" value="0.07523"> Å<sup>-1</sup> (q = 2π/λ) </span></td>
</tr>
<tr>
<td><span style="font-size:10pt"><input name="kCrys" onkeyup="kCrysconvert()" size="8" value="23.948"> Å<sup>-1</sup> (k<sub>i</sub> = 1/λ) </span></td>
<td><span style="font-size:10pt"><input name="qCrys" onkeyup="qCrysconvert()" size="8" value="0.01197"> Å<sup>-1</sup> (q = 1/λ) </span></td>
</tr>
<tr>
<td><span style="font-size:10pt"><input name="kAng" onkeyup="kAngconvert()" size="8" value="0.04176"> Å (λ) </span>
<td><span style="font-size:10pt"><input name="qAng" onkeyup="qAngconvert()" size="8" value="83.520"> Å (λ)</span>
</tr>
<tr>
<td><span style="font-size:10pt"><input name="kpm" onkeyup="kpmconvert()" size="8" value="4.1760"> pm (λ)</span>
<td><span style="font-size:10pt"><input name="qnm" onkeyup="qnmconvert()" size="8" value="835.20"> nm (λ)</span></td>
</tr>
<tr>
<td><span style="font-size:10pt"><input name="beta" onkeyup="betaconvert()" size="8" value="0.50237"> β = v/c</span></td>
<td><span style="font-size:10pt"><input name="qrlu" onkeyup="qrluconvert()" size="8" value="0.04562"> r.l.u</span></td>
</tr>
<tr>
<td><span style="font-size:10pt"><input name="gamma" onkeyup="gammaconvert()" size="8" value="1.15653"> γ</span></td>
</tr>
</tbody>
</form>
<script language="javascript">
c=299792458;
h=4.135667516e-15;
hc=1.97326963; // hbar*c in keV*Angstrom
mc2=510.99891; //mc^2 of electron in keV
PI=Math.PI;
function roundfive(num){
round = (Math.round(num*100000))/100000
//round = Math.round((num + 0.001) * 100000) / 100000
return (+round.toFixed(5))
}
function roundall(){
with (document.conversion){
keV.value   = roundfive(keV.value)
kPhys.value = roundfive(kPhys.value)
kCrys.value = roundfive(kCrys.value)
kAng.value  = roundfive(kAng.value )
kpm.value   = roundfive(kpm.value)
gamma.value = roundfive(gamma.value)
beta.value  = roundfive(beta.value)

mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function keVconvert(){
with (document.conversion){
kPhys.value = (1.0/hc)*Math.sqrt(keV.value*keV.value + 2*mc2*keV.value)
kCrys.value = kPhys.value/(2*PI)
kAng.value  = 1.00/kCrys.value
kpm.value   = 100*kAng.value
gamma.value = (keV.value/mc2)+1.00
beta.value  = Math.sqrt(gamma.value*gamma.value - 1)/(gamma.value)
mradconvert()
kPhys.value = roundfive(kPhys.value)
kCrys.value = roundfive(kCrys.value)
kAng.value  = roundfive(kAng.value )
kpm.value   = roundfive(kpm.value)
gamma.value = roundfive(gamma.value)
beta.value  = roundfive(beta.value)
mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function kPhysconvert(){
with (document.conversion){
keV.value = Math.sqrt(mc2*c2+(hc*kPhys.value)*(hc*kPhys.value)) - mc2
kCrys.value = kPhys.value/(2*PI)
kAng.value  = 1.00/kCrys.value
kpm.value   = 100*kAng.value
gamma.value = (keV.value/mc2)+1.00
beta.value  = Math.sqrt(gamma.value*gamma.value - 1)/(gamma.value)
mradconvert()
keV.value   = roundfive(keV.value)
kCrys.value = roundfive(kCrys.value)
kAng.value  = roundfive(kAng.value )
kpm.value   = roundfive(kpm.value)
gamma.value = roundfive(gamma.value)
beta.value  = roundfive(beta.value)
mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function kCrysconvert(){
with (document.conversion){
kPhys.value = 2*PI*kCrys.value
keV.value = Math.sqrt(mc2*mc2+(hc*kPhys.value)*(hc*kPhys.value)) - mc2
kAng.value  = 1.00/kCrys.value
kpm.value   = 100*kAng.value
gamma.value = (keV.value/mc2)+1.00
beta.value  = Math.sqrt(gamma.value*gamma.value - 1)/(gamma.value)
mradconvert()
keV.value   = roundfive(keV.value)
kPhys.value = roundfive(kPhys.value)
kAng.value  = roundfive(kAng.value )
kpm.value   = roundfive(kpm.value)
gamma.value = roundfive(gamma.value)
beta.value  = roundfive(beta.value)
mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function kAngconvert(){
with (document.conversion){
kCrys.value = 1.00/kAng.value
kPhys.value = 2*PI*kCrys.value
keV.value = Math.sqrt(mc2*mc2+(hc*kPhys.value)*(hc*kPhys.value)) - mc2
kpm.value   = 100*kAng.value
gamma.value = (keV.value/mc2)+1.00
beta.value  = Math.sqrt(gamma.value*gamma.value - 1)/(gamma.value)
mradconvert()
keV.value   = roundfive(keV.value)
kPhys.value = roundfive(kPhys.value)
kCrys.value = roundfive(kCrys.value)
kpm.value   = roundfive(kpm.value)
gamma.value = roundfive(gamma.value)
beta.value  = roundfive(beta.value)
mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function kpmconvert(){
with (document.conversion){
kAng.value = kpm.value/100.00
kCrys.value = 1.00/kAng.value
kPhys.value = 2*PI*kCrys.value
keV.value = Math.sqrt(mc2*mc2*+(hc*kPhys.value)*(hc*kPhys.value)) - mc2
gamma.value = (keV.value/mc2)+1.00
beta.value  = Math.sqrt(gamma.value*gamma.value - 1)/(gamma.value)
mradconvert()
keV.value   = roundfive(keV.value)
kPhys.value = roundfive(kPhys.value)
kCrys.value = roundfive(kCrys.value)
kAng.value   = roundfive(kAng.value)
gamma.value = roundfive(gamma.value)
beta.value  = roundfive(beta.value)
mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function gammaconvert(){
with (document.conversion){
keV.value   = (gamma.value -1)*mc2
kPhys.value = (1.0/hc)*Math.sqrt(keV.value*keV.value + 2*mc2*keV.value)
kCrys.value = kPhys.value/(2*PI)
kAng.value  = 1.00/kCrys.value
kpm.value   = 100*kAng.value
beta.value  = Math.sqrt(gamma.value*gamma.value - 1)/(gamma.value)
mradconvert()
keV.value   = roundfive(keV.value)
kCrys.value = roundfive(kCrys.value)
kAng.value  = roundfive(kAng.value )
kpm.value   = roundfive(kpm.value)
beta.value  = roundfive(beta.value)
kPhys.value = roundfive(kPhys.value)
mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function betaconvert(){
with (document.conversion){
gamma.value  = Math.sqrt(1.0/(1-beta.value*beta.value*))
keV.value   = (gamma.value -1)*mc2
kPhys.value = (1.0/hc)*Math.sqrt(keV.value*keV.value + 2*mc2*keV.value)
kCrys.value = kPhys.value/(2*PI)
kAng.value  = 1.00/kCrys.value
kpm.value   = 100*kAng.value
mradconvert()
keV.value   = roundfive(keV.value)
kCrys.value = roundfive(kCrys.value)
kAng.value  = roundfive(kAng.value )
kpm.value   = roundfive(kpm.value)
gamma.value = roundfive(gamma.value)
kPhys.value = roundfive(kPhys.value)
mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function mradconvert(){
with (document.conversion){
qPhys.value = kPhys.value*mrad.value*(1e-3)
qCrys.value = kCrys.value*mrad.value*(1e-3)
qAng.value  = 1.00/qCrys.value
qnm.value   = 10*qAng.value 
qrlu.value = alatt.value/qAng.value
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function qPhysconvert(){
with (document.conversion){
mrad.value = (1e3)*qPhys.value/kPhys.value
qCrys.value = kCrys.value*mrad.value*(1e-3)
qAng.value  = 1.00/qCrys.value
qnm.value   = 10*qAng.value 
qrlu.value = alatt.value/qAng.value
mrad.value  = roundfive(mrad.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function qCrysconvert(){
with (document.conversion){
mrad.value = (1e3)*qCrys.value/kCrys.value
qPhys.value = kPhys.value*mrad.value*(1e-3)
qAng.value  = 1.00/qCrys.value
qnm.value   = 10*qAng.value 
qrlu.value = alatt.value/qAng.value
mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function qAngconvert(){
with (document.conversion){
qCrys.value = 1.00/qAng.value
mrad.value  = (1e3)*qCrys.value/kCrys.value
qPhys.value = kPhys.value*mrad.value*(1e-3)
qnm.value   = 10*qAng.value 
qrlu.value  = alatt.value/qAng.value
mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function qnmconvert(){
with (document.conversion){
qAng.value  = qnm.value/10.0
qCrys.value = 1.00/qAng.value
mrad.value  = (1e3)*qCrys.value/kCrys.value
qPhys.value = kPhys.value*mrad.value*(1e-3)
qrlu.value  = alatt.value/qAng.value
mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qrlu.value  = roundfive(qrlu.value)
alatt.value = roundfive(alatt.value)
}}
function qrluconvert(){
with (document.conversion){
qAng.value  = alatt.value/qrlu.value
qCrys.value = 1.00/qAng.value
mrad.value  = (1e3)*qCrys.value/kCrys.value
qPhys.value = kPhys.value*mrad.value*(1e-3)
qnm.value   = 10*qAng.value 
mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
}}
function alattconvert(){
with (document.conversion){
qrlu.value  = alatt.value/qAng.value
mrad.value  = roundfive(mrad.value)
qPhys.value = roundfive(qPhys.value)
qCrys.value = roundfive(qCrys.value)
qAng.value  = roundfive(qAng.value)
qnm.value   = roundfive(qnm.value)
qrlu.value  = roundfive(qrlu.value)
}}
</script>
</font>
</body></html>