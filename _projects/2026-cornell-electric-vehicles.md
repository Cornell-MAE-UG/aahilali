---
layout: cev
title: "Cornell Electric Vehicles"
permalink: /projects/cornell-electric-vehicles/
featured_home: true
image: https://www.cornellelectricvehicles.org/vehicles/car-mask.webp
---

<div class="cev-page">
  <section class="cev-hero">
    <div class="cev-shell">
      <h1 class="cev-page-title">Cornell Electric Vehicles</h1>
      <p class="cev-page-subtitle">General overview of my work on Cornell Electric Vehicles, with a focus on the acceleration pedal assembly and steering-system layout for the 2026 vehicle.</p>
      <div class="cev-hero-actions">
        <a class="cev-btn cev-btn-primary" href="https://www.cornellelectricvehicles.org/" target="_blank" rel="noopener">Learn More About CEV</a>
        <a class="cev-btn cev-btn-secondary" href="#cev-collage">Click here to see photos :)</a>
      </div>
      <div class="cev-hero-image-wrap"><img class="cev-hero-image" src="https://www.cornellelectricvehicles.org/vehicles/car-mask.webp" alt="Cornell Electric Vehicles competition car"></div>
    </div>
  </section>

  <section class="cev-collage-section" id="cev-collage">
    <div class="cev-shell">
      <div class="cev-collage-intro">
        <h2 class="cev-section-title">Project Gallery</h2>
        <p>A visual overview of my design, analysis, and integration work on the 2026 vehicle. Click any image to view it larger.</p>
      </div>

      <div class="cev-collage">
        <figure class="cev-tile cev-tile-wide">
          <a href="{{ '/assets/images/cev/acceleration-pedal-annotated.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/acceleration-pedal-annotated.png' | relative_url }}" alt="Acceleration pedal design overview"></a>
          <figcaption>Acceleration pedal design and packaging</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-medium">
          <a href="{{ '/assets/images/cev/back-mount-shaft-holder-ansys.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/back-mount-shaft-holder-ansys.png' | relative_url }}" alt="ANSYS equivalent stress analysis of the acceleration pedal back mount and shaft holder"></a>
          <figcaption>Back mount / shaft holder — ANSYS equivalent stress</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-tall">
          <a href="{{ '/assets/images/cev/steering-assembly-overview.jpg' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-assembly-overview.jpg' | relative_url }}" alt="Steering assembly overview"></a>
          <figcaption>Steering-system integration</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-small">
          <a href="{{ '/assets/images/cev/gas-spring-shaft-load.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/gas-spring-shaft-load.png' | relative_url }}" alt="120.1 N load applied to the gas spring shaft"></a>
          <figcaption>Gas spring shaft loading</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-small">
          <a href="{{ '/assets/images/cev/gas-spring-shaft-stress.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/gas-spring-shaft-stress.png' | relative_url }}" alt="ANSYS equivalent stress analysis of the gas spring shaft"></a>
          <figcaption>Gas spring shaft — ANSYS equivalent stress</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-wide">
          <a href="{{ '/assets/images/cev/steering-mounting-plate-layout.jpg' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-mounting-plate-layout.jpg' | relative_url }}" alt="Steering flat plate layout"></a>
          <figcaption>Steering mounting plate and subsystem layout</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-medium">
          <a href="{{ '/assets/images/cev/design-acceleration-pedal.jpg' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/design-acceleration-pedal.jpg' | relative_url }}" alt="Acceleration pedal design"></a>
          <figcaption>Acceleration pedal development</figcaption>
        </figure>
      </div>

      <div class="cev-project-notes">
        <p>I designed and manufactured a lightweight acceleration pedal and sensor mounts in Autodesk Inventor, developed a MATLAB force model to size the pedal geometry and gas-spring configuration, and verified critical hardware using ANSYS.</p>
        <p>I also led the steering-system layout for the 2026 vehicle and designed the aluminum mounting plate that creates a shared mechanical interface for the rack and pinion, pedals, autobrake, autosteer, and related hardware.</p>
      </div>
    </div>
  </section>
</div>
