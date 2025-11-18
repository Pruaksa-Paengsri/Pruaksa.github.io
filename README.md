# Pruaksa.github.io
This repository contains the complete workflow for generating a scientific porosity–permeability crossplot for mixed clastic and carbonate reservoir samples, including: • Dataset preparation (CSV) • Python plotting script using pandas/matplotlib • Scientific-style figure • GitHub Pages publishing
---
title: "Senior Project – Porosity–Permeability Crossplot"
---

<div class="main-wrapper">

<div class="hero">
  <div class="badge">Senior Project · Reservoir Characterization</div>
  <div class="hero-title">Porosity–Permeability Crossplot</div>
  <div class="hero-subtitle">
    Mixed clastic–carbonate reservoir samples visualised with Python (pandas + matplotlib)  
    and published via GitHub Pages.
  </div>
</div>

<div class="card">
  <div class="section-title">Figure 1 – Scientific Crossplot </div>
  <div class="img-center">
    <img src="poro_perm_elsevier_style.png" alt="Porosity–Permeability Crossplot">
  </div>
  <p class="small-muted">
    Figure 1. Porosity (%) versus permeability (mD, log scale) for mixed clastic–carbonate samples. 
    Colors indicate facies, while marker shapes differentiate clastic and carbonate rock types.
  </p>
</div>

<div class="card">
  <div class="section-title">Dataset Overview</div>
  <ul>
    <li><strong>Porosity (%)</strong> – core plug porosity</li>
    <li><strong>Permeability_mD</strong> – measured permeability in millidarcy (log-scaled on the plot)</li>
    <li><strong>Facies</strong> – Sandstone_A/B/C, Carbonate_Mudstone, Wackestone, Packstone, Grainstone</li>
    <li><strong>RockType</strong> – Clastic vs. Carbonate</li>
    <li><strong>Depth_m</strong> – sampling depth (m)</li>
  </ul>
  <p>
    Clastic facies generally occupy the high-porosity, high-permeability domain, 
    whereas carbonate mudstones and wackestones cluster in the low-permeability field 
    and tend to behave as caprock or baffles.
  </p>
</div>

<div class="card">
  <div class="section-title">Workflow</div>
  <ol>
    <li>Create synthetic mixed clastic–carbonate dataset (<code>mixed_clastic_carbonate_simple.csv</code>).</li>
    <li>Use <code>pandas</code> to read the dataset in Python.</li>
    <li>Plot porosity vs. permeability (log scale) with <code>matplotlib</code>, using:
      <ul>
        <li>Colors for facies</li>
        <li>Marker shapes for rock types</li>
      </ul>
    </li>
    <li>Export the figure as <code>poro_perm_elsevier_style.png</code>.</li>
    <li>Publish the result and description on this GitHub Pages site.</li>
  </ol>
</div>

<div class="card">
  <div class="section-title">Project Note</div>
  <p>
    This page is part of my Senior Project deliverables. It demonstrates the full workflow from 
    <strong>data preparation → scientific visualisation → web presentation</strong> for reservoir characterization 
    and CO₂ storage–related studies.
  </p>
</div>

</div>
