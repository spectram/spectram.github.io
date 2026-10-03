---
permalink: /computing/
title: Data, software and computing
subtitle: >-
  SKA-era HI science depends as much on moving, reducing, and modelling data as on the telescopes. I reduce my own interferometric data, run my own simulations, and have worked inside a national supercomputing centre.
img_path: images/telescopes/sriram_mkt_2022.jpg
seo:
  metatitle: Data, software and computing | Sriram Sankar
  description: >-
    MeerKAT data reduction on SKA Regional Centre prototypes, a Pawsey Supercomputing Centre internship on research data workflows, simulations on HPC, and open-source software.
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: Data, software and computing | Sriram Sankar
      keyName: property
    - name: 'og:description'
      value: >-
        MeerKAT data reduction on SKA Regional Centre prototypes, a Pawsey Supercomputing Centre internship on research data workflows, simulations on HPC, and open-source software.
      keyName: property
    - name: 'og:image'
      value: images/telescopes/sriram_mkt_2022.jpg
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: Data, software and computing | Sriram Sankar
    - name: 'twitter:description'
      value: >-
        MeerKAT data reduction on SKA Regional Centre prototypes, a Pawsey Supercomputing Centre internship on research data workflows, simulations on HPC, and open-source software.
    - name: 'twitter:image'
      value: images/telescopes/sriram_mkt_2022.jpg
      relativeUrl: true
layout: page
---

<div class="sr-stats">
  <div class="sr-stat"><span class="num">66 h</span><span class="lbl">of MeerKAT data reduced for MeerRings</span></div>
  <div class="sr-stat"><span class="num">2</span><span class="lbl">SKA Regional Centre prototypes: ilifu and Setonix</span></div>
  <div class="sr-stat"><span class="num">4</span><span class="lbl">data-transfer tools benchmarked at Pawsey</span></div>
</div>

## MeerKAT data on SKA Regional Centre prototypes

For my MSc at the South African Astronomical Observatory, I built a MeerKAT data-reduction and HI analysis pipeline for interacting galaxies in two groups from the MeerChoirs survey. I then reduced all 66 hours (17 tracks) of [MeerRings](/meerrings/) data with a modified version of the [processMeerKAT](https://idia-pipelines.github.io/docs/processMeerKAT) pipeline on [ilifu](https://www.ilifu.ac.za/), South Africa's SKA Regional Centre prototype, under an HPC allocation I secured.

Since moving to Perth, I have refactored processMeerKAT to run on [Setonix](https://pawsey.org.au/systems/setonix/) at the Pawsey Supercomputing Centre, a second SKA Regional Centre prototype, and I maintain that version. Beyond my own programmes, I reduce MeerKAT data for several collaborations and single-source programmes.

## Pawsey Supercomputing Centre summer internship

*Nov 2025 to Feb 2026 · supervised by Gregory Orange and Luke Edwards*

I was selected from over 700 applicants for a summer internship at Pawsey, one of Australia's two Tier-1 high-performance computing facilities. My project, *Optimising research data workflows with object storage environments*, asked how researchers should move data between Pawsey's Acacia object store and the Setonix supercomputer, the kind of data movement that sits at the centre of any SKA Regional Centre.

<div class="sr-cards">
  <div class="sr-card">
    <h4>Benchmarks</h4>
    <p>I benchmarked four transfer tools, AWS CLI v2, s5cmd, rclone, and Globus, on three representative dataset classes: single large files, heterogeneous directory trees, and homogeneous multi-file sets. I measured throughput, run-to-run variability, and failure modes within typical user allocations on Setonix.</p>
  </div>
  <div class="sr-card">
    <h4>Tuning and integrity</h4>
    <p>I tuned the transfer clients (concurrency, parallelism, multipart uploads), derived an optimised rclone profile for Setonix, and compared integrity-checking strategies to balance reliability against peak throughput.</p>
  </div>
  <div class="sr-card">
    <h4>Outcomes</h4>
    <p>I turned the results into user-facing guidance on tool choice and configuration for Pawsey's documentation, proposed improvements to its data portal, and applied the findings to resolve data-movement bottlenecks in a live research workflow.</p>
  </div>
</div>

I presented the project at the internship showcase ([video](https://www.youtube.com/watch?v=NMZY2zVEdrI)).

## Simulations and analysis at scale

I ran idealised hydrodynamic simulations of hot-mode accretion with GIZMO on AWS EC2 ([Sankar et al. 2026a](https://doi.org/10.1093/mnras/stag1059)), and I analyse FIRE-2 cosmological zoom-in simulations and turn them into survey-matched synthetic HI cubes on HPC systems.

Systems I have worked on:

<ul class="sr-tags">
  <li><a href="https://pawsey.org.au/systems/setonix/">Setonix</a></li>
  <li>Acacia</li>
  <li><a href="https://www.ilifu.ac.za/">ilifu</a></li>
  <li><a href="https://supercomputing.swin.edu.au/docs/">OzSTAR</a></li>
  <li><a href="https://www.opencadc.org/science-containers/">CANFAR</a></li>
  <li><a href="https://aws.amazon.com/ec2/">AWS EC2</a></li>
  <li>Hyades</li>
  <li>Astro3</li>
</ul>

## Software

<div class="sr-cards">
  <div class="sr-card">
    <h4>processMeerKAT</h4>
    <p>The IDIA MeerKAT calibration and imaging pipeline. I maintain a refactor that runs on Setonix at Pawsey.</p>
    <p><a href="https://github.com/spectram/pipelines">My fork</a> · <a href="https://github.com/idia-astro/pipelines">Upstream</a></p>
  </div>
  <div class="sr-card">
    <h4>GaussPy+</h4>
    <p>Automated Gaussian decomposition of emission-line spectra, which I use to separate anomalous gas from rotating discs in HI cubes. I maintain a refactor.</p>
    <p><a href="https://github.com/spectram/gausspyplus">My fork</a> · <a href="https://github.com/mriener/gausspyplus">Upstream</a></p>
  </div>
  <div class="sr-card">
    <h4>Contributions</h4>
    <p>Contributions to <a href="https://github.com/seheon-oh/baygaud-PI">baygaud-PI</a>, a Bayesian line-profile decomposition code, and to <a href="https://github.com/yt-project/yt_astro_analysis">yt_astro_analysis</a>, the astrophysical analysis extension to yt.</p>
  </div>
</div>

Tools I use day to day:

<ul class="sr-tags">
  <li>Python</li><li>Bash</li><li>C/C++</li><li>SLURM</li><li>Docker</li><li>Git</li>
  <li>CASA</li><li>CARTA</li><li>SoFiA-2</li><li>3D-Barolo</li><li>GIZMO</li><li>yt</li><li>Cloudy</li><li>Astropy</li>
</ul>
