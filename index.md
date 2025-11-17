---
title: "Senior Project – Porosity–Permeability Crossplot"
---

# Porosity–Permeability Crossplot (Elsevier Style)

<img src="poro_perm_elsevier_style.png" width="650">

This page presents a scientific crossplot between **porosity (%)** and **permeability (mD)** generated as part of my senior project.  
The figure follows an **Elsevier-style** layout using Python (`pandas` + `matplotlib`).

---

## Dataset Overview

This dataset contains mixed **clastic–carbonate reservoir samples** with the following fields:

- `Porosity (%)`
- `Permeability_mD` (visualized on a log scale)
- `Facies` (Sandstone_A/B/C, Carbonate_Mudstone, Wackestone, Packstone, Grainstone)
- `RockType` (Clastic / Carbonate)
- `GrainSize`
- `Depth_m`

Clastic facies (sandstones) generally show higher porosity and permeability, while carbonate mudstones and wackestones have very low permeability and may act as **caprock or flow barriers**.

---

## Geological Interpretation

From the crossplot:

- **Sandstone facies** cluster in the high-porosity, high-permeability region → good reservoir quality.
- **Carbonate facies** form a low-permeability cluster → more suitable as caprock or baffles.
- Permeability spans more than two orders of magnitude, so a **logarithmic scale** on the Y-axis is required to visualize the trend properly.

---

## Python Workflow (Summary)

1. Read CSV file (`mixed_clastic_carbonate_simple.csv`) using `pandas`
2. Plot porosity vs. permeability using `matplotlib`
3. Use different colors for each **Facies**
4. Use different marker shapes for **RockType** (Clastic vs. Carbonate)
5. Save the figure as `poro_perm_elsevier_style.png`
6. Publish the figure and description here via **GitHub Pages**

---

_This page is part of my Senior Project workflow:  
**Data preparation → Python visualization → Web presentation (GitHub Pages).**_
