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
        <a class="cev-btn cev-btn-secondary" href="{{ '/assets/cev-full-technical-report.pdf' | relative_url }}" target="_blank" rel="noopener">View Full Technical Report</a>
      </div>
      <div class="cev-hero-image-wrap"><img class="cev-hero-image" src="https://www.cornellelectricvehicles.org/vehicles/car-mask.webp" alt="Cornell Electric Vehicles competition car"></div>
    </div>
  </section>

  <section class="cev-collage-section" id="cev-collage">
    <div class="cev-shell cev-gallery-layout">
      <aside class="cev-gallery-copy">
        <p class="cev-eyebrow">Oct. 2023 — Present</p>
        <h2 class="cev-section-title">Project Gallery</h2>
        <p>As a member of Cornell Electric Vehicles' Steering Subteam, I work within a multidisciplinary team of 75+ students designing and building a hyper-efficient electric vehicle for the Shell Eco-marathon. My work spans mechanical design, analysis, manufacturing, and subsystem integration.</p>
        <p>I designed and manufactured a lightweight acceleration pedal and sensor mounts in Autodesk Inventor, developing the assembly around packaging, stiffness, manufacturability, and driver feedback requirements. I built a static force model in MATLAB to size the pedal geometry and gas-spring configuration for approximately 25 lb of feedback force, and integrated a linear potentiometer to record pedal-position data during testing.</p>
        <p>I verified critical pedal hardware in ANSYS, including the back mount / shaft holder and gas spring shaft, to confirm stresses remained well below the yield strength of 6061-T6 aluminum.</p>
        <p>I also led the steering-system layout for the 2026 vehicle, defining the packaging relationship between the rack and pinion, pedal box, steering linkage, autobrake, autosteer, and other hardware. I designed a threaded aluminum mounting plate that provides a shared mechanical interface while prioritizing stability and low mass, and I have machined 50+ custom components using CNC equipment, a manual mill, and a lathe to support vehicle assembly.</p>
      </aside>

      <div class="cev-collage">
        <figure class="cev-tile cev-tile-feature"><a href="{{ '/assets/images/cev/acceleration-pedal-annotated.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/acceleration-pedal-annotated.png' | relative_url }}" alt="Acceleration pedal design overview"></a><figcaption>Acceleration pedal design and packaging</figcaption></figure>
        <figure class="cev-tile cev-tile-wide"><a href="{{ '/assets/images/cev/steering-layout-subsystems.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-layout-subsystems.png' | relative_url }}" alt="Steering system physical layout and subsystem packaging"></a><figcaption>Steering-system subsystem packaging and physical layout</figcaption></figure>
        <figure class="cev-tile cev-tile-wide"><a href="{{ '/assets/images/cev/steering-layout-cad-comparison.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-layout-cad-comparison.png' | relative_url }}" alt="Steering system physical and CAD layout comparison"></a><figcaption>Physical steering layout compared with the CAD assembly</figcaption></figure>
        <figure class="cev-tile cev-tile-portrait"><a href="{{ '/assets/images/cev/steering-linkage-clearance.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-linkage-clearance.png' | relative_url }}" alt="Steering linkage clearance detail"></a><figcaption>Steering linkage packaging and clearance detail</figcaption></figure>
        <figure class="cev-tile"><a href="{{ '/assets/images/cev/acceleration-pedal-matlab-analysis.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/acceleration-pedal-matlab-analysis.png' | relative_url }}" alt="MATLAB acceleration pedal analysis"></a><figcaption>MATLAB pedal geometry and gas-spring force analysis</figcaption></figure>
        <figure class="cev-tile cev-tile-code"><a href="{{ '/assets/images/cev/acceleration-pedal-matlab-code.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/acceleration-pedal-matlab-code.png' | relative_url }}" alt="MATLAB acceleration pedal force model code"></a><figcaption>MATLAB acceleration pedal force-model code</figcaption></figure>
        <figure class="cev-tile"><a href="{{ '/assets/images/cev/pedal-back-mount-stress.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/pedal-back-mount-stress.png' | relative_url }}" alt="ANSYS equivalent stress of pedal back mount"></a><figcaption>Pedal back mount / shaft holder — equivalent stress</figcaption></figure>
        <figure class="cev-tile"><a href="{{ '/assets/images/cev/gas-spring-shaft-load.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/gas-spring-shaft-load.png' | relative_url }}" alt="Gas spring shaft applied load"></a><figcaption>Gas spring shaft — applied 120.1 N load</figcaption></figure>
        <figure class="cev-tile"><a href="{{ '/assets/images/cev/gas-spring-shaft-stress.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/gas-spring-shaft-stress.png' | relative_url }}" alt="Gas spring shaft equivalent stress"></a><figcaption>Gas spring shaft — equivalent stress</figcaption></figure>
        <figure class="cev-tile cev-tile-portrait"><a href="{{ '/assets/images/cev/steering-linkage-stress.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-linkage-stress.png' | relative_url }}" alt="Steering linkage equivalent stress"></a><figcaption>Steering linkage — equivalent stress</figcaption></figure>
        <figure class="cev-tile"><a href="{{ '/assets/images/cev/steering-plate-chassis-integration.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-plate-chassis-integration.png' | relative_url }}" alt="Steering mounting plate integrated in chassis"></a><figcaption>Steering mounting plate integrated within the chassis</figcaption></figure>
        <figure class="cev-tile cev-tile-wide"><a href="{{ '/assets/images/cev/steering-mounting-plate-design.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-mounting-plate-design.png' | relative_url }}" alt="Steering mounting plate design"></a><figcaption>Steering mounting plate design and mounting pattern</figcaption></figure>
        <figure class="cev-tile cev-tile-wide"><a href="{{ '/assets/images/cev/steering-plate-loads.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-plate-loads.png' | relative_url }}" alt="Steering mounting plate ANSYS loads"></a><figcaption>Steering mounting plate — applied loads and boundary conditions</figcaption></figure>
        <figure class="cev-tile cev-tile-wide"><a href="{{ '/assets/images/cev/steering-plate-directional-deformation.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-plate-directional-deformation.png' | relative_url }}" alt="Steering mounting plate directional deformation"></a><figcaption>Steering mounting plate — directional deformation</figcaption></figure>
        <figure class="cev-tile cev-tile-wide"><a href="{{ '/assets/images/cev/steering-plate-total-deformation.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-plate-total-deformation.png' | relative_url }}" alt="Steering mounting plate total deformation"></a><figcaption>Steering mounting plate — total deformation</figcaption></figure>
      </div>
    </div>
  </section>
</div>
