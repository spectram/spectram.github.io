---
permalink: /research/
title: Research Overview
subtitle: >-
  I bridge hydrodynamic simulations and resolved HI 21 cm observations to study how galaxies acquire gas at the interface between their discs and the surrounding medium.
img_path: images/research-bg.jpg
tagline: Hoping to add a page to Humanity's book of the Cosmos
seo:
  metatitle: Research Overview | Sriram Sankar
  description: I bridge hydrodynamic simulations and resolved HI 21 cm observations to study how galaxies acquire gas at the interface between their discs and the surrounding medium.
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: Research Overview | Sriram Sankar
      keyName: property
    - name: 'og:description'
      value: >-
        I bridge hydrodynamic simulations and resolved HI 21 cm observations to study how galaxies acquire gas at the interface between their discs and the surrounding medium.
      keyName: property
    - name: 'og:image'
      value: images/research-bg.jpg
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: Research Overview | Sriram Sankar
    - name: 'twitter:description'
      value: >-
        I bridge hydrodynamic simulations and resolved HI 21 cm observations to study how galaxies acquire gas at the interface between their discs and the surrounding medium.
    - name: 'twitter:image'
      value: images/research-bg.jpg
      relativeUrl: true
layout: page
math: true
---


## How do galaxies get their gas?

