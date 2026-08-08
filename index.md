---
layout: page
title: ENSIM
---

<script>
    document.title = "ensim";
</script>

<p align="center"><img src="ensim5.png"></p>

<style>
body {
    background-color: #101010;
    color: #FFFFFF;
}
.post-title,
.post-header {
    color: #FFFFFF;
}
.site-header,
.site-footer {
    display: none;
}
</style>

We are an independent research and development team based in Vancouver, BC,
on a mission to model realistic, real-time, internal combustion
engine audio for use in the games industry.

<video controls style="width: 100%; height: auto; margin-top: 20px; margin-bottom: 20px;">
    <source src="video.mp4" type="video/mp4">
</video>

Our latest `ENSIM` alpha uses custom built proprietary, cache-friendly, single-threaded
numerical SIMD solvers to compute isentropic mass flow rates, combustion chamber thermodynamics,
piston kinematics, and computational fluid dynamics, all in real time. `ENSIM` approximates the standard
C₈H₁₈ 14.7:1 air-fuel combustion process using a hypothetical gas with a molar mass of 0.0023 kg/mol
and a heat-capacity ratio of 1.5.

<p align="center"><img src="pvtv2.png" style="margin-top: 0px; margin-bottom: 0px;"></p>

This gas model produces extremely high combustion temperatures, reaching well into the
hypothetical 7000 K range, to generate intense, harmonically rich pulse trains guided by
quintic cam-profile polynomials.

<p align="center"><img src="pulse2.png" style="margin-top: 20px; margin-bottom: 20px;"></p>

`ENSIM` on a 2019 business grade laptop `Intel(R) Core(TM) i7-8665U CPU @ 1.90GHz`
can execute 48000 audio samples of a 36-chamber 4-piston engine and one dimensional CFD pipe
in 0.2 seconds, entirely from a single core's L1 cache, without CPU or thread migrations,
all while accepting controller inputs at 240 Hz:

```
            0  context-switches:u       #  0.0    cs_per_second
            0  cpu-migrations:u         #  0.0    migrations_per_second
    2,376,758  L1-dcache-load-misses:u  #  0.7 %  l1d_miss_rate
       83,108  branch-misses:u          #  0.1 %  branch_miss_rate
1,627,262,496  instructions:u           #  2.2    insn_per_cycle
  362,993,860  dTLB-loads:u             #  0.0 %  dtlb_miss_rate
```

<br>

As always,

<p align="center"><img src="us2.png" style="margin-top: 20px; margin-bottom: 20px;"></p>
