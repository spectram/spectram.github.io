---
layout: page
permalink: /
title: Astro-know-me!
tagline: |- 
  On the day you are born, you are bestowed a phrase that
  sets you off on a lifelong mission, in search of a definition. 
has_more_link: true
more_link_text: Find out more
img_path: images/home-bg.jpg
seo:
  metatitle: Astro-know-me | Sriram Sankar
  description: |-
    PhD candidate at ICRAR bridging hydrodynamic simulations and resolved HI 21 cm observations to study how galaxies acquire gas, in preparation for SKA-Mid.
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: Astro-know-me | Sriram Sankar
      keyName: property
    - name: 'og:description'
      value: PhD candidate at ICRAR bridging hydrodynamic simulations and resolved HI 21 cm observations to study how galaxies acquire gas, in preparation for SKA-Mid.
      keyName: property
    - name: 'og:image'
      value: images/home-bg.jpg
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: Astro-know-me | Sriram Sankar
    - name: 'twitter:description'
      value: PhD candidate at ICRAR bridging hydrodynamic simulations and resolved HI 21 cm observations to study how galaxies acquire gas, in preparation for SKA-Mid.
    - name: 'twitter:image'
      value: images/home-bg.jpg
      relativeUrl: true
layout: page
---

I am a PhD candidate at the International Centre for Radio Astronomy Research (ICRAR), The University of Western Australia, supported by an ASTRO 3D scholarship and supervised by Prof. Chris Power and Prof. Barbara Catinella. I study how galaxies acquire the gas that sustains their star formation, using the 21 cm emission of neutral hydrogen (HI). My work bridges hydrodynamic simulations and resolved HI observations: I build physical models of how gas settles onto galaxy discs, carry simulated galaxies through to synthetic observations that match real surveys, and reduce and analyse MeerKAT data myself. I will submit my thesis in August 2027.