Galaxies like the Milky Way would exhaust their gas within a few billion years, yet they have formed stars for much longer, so they must be refuelled ([Fraternali 2017](https://doi.org/10.1007/978-3-319-52512-9_14)). How that gas arrives sets the angular momentum it delivers, and with it how discs form, grow, and warp. Hot-mode accretion, cold flows, and galactic fountains have all been proposed, and the channels differ most at the interface between the disc and the surrounding circumgalactic medium (CGM).

The 21 cm emission of neutral hydrogen (HI) traces this interface. HI discs extend to about twice the stellar radius and are almost always warped, and around them sits anomalous gas: extraplanar, lagging, or non-circular emission that does not follow the rotating disc. Deep interferometers now detect anomalous HI routinely (e.g. [Healy et al. 2024](https://doi.org/10.1051/0004-6361/202347475); [Kurapati et al. 2025](https://doi.org/10.1093/mnras/staf387)), but a spectrum collapses rotation, non-circular motion, gas temperature, and line-of-sight position onto one velocity axis, so different physical processes can produce similar line profiles. My work bridges hydrodynamic simulations and resolved HI observations to connect what we see to the physics that produced it.

---

### Theory: a physical origin for extended, warped HI discs
***with Jonathan Stern (Tel Aviv University)***

The outer HI discs of spirals are almost always warped ([García-Ruiz et al. 2002](https://doi.org/10.1051/0004-6361:20020976)), but what drives the warps, and why they last, has not been established. Building on [Stern et al. (2024)](https://doi.org/10.1093/mnras/stae824), who showed that hot, rotating CGM inflows flatten into a disc geometry and cool at the disc–halo interface, I combined analytic calculations with idealised hydrodynamic simulations run with GIZMO. The inner hot (~10<sup>6</sup> K) atmosphere of a galaxy continuously condenses onto its cool (~10<sup>4</sup> K) disc, and a tilt between the spin of the atmosphere and the disc produces an extended, warped outer HI disc ([Sankar et al. 2026a, *MNRAS* 549, stag1059](https://doi.org/10.1093/mnras/stag1059)). The mechanism accounts for the ubiquity and longevity of warps and for the scarcity of cool gas in the inner CGM ([Marasco et al. 2025](https://doi.org/10.1051/0004-6361/202453172)). It also turns a warp into a measurement: the outer HI encodes the angular momentum and accretion rate of the hot atmosphere.

|![Temperature, HI column density, and line-of-sight velocity of a simulated galaxy accreting from a hot atmosphere tilted by 30 degrees relative to its disc](/images/sci/hot_accretion_warp.png)|
|:--:|
|*Hot-mode accretion onto a disc tilted by 30° produces an extended, warped HI disc. The panels show the gas temperature (left), HI column density (centre), and line-of-sight velocity (right) 3 Gyr into an idealised simulation, viewed edge-on. From [Sankar et al. (2026a)](https://doi.org/10.1093/mnras/stag1059).*|

---

### Forward modelling: how much anomalous gas do observations recover?
***with Chris Power, Barbara Catinella, Jonathan Stern, and the FIRE collaboration***

Testing an accretion model against resolved HI first requires knowing how much of the predicted gas an observation recovers. I measured this for six Milky Way-mass galaxies from the FIRE-2 cosmological zoom-in simulations, whose accretion follows the hot-mode picture above ([Hafen et al. 2022](https://doi.org/10.1093/mnras/stac1603); [Sultan et al. 2026](https://doi.org/10.1093/mnras/stag1117)). Two observationally motivated definitions of anomalous gas, a geometric one (gas more than twice the scale height above the disc) and a kinematic one (how closely a gas element follows circular rotation), trace largely distinct gas and assign 12% to 49% of the HI mass to anomalous gas; only the kinematic selection isolates the coherent radial inflow.

I then forward-modelled each galaxy into survey-matched HI cubes, tracking the simulation particles behind every spectrum, and applied the standard peak-masking extraction (e.g. [Marasco et al. 2019](https://doi.org/10.1051/0004-6361/201936338)). After correcting for smeared disc emission, the extraction recovers only 4% to 13% of the true anomalous gas, less than 1% of the total HI. The shortfall depends on both the extraction method and the survey depth, so no single factor converts extracted emission into the underlying anomalous gas budget. Simulations and observations can therefore be compared only after the simulated galaxies pass through the same observing and extraction steps as the data (Sankar et al. 2026b, to be submitted to *MNRAS*).

---

### Observations: anomalous gas in interacting galaxies
***with Moses Mogotsi (SAAO), Matthew Bershady (UW-Madison), and the MeerChoirs and MeerRings collaborations***

Encounters between galaxies, whether collisions, fly-bys, or mergers, displace gas from the disc and leave signatures that HI traces well beyond the stars: tidal tails, bridges, warps, and anomalous gas. These signatures record the encounter geometry and timescale, and they show how the environment moves gas in and out of galaxies.

##### MeerChoirs
*PI: Moses Mogotsi, MeerKAT Open Time (2020 and 2022)*

MeerChoirs maps the HI in nearby low-mass, late-type dominated, gas-rich groups to study how the group environment shapes galaxy evolution. For my MSc dissertation, I developed a method that separates gas at anomalous velocities from HI discs using 3D tilted-ring modelling, physically motivated Gaussian decomposition, and kinematic tagging, and applied it to two groups. The four interactions in them, two major and two minor mergers, revealed anomalous gas, non-circular flows, disturbed rotation curves, warps, extraplanar gas, tidal tails, and bridges, and the motion of the anomalous gas in the plane of the galaxies indicated gas exchange between the interacting galaxies.
<div>
  <p class="read-more">
    <a class="read-more-link" href="/msc_thesis">Click here to read my MSc. thesis abstract and see some cool visualisations<span class="icon-arrow-right" aria-hidden="true"></span></a>
  </p>
</div>

##### MeerRings
*PI and technical lead: Sriram Sankar, MeerKAT Open Time (2023)*

Collisional ring galaxies form when an intruder galaxy passes through the disc of a target galaxy, and their star formation has been studied far more than their gas. MeerRings maps the HI and L-band continuum in eight of them, seven observed in 55 hours of new MeerKAT time and one from 11 hours of archival data. It is the first deep, resolved, and systematic HI census of a sample of collisional ring galaxies, and the first systematic study of the anomalous gas produced by a well-understood class of interaction. I reduced all 66 hours of data with my modified processMeerKAT pipeline on the ilifu cloud in South Africa.
<div>
  <p class="read-more">
    <a class="read-more-link" href="/meerrings">Click here to read more about MeerRings<span class="icon-arrow-right" aria-hidden="true"></span></a>
  </p>
</div>

##### Surveys and the multiphase view

HI is one phase of the gas cycle. With the [MAUVE](https://mauve.icrar.org) collaboration, which studies galaxies in the Virgo cluster, we found cold neutral gas in the star-formation-driven outflow of NGC 4383 and evidence for a fountain flow ([Cortese et al. 2026, *PASA* 43, e034](https://doi.org/10.1017/pasa.2026.10159)). The WALLABY pilot survey on ASKAP revealed a fourth member of the ESO 179-013 system ([Guimarães Silva et al. 2026, *ApJ* 1008, 235](https://doi.org/10.3847/1538-4357/ae89b7)). I also lead a 15-hour MeerKAT programme, awarded at priority A in 2024, titled "The first multiphase study of star-formation-driven outflows below the star-forming main sequence".

---

### Looking ahead: SKA-Mid

SKA-Mid, under construction in South Africa's Karoo, will incorporate MeerKAT's dishes into a much larger array. Mapping the hydrogen reservoirs around galaxies, from which they draw gas to form stars, is a stated [SKAO science goal](https://www.skao.int/en/explore/science-goals/131/exploring-galaxy-evolution): SKA-Mid will reach the faint HI at the disc–CGM interface in far more galaxies, at higher resolution and over larger volumes than any precursor. Interpreting those data will take people who understand both the simulations and the observations, and the computing in between. I have spent my career so far building that combination, from analytic theory and hydrodynamic simulations to reducing MeerKAT data on SKA Regional Centre prototypes, and I am excited to put it to work on SKA-Mid.

---

### Foundations: multiphase gas in absorption
***with Anand Narayanan (IIST), Jane Charlton (PSU), the late Blair Savage (UW-Madison), et al.***

My research began with quasar absorption-line spectroscopy. Background quasars act as flashlights: the light picks up absorption signatures from ions in the gas it passes through, revealing the physical and chemical state of otherwise invisible gas around and between galaxies.

> Studying gas reservoirs using information conveyed by tiny ions through passerby messengers that were sent out across spacetime by distant luminous sources.

<div class="flex-container">
    <div class="text">
        <p>In <a href="https://ui.adsabs.harvard.edu/abs/2022MNRAS.510.5796S/abstract">Sameer et al. 2022</a> (fifth author), we studied the physical and chemical properties of the Leo HI Ring and the Leo I Group using HST COS observations of 11 quasar sightlines spread over a $\sim 600 \times 800$ kpc$^2$ region. We coupled cloud-by-cloud, multiphase, Bayesian ionization modeling with galaxy property information to determine the plausible origin of the absorbing gas along these sightlines.</p>
    </div>
    <div class="image">
        <img src="/images/sci/sameer+22_leo_ring.png" alt="Figure showing sightlines close to the Leo Ring from Sameer+2022">
        <p><em>Figure showing sightlines close to the Leo Ring from Sameer+2022</em></p>
    </div>
</div>

<div class="flex-container reverse">
  <div class="text">
    In my first, first-author paper (<a href="https://ui.adsabs.harvard.edu/abs/2020MNRAS.498.4864S/abstract">Sankar et al. 2020</a>), we utilized a series of diagnostic ions spanning a wide range of ionization energies (OII to OVI) to study a sample of five intermediate redshift absorbers likely tracing the CGM. We performed detailed component-by-component modeling of high-resolution UV-HST and Optical-Keck archival spectroscopic data to extract information on the small-scale metallicity-density-temperature structure of the clouds. We inferred nucleosynthetic yields that suggest a preferential enrichment from Type II SNe. Despite metal enrichment, we inferred a wide range for [O/H] in the absorbers suggesting poor small-scale mixing of metals with hydrogen. This work reports the lowest redshift intervening absorber with HeI detected, three systems with OV detected, and one system with NeV, NeVI detected along with OIII to OVI. The paper is featured in C.W. Churchill's <a href="https://www.qsoabslines.org"><em>Quasar Absorption Lines</em></a> textbook as a first detailed view of OVI absorbers at z~1.
  </div>
  <div class="image">
    <img src="/images/sci/sankar+20_components.png" alt="Figure showing multi-component fits to absorption lines from Sankar+2020">
    <p><em>Figure showing multi-component fits to absorption lines from Sankar+2020</em></p>
  </div>
</div>

In [Pradeep, Sankar, et al. (2020)](https://ui.adsabs.harvard.edu/abs/2020MNRAS.493..250P/abstract) we report a low redshift, multiphase weak-MgII analog absorber that resides in an overdense environment with an ionization structure that is remarkably similar to that of Galactic high-velocity clouds. This work demonstrates the advantage of using weak low ionization absorbers as a means to study the CGM of external galaxies. 

--- 

The header image is Arp 271, a group in the MeerChoirs sample observed with the VIMOS instrument on VLT. Credits to Juan Carlos Munoz-Mateos, ESO. 