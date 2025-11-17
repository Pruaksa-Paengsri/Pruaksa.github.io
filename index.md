---
title: "Senior Project – Porosity–Permeability Crossplot"
---

<style>
.main-wrapper {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem 1rem 4rem;
}
.hero {
  text-align: center;
  margin-bottom: 2rem;
}
.hero-title {
  font-size: 2.2rem;
  margin-bottom: 0.5rem;
}
.hero-subtitle {
  font-size: 1.05rem;
  color: #555;
}
.badge {
  display: inline-block;
  padding: 0.2rem 0.6rem;
  border-radius: 999px;
  font-size: 0.8rem;
  background: #e3f2fd;
  color: #1565c0;
  margin-bottom: 0.75rem;
}
.section-title {
  font-size: 1.3rem;
  margin-top: 1.8rem;
  margin-bottom: 0.6rem;
}
.card {
  background: #ffffff;
  border-radius: 12px;
  padding: 1.2rem 1.4rem;
  box-shadow: 0 4px 12px rgba(0,0,0,0.06);
  margin-bottom: 1.4rem;
}
.img-center {
  text-align: center;
  margin: 1rem 0;
}
.img-center img {
  max-width: 100%;
  border-radius: 10px;
  box-shadow: 0 4px 16px rgba(0,0,0,0.15);
}
.small-muted {
  font-size: 0.85rem;
  color: #777;
}
</style>

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
