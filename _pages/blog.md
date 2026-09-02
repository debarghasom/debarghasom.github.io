---
layout: page
permalink: /blog/
title: Blog
description: Notes, empirical explorations, and research animations.
nav: true
nav_order: 6
---

<style>
  .blog-entry {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 2rem;
    margin-bottom: 2.5rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid #374151;
  }
  .blog-visual {
    flex: 0 0 48%;
    max-width: 48%;
  }
  .blog-text {
    flex: 1;
  }
  .slider-box {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .slider-img {
    width: 100%;
    aspect-ratio: 16 / 10;
    object-fit: cover;
    border-radius: 8px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
    background-color: #111827;
  }
  .slider-control-row {
    width: 100%;
    margin-top: 0.75rem;
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }
  .slider-control-row input[type=range] {
    flex: 1;
    cursor: pointer;
  }
  .slider-label {
    font-size: 0.8rem;
    color: #9ca3af;
    font-family: monospace;
    white-space: nowrap;
  }
  @media (max-width: 768px) {
    .blog-entry {
      flex-direction: column;
      gap: 1.5rem;
    }
    .blog-visual {
      flex: 0 0 100%;
      max-width: 100%;
      width: 100%;
    }
  }
</style>

<div class="blog-entry">
  <div class="blog-visual">
    <div class="slider-box">
      <img id="regFrame" class="slider-img" src="{{ '/assets/img/publication_preview/uc-berkeley.png' | relative_url }}" alt="Regression Frame Slider">
      
      <div class="slider-control-row">
        <input type="range" id="regSlider" min="1" max="4" value="1" step="1" oninput="updateRegFrame(this.value)">
        <span class="slider-label" id="regFrameLabel">Frame: 1 / 4</span>
      </div>
    </div>
  </div>
  <div class="blog-text">
    <h3 style="margin-bottom: 0.4rem; font-weight: bold;">
      <a href="{{ '/blog/deposit-competition-dynamics/' | relative_url }}">Dynamic Pass-Through Across Indian Banking Groups</a>
    </h3>
    <div style="font-size: 0.85rem; color: #9ca3af; margin-bottom: 0.75rem;">
      <i class="fa-regular fa-calendar"></i> August 2026 &nbsp;&middot;&nbsp; 4 min read
    </div>
    <p style="font-size: 0.95rem; line-height: 1.6; margin-bottom: 1rem; color: #d1d5db;">
      Use the scrub bar on the left to step through each year of rate transmission following deregulation. We observe the dispersion of repo rate pass-through across public and private banks.
    </p>
    <a href="{{ '/blog/deposit-competition-dynamics/' | relative_url }}" class="badge bg-primary text-white" style="font-size: 0.85rem; text-decoration: none; padding: 6px 12px; border-radius: 4px; display: inline-flex; align-items: center; gap: 0.35rem;">
      Read Post <i class="fa-solid fa-arrow-right fa-xs"></i>
    </a>
  </div>
</div>

<script>
  // Array of image paths for the slider frames
  const regFrames = [
    "{{ '/assets/img/publication_preview/uc-berkeley.png' | relative_url }}",
    "{{ '/assets/img/publication_preview/brown-university.png' | relative_url }}",
    "{{ '/assets/img/publication_preview/harvard-university.png' | relative_url }}",
    "{{ '/assets/img/publication_preview/yale-university.png' | relative_url }}"
  ];

  function updateRegFrame(val) {
    const idx = parseInt(val, 10) - 1;
    document.getElementById('regFrame').src = regFrames[idx];
    document.getElementById('regFrameLabel').innerText = "Frame: " + val + " / " + regFrames.length;
  }
</script>


<div class="blog-entry">
  <div class="blog-visual">
    <img src="{{ '/assets/img/main_pic_1.jpeg' | relative_url }}" class="slider-img" alt="Choropleth Map Animation">
    </div>
  <div class="blog-text">
    <h3 style="margin-bottom: 0.4rem; font-weight: bold;">
      <a href="{{ '/blog/spatial-deposit-dispersion/' | relative_url }}">Visualizing State-Level Deposit Shifts Over 15 Years</a>
    </h3>
    <div style="font-size: 0.85rem; color: #9ca3af; margin-bottom: 0.75rem;">
      <i class="fa-regular fa-calendar"></i> July 2026 &nbsp;&middot;&nbsp; 6 min read
    </div>
    <p style="font-size: 0.95rem; line-height: 1.6; margin-bottom: 1rem; color: #d1d5db;">
      Choropleth heatmaps highlighting shifting deposit concentration across Indian districts. The looping animation visualizes how metropolitan centers reallocate liquidity following credit surges.
    </p>
    <a href="{{ '/blog/spatial-deposit-dispersion/' | relative_url }}" class="badge bg-primary text-white" style="font-size: 0.85rem; text-decoration: none; padding: 6px 12px; border-radius: 4px; display: inline-flex; align-items: center; gap: 0.35rem;">
      Read Post <i class="fa-solid fa-arrow-right fa-xs"></i>
    </a>
  </div>
</div>


<div class="blog-entry" style="border-bottom: none;">
  <div class="blog-visual">
    <img src="{{ '/assets/img/icon_logo_DS.png' | relative_url }}" class="slider-img" style="object-fit: contain; background: #000000; padding: 1rem;" alt="Static preview">
  </div>
  <div class="blog-text">
    <h3 style="margin-bottom: 0.4rem; font-weight: bold;">
      <a href="{{ '/blog/estimating-nested-logits/' | relative_url }}">Notes on Estimating Micro-BLP and Nested Logits</a>
    </h3>
    <div style="font-size: 0.85rem; color: #9ca3af; margin-bottom: 0.75rem;">
      <i class="fa-regular fa-calendar"></i> May 2026 &nbsp;&middot;&nbsp; 8 min read
    </div>
    <p style="font-size: 0.95rem; line-height: 1.6; margin-bottom: 1rem; color: #d1d5db;">
      A short technical guide on setting up instruments and contraction mappings when estimating banking demand using discrete choice models.
    </p>
    <a href="{{ '/blog/estimating-nested-logits/' | relative_url }}" class="badge bg-primary text-white" style="font-size: 0.85rem; text-decoration: none; padding: 6px 12px; border-radius: 4px; display: inline-flex; align-items: center; gap: 0.35rem;">
      Read Post <i class="fa-solid fa-arrow-right fa-xs"></i>
    </a>
  </div>
</div>