---
bigimg: /img/trappist1f.jpg
layout: page
title: Maël Voyer
subtitle: Commissariat à l'énergie atomique (CEA) - Paris-Cité University
css: /custom/main.css

---

Hey, I am Maël a PhD student at CEA in Saclay. I focus on the properties of exoplanet atmospheres and improving the data reduciton for JWST MIRI-LRS and NIRSpec IFU. 

---

**New aerosol grid available for water ice!**

---

### New paper, TauREx plugin and dataset.

<img src="/img/taurex_pcq_logo.png" 
     alt="TauREx-PCQ logo" 
     width="220" 
     align="right"
     style="margin-left: 20px; margin-bottom: 10px;" />

I recently published a new paper about how we implement clouds models in atmospheric retrievals: Voyer & Changeat [(2026)](https://arxiv.org/abs/2601.14177). In study we show that we can get rid of the computationnaly expensive Mie theory by linearising it. We pre-compute grids of extinction, scattering and asymmetry coefficients for seven species (Silicates, Titan tholins). This provides a significant speed-ups and scaling in retrievals. Compared to retrievals using on the fly Mie theory we obtained speed-ups from 1,4 to 2.3 for single cloud retrievals. However, for retrievals with four clouds we achieved a speed-up of **17 times**. The grids are freely available [Zenodo](https://zenodo.org/records/17456673) as well as a TuREx plugin: TauREx-PCQ that utilizes them ([soure code](https://github.com/groningen-exoatmospheres/taurex-PCQ/)) available from Pypi: `pip install taurex-pcq`.

---

### Research Interests
My research interests include:
- Physics, chemistry and everything related to exoplanets and their formation.
- Bayesian retrieval methods.
- JWST instruments (MIRI, NIRSpec, etc.), ARIEL, PLATO, ELT
- Science.

## Curriculum Vitae

---

### Contact
Email : mael.voyer@cea.fr     <br />
**PhD student** <br />
Astrophysics Department, CEA & Paris-Cité University <br />
Orme des meirisiers<br />
Gif-sur-Yvette <br />
France     <br />
