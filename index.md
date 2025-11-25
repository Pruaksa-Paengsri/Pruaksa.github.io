---
title: "Senior Project – Reservoir Porosity & Thin Section Porosity"
---

<style>
.main-wrapper {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem 1rem 4rem;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
}
.hero {
  text-align: center;
  margin-bottom: 2rem;
}
.hero h1 {
  font-size: 2.2rem;
  margin-bottom: 0.3rem;
}
.hero p {
  font-size: 1rem;
  color: #555;
}
.badge {
  display: inline-block;
  padding: 0.25rem 0.7rem;
  border-radius: 999px;
  font-size: 0.8rem;
  background: #e3f2fd;
  color: #1565c0;
  margin-bottom: 0.6rem;
}
.section-title {
  font-size: 1.35rem;
  margin-bottom: 0.4rem;
}
.card {
  background: #ffffff;
  border-radius: 14px;
  padding: 1.4rem 1.6rem;
  margin-bottom: 1.5rem;
  box-shadow: 0 4px 14px rgba(0,0,0,0.06);
}
.img-center {
  text-align: center;
  margin: 0.8rem 0;
}
.img-center img {
  max-width: 100%;
  border-radius: 12px;
}
.small-muted {
  font-size: 0.85rem;
  color: #777;
}
.button-row a {
  display: inline-block;
  margin-right: 0.6rem;
  margin-bottom: 0.4rem;
  padding: 0.35rem 0.9rem;
  border-radius: 999px;
  border: 1px solid #1976d2;
  font-size: 0.85rem;
  text-decoration: none;
  color: #1976d2;
}
.button-row a:hover {
  background: #1976d2;
  color: #fff;
}
</style>

<div class="main-wrapper">

  <div class="hero">
    <div class="badge">Senior Project · Reservoir Characterization</div>
    <h1>Porosity Projects – Logs & Thin Sections</h1>
    <p>
      Small data–to–visualisation workflows using Python and GitHub Pages, 
      connected to my senior project on reservoir quality.
    </p>
  </div>

  <!-- PART 1: Reservoir Porosity–Permeability Crossplot -->
  <div class="card">
    <div class="section-title">1. Reservoir Porosity–Permeability Crossplot</div>
    <p>
      This part uses a synthetic mixed clastic–carbonate dataset to visualise the relationship between 
      <strong>porosity (%)</strong> and <strong>permeability (mD)</strong>, similar to what is done in 
      reservoir characterization and CO₂ storage screening.
    </p>

    <div class="img-center">
      <img src="poro_perm_elsevier_style.png" alt="Porosity–Permeability Crossplot">
    </div>
    <p class="small-muted">
      Figure 1. Porosity versus permeability crossplot. Colours represent facies, and marker shapes 
      differentiate clastic and carbonate rock types. Permeability is shown in log scale.
    </p>

    <p>
      The crossplot clearly shows that sandstone facies tend to have higher porosity and permeability 
      and therefore better reservoir quality, while carbonate mudstone and wackestone cluster in 
      low-permeability ranges and are more likely to act as seals or baffles.
    </p>

    <div class="button-row">
      <a href="mixed_clastic_carbonate_simple.csv" download>Download reservoir CSV</a>
      <a href="poro_perm_crossplot.py" download>Download plotting code</a>
    </div>
  </div>

  <!-- PART 2: Thin Section Image-Based Porosity -->
  <div class="card">
    <div class="section-title">2. Thin Section Porosity from Blue-Dyed Images</div>
    <p>
      This mini project uses <strong>blue-dyed thin-section images</strong> of sample SB1_SST (sandstone, 40x) 
      and applies simple image processing in Python to estimate <strong>2D porosity (%)</strong> from pore space 
      filled with blue epoxy.
    </p>

    <div class="img-center">
      <img src="SB1_SST_40x_01_overlay.png" alt="Thin section pore overlay">
    </div>
    <p class="small-muted">
      Figure 2. Thin-section image of SB1_SST_40x_01 with pore boundaries highlighted in red. 
      Blue epoxy indicates pore space.
    </p>

    <p>
      The workflow is:
    </p>
    <ol>
      <li>Read thin-section images <code>SB1_SST_40x_01–04.jpg</code> using OpenCV.</li>
      <li>Convert the images from BGR to HSV colour space.</li>
      <li>Apply a blue colour threshold (for the epoxy) using <code>cv2.inRange()</code>.</li>
      <li>Count pore pixels vs. total pixels to estimate 2D porosity for each image.</li>
      <li>Export results to <code>porosity_results_SB1_SST.csv</code>.</li>
    </ol>

    <p>
      This is a simple image-based porosity estimate (2D), not a replacement for lab measurements, 
      but it demonstrates how thin-section images can be linked to digital analysis in Python and 
      connected back to core/log interpretation in my senior project.
    </p>

    <div class="button-row">
      <a href="porosity_results_SB1_SST.csv" download>Download thin-section CSV</a>
      <a href="pointcount.py" download>Download thin-section code</a>
    </div>
  </div>

  <!-- PART 3: Note / Future Work -->
  <div class="card">
    <div class="section-title">3. Notes & Future Ideas</div>
    <p>
      Both parts of this page are small workflows that support my main senior project on reservoir 
      characterization. The same ideas can be extended to:
    </p>
    <ul>
      <li>Compare thin-section porosity with core plug porosity and log-based porosity.</li>
      <li>Run the image-based porosity workflow on multiple facies, not just one sandstone sample.</li>
      <li>Integrate the results into a larger petrophysical or static modelling study.</li>
    </ul>
  </div>

</div>