Galaxies like the Milky Way would exhaust their gas within a few billion years, yet they have formed stars for much longer. The gas that refuels them passes through the interface between the disc and the surrounding circumgalactic medium (CGM), where HI appears as extended, warped outer discs and as anomalous gas: extraplanar, lagging, or non-circular emission that does not follow the rotating disc. Deep interferometers such as [MeerKAT](https://www.sarao.ac.za/science/meerkat/), a precursor of [SKA-Mid](https://www.skao.int/en/explore/telescopes/ska-mid), now reach this faint gas in nearby galaxies. SKA-Mid will map it in far more galaxies, at higher resolution and sensitivity, and I am excited to help turn those maps into an understanding of how galaxies grow.

<div>
  <p class="read-more">
    <a class="read-more-link" href="/contact">Click here to check out my publications list and CV<span class="icon-arrow-right" aria-hidden="true"></span></a>
  </p>
</div>

---

### Theory and simulations

With [Prof. Jonathan Stern](https://www.sternjon.sites.tau.ac.il/) at Tel Aviv University, I combined analytic calculations with idealised hydrodynamic simulations to show that the hot (~10<sup>6</sup> K) atmosphere of a spiral galaxy continuously condenses onto a cool (~10<sup>4</sup> K) disc, and that a tilt between the atmosphere and the disc produces an extended, warped outer HI disc ([Sankar et al. 2026a, *MNRAS* 549](https://doi.org/10.1093/mnras/stag1059)). The mechanism explains why warps are so common and long-lived, and it turns an observed warp into a measurement of the hot atmosphere.

As a member of the [FIRE](https://fire.northwestern.edu/) collaboration, I forward-modelled six Milky Way-mass FIRE-2 galaxies into survey-matched HI cubes, tracking the simulation particles behind every spectrum, to measure how much of the anomalous gas a standard extraction recovers (Sankar et al. 2026b, to be submitted to *MNRAS*). At ICRAR, I host the Computational Theory Group.

<div>
  <p class="read-more">
    <a class="read-more-link" href="/research">Click here to read more about this work<span class="icon-arrow-right" aria-hidden="true"></span></a>
  </p>
</div>

### Observations

I am PI and technical lead of [**MeerRings**](/meerrings), a MeerKAT programme that maps HI in eight collisional ring galaxies, seven observed in 55 hours of new MeerKAT time and one from the archive. I reduced all of the data myself. For my MSc at the South African Astronomical Observatory (SAAO) and the University of Cape Town, supervised by Dr. Moses Mogotsi and Prof. Matthew A. Bershady, I developed a method that combines 3D tilted-ring modelling, Gaussian decomposition, and kinematic tagging to separate anomalous gas from rotating discs, and applied it to interacting galaxies in two groups from the MeerChoirs MeerKAT survey. I have also contributed to papers from the MAUVE programme on the Virgo cluster and from the WALLABY pilot survey on ASKAP ([Cortese et al. 2026](https://doi.org/10.1017/pasa.2026.10159); [Guimarães Silva et al. 2026](https://doi.org/10.3847/1538-4357/ae89b7)). In total, I have won over 90 hours of MeerKAT and SALT time as PI.

<div>
  <p class="read-more">
    <a class="read-more-link" href="/meerrings">Click here to read more about MeerRings<span class="icon-arrow-right" aria-hidden="true"></span></a>
  </p>
</div>
<div>
  <p class="read-more">
    <a class="read-more-link" href="/msc_thesis">Click here to read my MSc. thesis abstract and see some cool visualisations<span class="icon-arrow-right" aria-hidden="true"></span></a>
  </p>
</div>

### Computing

I have reduced MeerKAT data on two SKA Regional Centre prototypes, [ilifu](https://www.ilifu.ac.za/) in South Africa and [Setonix](https://pawsey.org.au/systems/setonix/) at the Pawsey Supercomputing Centre in Australia, using my modified version of the processMeerKAT pipeline. As a Pawsey summer intern, I benchmarked data transfer between Pawsey's Acacia object store and Setonix ([poster](https://www.youtube.com/watch?v=NMZY2zVEdrI)). I run my simulations and analysis on high-performance computing systems and contribute to open-source astronomy software, including processMeerKAT, GaussPy+, baygaud-PI, and yt_astro_analysis.

### Where I started

I entered astronomy from mechanical engineering, through quasar absorption-line spectroscopy with [Prof. Anand Narayanan](https://www.iist.ac.in/ess/anand) at the Indian Institute of Space Science and Technology (IIST). Using archival spectra from the Hubble Space Telescope and the Keck Observatory, I measured the density, temperature, and metallicity of multiphase gas around galaxies. This work produced three papers ([Pradeep, Sankar, et al. 2020](https://ui.adsabs.harvard.edu/abs/2020MNRAS.493..250P/abstract); [Sankar et al. 2020](https://ui.adsabs.harvard.edu/abs/2020MNRAS.498.4864S/abstract); [Sameer et al. 2022](https://ui.adsabs.harvard.edu/abs/2022MNRAS.510.5796S/abstract)), and my first first-author paper is featured in C.W. Churchill's [*Quasar Absorption Lines*](https://www.qsoabslines.org) textbook.

### Mentoring and community

I have supervised six students, from undergraduate to PhD level, at IIST, the University of Kerala, and SAAO/UCT. I supervise with a flat hierarchy and open communication, and I enjoy passing on what I have learnt to students who would otherwise have little access to frontier research. At ICRAR, I am a student representative; in Cape Town, I founded the [Green SAAO](/sideprojects/greensaao/) sustainability movement, organised the extragalactic discussion group, represented postgraduate students, and volunteered for public outreach.

---

### Fortunately, I am not just my work

Aside from astrophysical research, I enjoy a range of activities such as: reading philosophical novels; writing poetry; creating music; binging on - anime, sci-fi shows, and documentaries; outdoor activities such as gardening, hiking, and stargazing; and exploring open-source codes and cool software technologies. I also spend some time thinking about and working on climate action through personal lifestyle choices and pushing for systemic changes in my immediate environment.

<div>
  <p class="read-more">
    <a class="read-more-link" href="/sideprojects">Click here to read about some of my past side-projects<span class="icon-arrow-right" aria-hidden="true"></span></a>
  </p>
</div>
I have filled this website with some of the poems that I have written over the years and some images from my gallery. I have also added some of the projects that I was able to bequeath life to through dedication and hard work. In other words, I am committing a small part of myself to a GitHub repository.
<div>
  <p class="read-more">
    <a class="read-more-link" href="/thoughts">Click here to read some of my poetry<span class="icon-arrow-right" aria-hidden="true"></span></a>
  </p>
</div>
> Thoughts think me, thought I   
But, I am but a thought  
A hundred I exist  
In a hundred minds, I fit  
Zillion impressions persist  
The hundred I coexist  
Sometimes thoughts desist  
But I never resist  
For a hundred I exist  
None of which is me    
Yet, all of which is me   

<!---
I started with a Stackbit v1 theme but heavily modified it for my purpose (stackbit v2 platform is looking great, I highly recommend it).
--->
