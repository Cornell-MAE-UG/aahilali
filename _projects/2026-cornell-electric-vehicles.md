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
      <p class="cev-page-subtitle">General overview of my work on Cornell Electric Vehicles, with a focus on the acceleration pedal assembly and steering flat plate for the 2026 vehicle.</p>
      <div class="cev-hero-actions">
        <a class="cev-btn cev-btn-primary" href="https://www.cornellelectricvehicles.org/" target="_blank" rel="noopener">Learn More About CEV</a>
        <a class="cev-btn cev-btn-secondary" href="#cev-photos">Click here to see photos :)</a>
      </div>
      <div class="cev-hero-image-wrap">
        <img class="cev-hero-image" src="https://www.cornellelectricvehicles.org/vehicles/car-mask.webp" alt="Cornell Electric Vehicles competition car">
      </div>
    </div>
  </section>

  <section class="cev-section">
    <div class="cev-shell">
      <h2 class="cev-section-title">Acceleration Pedal</h2>
      <p class="cev-section-year">2025 - 2026</p>

      <div class="cev-two-col">
        <div class="cev-image-col">
          <a href="{{ '/assets/images/cev/design-acceleration-pedal.svg' | relative_url }}" target="_blank" rel="noopener">
            <img src="{{ '/assets/images/cev/design-acceleration-pedal.svg' | relative_url }}" alt="Acceleration pedal design overview">
          </a>
          <p class="cev-caption">Acceleration pedal design overview</p>
        </div>

        <div class="cev-text-col">
          <p>I designed and manufactured a lightweight acceleration pedal and sensor mounts in Autodesk Inventor. The assembly was designed to package cleanly alongside the brake pedal and mount directly to the steering flat plate while remaining lightweight, stiff, and manufacturable.</p>
          <p>I developed a static force model in MATLAB to size the pedal geometry and gas-spring configuration around a target feedback force of approximately 25 lb. The design integrates a linear potentiometer to measure pedal displacement and record position data during vehicle testing.</p>
          <p>I also evaluated critical hardware in ANSYS, including the back mount / shaft holder and gas spring shaft, to verify that stresses remained well below the yield strength of 6061-T6 aluminum.</p>
        </div>
      </div>

      <div class="cev-analysis-summary two-up">
        <article>
          <h3>Back Mount / Shaft Holder — ANSYS</h3>
          <p><strong>Maximum equivalent stress:</strong> 10.203 MPa</p>
          <p><strong>6061-T6 yield strength:</strong> 276 MPa</p>
          <p><strong>Factor of safety:</strong> 27.1</p>
        </article>
        <article>
          <h3>Gas Spring Shaft — Hand Calculations & ANSYS</h3>
          <p><strong>Maximum stress:</strong> 37.04 MPa</p>
          <p><strong>6061-T6 yield strength:</strong> 276 MPa</p>
          <p><strong>Factor of safety:</strong> 7.42</p>
        </article>
      </div>
    </div>
  </section>

  <section class="cev-section">
    <div class="cev-shell">
      <h2 class="cev-section-title">Steering System Layout & Flat Plate</h2>
      <p class="cev-section-year">2025 - 2026</p>

      <div class="cev-two-col">
        <div class="cev-image-col">
          <a href="{{ '/assets/images/cev/steering-assembly-overview.jpg' | relative_url }}" target="_blank" rel="noopener">
            <img src="{{ '/assets/images/cev/steering-assembly-overview.jpg' | relative_url }}" alt="Steering assembly overview">
          </a>
          <p class="cev-caption">Steering assembly overview</p>
        </div>
        <div class="cev-text-col">
          <p>I led the steering system layout for the 2026 vehicle and defined the packaging relationship between the rack and pinion, driver controls, pedal box, and autonomy hardware.</p>
          <p>I designed a threaded aluminum mounting plate that creates a common mechanical interface for the rack and pinion, pedals, autobrake, autosteer, and related hardware. The design was developed for maximum stability and minimal weight while simplifying integration and maintaining component alignment.</p>
          <p>I also performed structural analysis on the plate to evaluate applied loads, deformation, elastic strain, and equivalent stress before finalizing the mounting architecture.</p>
        </div>
      </div>

      <div class="cev-wide-figure">
        <a href="{{ '/assets/images/cev/steering-mounting-plate-layout.jpg' | relative_url }}" target="_blank" rel="noopener">
          <img src="{{ '/assets/images/cev/steering-mounting-plate-layout.jpg' | relative_url }}" alt="Steering flat plate layout">
        </a>
        <p class="cev-caption">Steering flat plate layout showing the interface for pedals, rack-and-pinion hardware, and autonomy components.</p>
      </div>

      <div class="cev-analysis-summary three-up">
        <article>
          <h3>Applied Loads</h3>
          <p>Load cases represented forces introduced through the steering, pedal, and autonomy mounting interfaces.</p>
        </article>
        <article>
          <h3>Deformation</h3>
          <p>Directional and total deformation studies were used to verify that the plate remained stiff under the expected operating loads.</p>
        </article>
        <article>
          <h3>Equivalent Stress</h3>
          <p><strong>Maximum equivalent stress:</strong> approximately 12.105 MPa</p>
          <p><strong>Estimated factor of safety:</strong> approximately 23</p>
        </article>
      </div>
    </div>
  </section>

  <section class="cev-section cev-results">
    <div class="cev-shell">
      <h2 class="cev-section-title">Competition Results</h2>
      <div class="cev-stat-grid">
        <div class="cev-stat"><strong>75+</strong><span>students collaborating across the team</span></div>
        <div class="cev-stat"><strong>5th</strong><span>on-track finish at Shell Eco-marathon Americas</span></div>
        <div class="cev-stat"><strong>2</strong><span>off-track awards</span></div>
        <div class="cev-stat"><strong>$4,500</strong><span>competition prize funding</span></div>
      </div>
    </div>
  </section>

  <section class="cev-section cev-gallery" id="cev-photos">
    <div class="cev-shell">
      <h2 class="cev-section-title">Photos / Fun</h2>
      <p class="cev-section-year">Click any image to view it larger</p>
      <div class="cev-photo-grid">
        <a href="https://www.cornellelectricvehicles.org/vehicles/car-mask.webp" target="_blank" rel="noopener"><img src="https://www.cornellelectricvehicles.org/vehicles/car-mask.webp" alt="Cornell Electric Vehicles competition car"></a>
        <a href="{{ '/assets/images/cev/design-acceleration-pedal.svg' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/design-acceleration-pedal.svg' | relative_url }}" alt="Acceleration pedal design overview"></a>
        <a href="{{ '/assets/images/cev/steering-assembly-overview.jpg' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-assembly-overview.jpg' | relative_url }}" alt="Steering assembly overview"></a>
        <a href="{{ '/assets/images/cev/steering-mounting-plate-layout.jpg' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/cev/steering-mounting-plate-layout.jpg' | relative_url }}" alt="Steering flat plate layout"></a>
      </div>
    </div>
  </section>
</div>
