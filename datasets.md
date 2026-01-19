---
layout: page
title: Datasets
subtitle: 
---

# Pre-computed extinction, scattering, and asymmetry grids for aerosols

Understanding clouds and aerosols is essential for interpreting exoplanet and brown-dwarf spectra, especially with the high information content delivered by JWST and upcoming population missions such as ARIEL.
In atmospheric retrieval frameworks, cloud opacities are commonly computed using Mie theory, which relies on repeated evaluations of the Lorenz–Mie equations across particle sizes and wavelengths. These calculations are computationally expensive and often dominate retrieval run time, particularly when multiple cloud species are included.

To overcome this limitation, we developed pre-computed grids of aerosol optical properties for seven condensate species relevant to exoplanet atmospheres (silicates and Titan tholins).
For each species, we pre-compute:
- the extinction efficiency Q_ext,
- the scattering efficiency Q_scat,
- and the asymmetry parameter g,

over a wide range of particle radii (1 nm to 30 microns) and wavelengths (0.3–50 µm).

During a retrieval, these quantities are obtained via linear interpolation within the grids rather than computed on the fly. This approach is effectively equivalent to linearising Mie theory with respect to particle radius, while preserving numerical accuracy.
The specific species already released are:

- Mg2SiO4 amorph sol − gel,
- MgSiO3 amorph glass,
- MgSiO3 amorph sol − gel,
- SiO2 alpha,
- SiO2 amorph,
- SiO,
- Titan tholins.

These grids provide:
-	Orders-of-magnitude speed-up:
Retrievals become significantly faster, especially when multiple cloud species are included. In our benchmarks, four-cloud retrievals were up to 17× faster than equivalent models using direct Mie calculations.

- Excellent numerical accuracy:
We carefully control interpolation errors, ensuring relative errors below $10^{-4}$. Tests on synthetic JWST- and ARIEL-like datasets show no measurable impact on retrieved atmospheric parameters.

- Scales effortlessly with the number of cloud species:
Unlike direct Mie calculations, computation time does not increase exponentially with the number of cloud species, making this approach well suited for population studies and high-dimensional retrievals.

- Compatible with both retrievals and self-consistent models:
Although current free retrievals mainly use $Q_\mathrm{ext}$, the inclusion of $Q_\mathrm{scat}$ and $g$ makes these grids directly applicable to more advanced radiative-transfer and cloud models.

Access to the data

All grids are freely available on Zenodo:

👉 [](https://doi.org/10.5281/zenodo.17456673)

We also provide TauREx-PCQ ([](https://github.com/groningen-exoatmospheres/taurex-PCQ)), a public plugin that integrates these grids directly into the TauREx atmospheric retrieval framework, enabling fast and scalable cloud modelling with minimal user overhead.

---
