---
layout: post
---
title: "Senior Project: Scientific Porosity–Permeability Crossplot"
---

# Porosity–Permeability Crossplot (Elsevier Scientific Style)

<img src="poro_perm_elsevier_style.png" width="600">

This page presents a scientific crossplot between **porosity (%)** and **permeability (mD)** generated as part of my Senior Project.  
The figure follows the visual style commonly used in **Elsevier journals** (e.g., *Marine and Petroleum Geology*, *Journal of Structural Geology*, *Fuel*) using muted color palettes, clean markers, and log-scale permeability.

---

## 📌 Dataset Description
This project uses a mixed **clastic–carbonate reservoir dataset** containing 30 core samples with the following fields:

- `Porosity (%)`
- `Permeability_mD` (log scale visualization)
- `Facies` (Sandstone_A/B/C, Carbonate_Mudstone, Wackestone, Packstone, Grainstone)
- `RockType` (Clastic / Carbonate)
- `GrainSize`
- `Depth_m`

Clastic rocks generally show higher porosity and permeability, while carbonate mudstones and wackestones exhibit extremely low permeability and form potential **caprock/baffles**.

---

## 📊 Geological Interpretation
**Key observations from the plot:**
- **Sandstone facies** cluster on the upper-right region → good reservoir quality  
- **Carbonate facies** form a low-permeability cluster → likely caprock  
- Permeability spans **over two orders of magnitude**, making log-scaling essential  
- Facies separation is consistent with typical mixed siliciclastic–carbonate systems

---

## 🧪 Python Code Used to Generate the Figure

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("mixed_clastic_carbonate_simple.csv")

plt.style.use('default')
plt.rcParams['font.family'] = 'sans-serif'
plt.rcParams['axes.linewidth'] = 0.8

elsevier_colors = [
    "#1f77b4", "#ff7f0e", "#2ca02c",
    "#d62728", "#9467bd", "#8c564b", "#e377c2"
]

facies_list = df["Facies"].unique()
colors = elsevier_colors[:len(facies_list)]

rock_markers = {"Clastic": "o", "Carbonate": "^"}

fig, ax = plt.subplots(figsize=(7,6))

for facies, color in zip(facies_list, colors):
    facies_data = df[df["Facies"] == facies]
    for rock in facies_data["RockType"].unique():
        sub = facies_data[facies_data["RockType"] == rock]
        ax.scatter(
            sub["Porosity (%)"], sub["Permeability_mD"],
            marker=rock_markers[rock], s=55, color=color,
            edgecolor="black", linewidth=0.5, alpha=0.9,
            label=f"{facies} ({rock})"
        )

ax.set_xlabel("Porosity (%)")
ax.set_ylabel("Permeability (mD)")
ax.set_yscale("log")
ax.legend(frameon=False, loc="lower right")

plt.tight_layout()
plt.savefig("poro_perm_elsevier_style.png", dpi=400)
plt.show()
