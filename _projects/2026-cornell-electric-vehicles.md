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
    <div class="cev-shell cev-gallery-layout">
      <aside class="cev-gallery-copy">
        <p class="cev-eyebrow">2025 — 2026</p>
        <h2 class="cev-section-title">Project Gallery</h2>
        <p>I designed and manufactured a lightweight acceleration pedal and sensor mounts in Autodesk Inventor. The assembly was designed to package cleanly alongside the brake pedal and mount directly to the steering flat plate while remaining lightweight, stiff, and manufacturable.</p>
        <p>I developed a static force model in MATLAB to size the pedal geometry and gas-spring configuration around a target feedback force of approximately 25 lb. The design integrates a linear potentiometer to measure pedal displacement and record position data during vehicle testing.</p>
        <p>I also evaluated critical hardware in ANSYS, including the back mount / shaft holder and gas spring shaft, to verify that stresses remained well below the yield strength of 6061-T6 aluminum.</p>
        <p>I led the steering-system layout for the 2026 vehicle and defined the packaging relationship between the rack and pinion, driver controls, pedal box, and autonomy hardware. I designed the aluminum mounting plate that creates a shared mechanical interface for the rack and pinion, pedals, autobrake, autosteer, and related hardware.</p>
      </aside>

      <div class="cev-collage">
        <figure class="cev-tile cev-tile-feature">
          <a href="{{ '/assets/images/cev/acceleration-pedal-annotated.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/acceleration-pedal-annotated.png' | relative_url }}" alt="Acceleration pedal design overview"></a>
          <figcaption>Acceleration pedal design and packaging</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-standard">
          <a href="{{ '/assets/images/cev/back-mount-shaft-holder-ansys.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/back-mount-shaft-holder-ansys.png' | relative_url }}" alt="ANSYS equivalent stress analysis of the acceleration pedal back mount and shaft holder"></a>
          <figcaption>Back mount / shaft holder — ANSYS equivalent stress</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-standard">
          <a href="{{ '/assets/images/cev/gas-spring-shaft-load.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/gas-spring-shaft-load.png' | relative_url }}" alt="120.1 N load applied to the gas spring shaft"></a>
          <figcaption>Gas spring shaft — applied load</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-standard">
          <a href="{{ '/assets/images/cev/gas-spring-shaft-stress.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/gas-spring-shaft-stress.png' | relative_url }}" alt="ANSYS equivalent stress analysis of the gas spring shaft"></a>
          <figcaption>Gas spring shaft — ANSYS equivalent stress</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-tall">
          <a href="{{ '/assets/images/cev/steering-assembly-overview.jpg' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-assembly-overview.jpg' | relative_url }}" alt="Steering assembly overview"></a>
          <figcaption>Steering-system integration</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-wide">
          <a href="{{ '/assets/images/cev/steering-mounting-plate-layout.jpg' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-mounting-plate-layout.jpg' | relative_url }}" alt="Steering flat plate layout"></a>
          <figcaption>Steering mounting plate and subsystem layout</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-standard">
          <a href="{{ '/assets/images/cev/design-acceleration-pedal.jpg' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/design-acceleration-pedal.jpg' | relative_url }}" alt="Acceleration pedal design"></a>
          <figcaption>Acceleration pedal development</figcaption>
        </figure>
      </div>
    </div>
  </section>
</div>
