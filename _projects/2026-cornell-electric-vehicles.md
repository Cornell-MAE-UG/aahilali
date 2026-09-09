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

        <figure class="cev-tile cev-tile-wide">
          <a href="{{ '/assets/images/cev/steering-layout-subsystems.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-layout-subsystems.png' | relative_url }}" alt="Steering system physical layout and subsystem packaging"></a>
          <figcaption>Steering-system subsystem packaging and physical layout</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-wide">
          <a href="{{ '/assets/images/cev/steering-layout-cad-comparison.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-layout-cad-comparison.png' | relative_url }}" alt="Steering system physical and CAD layout comparison"></a>
          <figcaption>Physical steering layout compared with the CAD assembly</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-portrait">
          <a href="{{ '/assets/images/cev/steering-linkage-clearance.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-linkage-clearance.png' | relative_url }}" alt="Steering linkage clearance detail"></a>
          <figcaption>Steering linkage packaging and clearance detail</figcaption>
        </figure>

        <figure class="cev-tile">
          <a href="{{ '/assets/images/cev/acceleration-pedal-matlab-analysis.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/acceleration-pedal-matlab-analysis.png' | relative_url }}" alt="MATLAB acceleration pedal analysis"></a>
          <figcaption>MATLAB pedal geometry and gas-spring force analysis</figcaption>
        </figure>

        <figure class="cev-tile">
          <a href="{{ '/assets/images/cev/pedal-back-mount-stress.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/pedal-back-mount-stress.png' | relative_url }}" alt="ANSYS equivalent stress of pedal back mount"></a>
          <figcaption>Pedal back mount / shaft holder — equivalent stress</figcaption>
        </figure>

        <figure class="cev-tile">
          <a href="{{ '/assets/images/cev/gas-spring-shaft-load.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/gas-spring-shaft-load.png' | relative_url }}" alt="Gas spring shaft applied load"></a>
          <figcaption>Gas spring shaft — applied 120.1 N load</figcaption>
        </figure>

        <figure class="cev-tile">
          <a href="{{ '/assets/images/cev/gas-spring-shaft-stress.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/gas-spring-shaft-stress.png' | relative_url }}" alt="Gas spring shaft equivalent stress"></a>
          <figcaption>Gas spring shaft — equivalent stress</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-portrait">
          <a href="{{ '/assets/images/cev/steering-linkage-stress.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-linkage-stress.png' | relative_url }}" alt="Steering linkage equivalent stress"></a>
          <figcaption>Steering linkage — equivalent stress</figcaption>
        </figure>

        <figure class="cev-tile">
          <a href="{{ '/assets/images/cev/steering-plate-chassis-integration.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-plate-chassis-integration.png' | relative_url }}" alt="Steering mounting plate integrated in chassis"></a>
          <figcaption>Steering mounting plate integrated within the chassis</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-wide">
          <a href="{{ '/assets/images/cev/steering-mounting-plate-design.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-mounting-plate-design.png' | relative_url }}" alt="Steering mounting plate design"></a>
          <figcaption>Steering mounting plate design and mounting pattern</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-wide">
          <a href="{{ '/assets/images/cev/steering-plate-loads.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-plate-loads.png' | relative_url }}" alt="Steering mounting plate ANSYS loads"></a>
          <figcaption>Steering mounting plate — applied loads and boundary conditions</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-wide">
          <a href="{{ '/assets/images/cev/steering-plate-directional-deformation.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-plate-directional-deformation.png' | relative_url }}" alt="Steering mounting plate directional deformation"></a>
          <figcaption>Steering mounting plate — directional deformation</figcaption>
        </figure>

        <figure class="cev-tile cev-tile-wide">
          <a href="{{ '/assets/images/cev/steering-plate-total-deformation.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-plate-total-deformation.png' | relative_url }}" alt="Steering mounting plate total deformation"></a>
          <figcaption>Steering mounting plate — total deformation</figcaption>
        </figure>
      </div>
    </div>
  </section>
</div>
