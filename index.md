---
layout: page
title: ENSIM5
---

<script>
    document.title = "ensim";
</script>

<style>
body {
    background-color: #101010;
}
.site-header,
.site-footer {
    display: none;
}
</style>

We are an independent research and development team based in Vancouver, BC,
on a mission to model realistic, real-time, internal combustion
engine audio for use in the games industry.

<video controls style="width: 100%; height: auto; margin-bottom: 10px;">
    <source src="video.mp4" type="video/mp4">
</video>

Our latest `ENSIM5` alpha uses custom built proprietary, cache-friendly, single-threaded SIMD
numerical solvers to compute - in real-time with a 240 Hz controller input rate -
isentropic mass flow rates, combustion chamber thermodynamics, piston kinematics,
and computational fluid dynamics.

![](pvtv2.png)

`ENSIM5` approximates the standard C8H18 14.7:1 Air-Fuel combustion process with a hypothetical
gas of molar mass of density 0.0023kg / mol and a heat capacity ratio of 1.5. This combusts
_hot_, well into a hypothetical 7000K temperature region, to create the ultimate high harmonic
pulse train that powers a one dimensional computational fluid dynamics pipe for audio generation.
