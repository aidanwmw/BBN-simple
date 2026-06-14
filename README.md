# BBN-simple: How to Bake a Universe-Sized Cake

[![arXiv](https://img.shields.io/badge/arXiv-2412.07893-b31b1b.svg)](https://arxiv.org/abs/2412.07893)
![Python](https://img.shields.io/badge/python-3.8%2B-blue)

> A pedagogical, from-scratch Big Bang Nucleosynthesis code aimed at an advanced undergraduate or beginning graduate level.

Paper: [arXiv:2412.07893](https://arxiv.org/abs/2412.07893)

## Abstract

Big Bang Nucleosynthesis (BBN), the process of creation of lightest elements in the early universe, is a highly robust, precise, and ultimately successful theory that forms one of the three pillars of the standard hot-Big-Bang cosmological model. Existing theoretical treatments of BBN and the associated computer codes are accurate and flexible, but are typically highly technical and opaque, and not suitable for pedagogical understanding of the BBN. Here we present BBN-simple, a from-scratch, minimum requirement, numerical calculation of the lightest element abundances pitched at an advanced undergraduate or beginning graduate level.

## Background

In the first few minutes after the Big Bang, the universe was hot and dense enough for nuclear reactions to fuse protons and neutrons into the lightest elements: deuterium, helium-3, helium-4, tritium, lithium-7, and beryllium-7. This process, known as Big Bang Nucleosynthesis, is one of the three pillars of the standard cosmological model. While production-grade BBN codes (e.g., ParthenoPE, AlterBBN) are highly accurate with many nuances and higher-order corrections, their complexity makes them difficult to use as teaching tools. BBN-simple strips the problem down to its essential physics, with every equation explained and every line of code visible.

## Repository Contents

- `bbn-simple.ipynb` — The complete, self-contained BBN calculation as a Jupyter notebook using rates from REACLIB
- `README.md` — This file

The notebook is also hosted as a browsable HTML page [here](http://aidanwmw.github.io).

## Notebook Overview

The notebook walks through every step of a BBN calculation:

1. **Thermodynamics & the Time–Temperature Relation** — Solving the Friedmann equations to relate cosmic time to photon/neutrino temperature. Includes full Fermi–Dirac integrals for electron/positron energy density via Gauss–Laguerre quadrature.

2. **Weak Reactions (n $\leftrightarrow$ p)** — Neutron–proton interconversion via the weak interaction, with temperature-dependent rates and the final neutron freeze-out abundance.

3. **Nuclear Statistical Equilibrium (NSE)** — Saha-like equations for deuterium, tritium, helium-3, and helium-4, used for the initial conditions of our abundance equations.

4. **Full Nuclear Network** — Coupled ODE integration of all major species (n, p, d, t, He-3, He-4, Li-7, Be-7) using REACLIB strong reaction rate fits.

5. **Results** — The classic BBN abundance-vs-time plot, showing the freeze-out of each species and their (approximate) final primordial abundances.

## Results

![Abundance evolution](figures/)

The code reproduces the standard BBN results: Yp $\approx 0.24$, D/H $\approx$ 2.6 \times 10^{-5}$, in reasonable agreement with precision codes like ParthenoPE and AlterBBN, given our approximations (see the paper for detailed comparison).

## Citing

If you use this code or the associated paper, please cite:

```bibtex
@article{Meador-Woodruff:2024bbn,
    author = "Meador-Woodruff, Aidan and Huterer, Dragan",
    title = "{BBN-simple: How to Bake a Universe-Sized Cake}",
    eprint = "2412.07893",
    archivePrefix = "arXiv",
    primaryClass = "astro-ph.CO",
    year = "2024"
}
```

Contact
- Aidan Meador-Woodruff — ameadorw@ur.rochester.edu
- Dragan Huterer — huterer@umich.edu

For code-specific questions or errata, please email Aidan Meador-Woodruff.
