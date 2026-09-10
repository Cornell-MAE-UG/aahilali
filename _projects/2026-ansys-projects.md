---
layout: ansys
title: "ANSYS / CFD Projects"
excerpt: "Computational fluid dynamics projects using ANSYS Fluent, mesh refinement, analytical validation, and engineering interpretation."
permalink: /projects/ansys/
---

<div class="ansys-page">
  <section class="ansys-hero">
    <div class="ansys-shell">
      <p class="ansys-kicker">ANSYS Fluent · Computational Fluid Dynamics</p>
      <h1 class="ansys-title">ANSYS / CFD Projects</h1>
    </div>
  </section>

  <section class="ansys-project-block" id="airfoil">
    <div class="ansys-shell">
      <div class="ansys-project-intro">
        <div>
          <p class="ansys-label">Project 01</p>
          <h2>Compressible Flow over a NACA 0012 Airfoil</h2>
          <p class="ansys-meta">ANSYS Fluent · Compressible Flow · Shock Formation · Aerodynamic Loads · Model Comparison</p>
        </div>
        <div class="ansys-project-copy">
          <p>Simulated flow over a NACA 0012 airfoil at Mach 0.4, 0.7, 1.1, and 1.3 to examine how the flow field changes from subsonic to supersonic conditions. The analysis compared local Mach number, pressure, temperature, and aerodynamic loading across the four operating points.</p>
          <p>At the supersonic conditions, the solution developed strong compression and expansion features around the airfoil. A second Mach 1.3 case was then solved with an incompressible model to show how strongly the predicted flow field and aerodynamic loads depend on including compressibility.</p>
        </div>
      </div>

      <div class="ansys-stats">
        <div><span>Airfoil</span><strong>NACA 0012</strong></div>
        <div><span>Mach range</span><strong>0.4 → 1.3</strong></div>
        <div><span>Drag coefficient</span><strong>0.011 → 0.141</strong></div>
        <div><span>Mach 1.3 drag</span><strong>16,931.7 N</strong></div>
      </div>

      <div class="ansys-calcs ansys-insight-panel">
        <div class="ansys-calcs-header">
          <div><p class="ansys-label">Engineering Interpretation</p><h3>What changed as the flow became supersonic</h3></div>
          <p>The value of this study is not just the contour output. The Mach sweep shows the onset of compressibility effects, while the Mach 1.3 model comparison quantifies how much the physics assumption changes the predicted aerodynamic response.</p>
        </div>
        <div class="ansys-calc-grid">
          <div class="ansys-calc-card">
            <h4>Mach Regime</h4>
            <p>Mach 0.4 and 0.7 remain subsonic, while Mach 1.1 and 1.3 show the pronounced wave structure associated with supersonic flow.</p>
          </div>
          <div class="ansys-calc-card">
            <h4>Aerodynamic Consequence</h4>
            <div class="ansys-calc-values"><span>C<sub>D</sub> at Mach 0.7</span><strong>0.01103</strong></div>
            <div class="ansys-calc-values"><span>C<sub>D</sub> at Mach 1.1</span><strong>0.1459</strong></div>
            <p class="ansys-calc-note">The sharp increase in drag coefficient reflects the added wave drag once the flow becomes supersonic.</p>
          </div>
          <div class="ansys-calc-card">
            <h4>Compressibility Matters</h4>
            <div class="ansys-calc-values"><span>Compressible C<sub>D</sub></span><strong>0.14135</strong></div>
            <div class="ansys-calc-values"><span>Incompressible C<sub>D</sub></span><strong>0.05542</strong></div>
            <div class="ansys-calc-values"><span>Drag force ratio</span><strong>2.45×</strong></div>
          </div>
        </div>
      </div>

      <div class="ansys-feature-grid">
        <figure class="ansys-figure ansys-figure-wide"><a href="{{ '/assets/images/ansys/mach-number-0-7.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/mach-number-0-7.png' | relative_url }}" alt="Local Mach number contour at Mach 0.7"></a><figcaption><strong>Subsonic Baseline.</strong> Local Mach number at Mach 0.7 shows smooth acceleration around the airfoil without a shock structure.</figcaption></figure>
        <figure class="ansys-figure ansys-figure-wide"><a href="{{ '/assets/images/ansys/mach-number-1-3.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/mach-number-1-3.png' | relative_url }}" alt="Local Mach number contour at Mach 1.3"></a><figcaption><strong>Supersonic Flow.</strong> The Mach 1.3 solution shows the strong wave structure and large local changes in Mach number around the airfoil.</figcaption></figure>
      </div>

      <div class="ansys-gallery ansys-project-gallery ansys-gallery-two">
        <figure class="ansys-card ansys-card-emphasis"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/pressure-mach-1-3-compressible.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/pressure-mach-1-3-compressible.png' | relative_url }}" alt="Compressible static pressure contour at Mach 1.3"></a></div><figcaption><h3>Compressible Pressure Field</h3><p>The pressure solution captures the strong compression and expansion regions around the airfoil at Mach 1.3.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/pressure-mach-1-3-incompressible.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/pressure-mach-1-3-incompressible.png' | relative_url }}" alt="Incompressible static pressure contour at Mach 1.3"></a></div><figcaption><h3>Incompressible Comparison</h3><p>The incompressible model does not reproduce the same pressure structure and substantially underpredicts the aerodynamic drag.</p></figcaption></figure>
      </div>

      <div class="ansys-results-box">
        <h3>Compressibility changed the predicted aerodynamic loading dramatically</h3>
        <p>At Mach 1.3, the compressible model predicted C<sub>D</sub> = 0.14135 and 16,931.7 N of drag, compared with C<sub>D</sub> = 0.05542 and 6,910.8 N from the incompressible model. The compressible prediction was about 2.45 times larger, showing why the correct flow model is essential in the supersonic regime.</p>
      </div>
    </div>
  </section>

  <section class="ansys-project-block" id="pipe-flow">
    <div class="ansys-shell">
      <div class="ansys-project-intro">
        <div>
          <p class="ansys-label">Project 02</p>
          <h2>Laminar Pipe Flow &amp; Heat Transfer</h2>
          <p class="ansys-meta">ANSYS Fluent · Internal Flow · Convective Heat Transfer · Grid Convergence · Analytical Validation</p>
        </div>
        <div class="ansys-project-copy">
          <p>Modeled laminar internal flow and thermal development through a 3 m long, 0.2 m diameter pipe with a 2 m/s inlet velocity, 300 K inlet temperature, and 400 K constant wall temperature. The model captured both hydrodynamic development and the evolving thermal boundary layer.</p>
          <p>Used classical pipe flow and heat transfer relations as benchmarks, then repeated the Fluent solution on four meshes to check grid sensitivity. Validation was performed independently through the outlet velocity profile, outlet temperature, and fully developed Nusselt number.</p>
        </div>
      </div>

      <div class="ansys-stats">
        <div><span>Reynolds number</span><strong>200</strong></div>
        <div><span>Wall temperature</span><strong>400 K</strong></div>
        <div><span>Grid study</span><strong>25×100 → 150×600</strong></div>
        <div><span>Best Nu agreement</span><strong>0.01%</strong></div>
      </div>

      <div class="ansys-calcs">
        <div class="ansys-calcs-header">
          <div><p class="ansys-label">Analytical Foundation</p><h3>Closed form checks of flow and heat transfer</h3></div>
          <p>The calculations establish when the flow should become developed, define the expected parabolic velocity profile, and provide theoretical heat transfer quantities for comparison with CFD.</p>
        </div>
        <div class="ansys-calc-grid ansys-calc-grid-two">
          <div class="ansys-calc-card">
            <h4>Flow Development</h4>
            <div class="ansys-equation">Re<sub>D</sub> = ρVD / μ = 200</div>
            <div class="ansys-calc-values"><span>Hydrodynamic entrance length</span><strong>L<sub>h</sub> ≈ 2.00 m</strong></div>
            <div class="ansys-calc-values"><span>Thermal entrance length</span><strong>L<sub>t</sub> ≈ 2.00 m</strong></div>
            <div class="ansys-equation">u(r) = 2V[1 − (r/R)<sup>2</sup>]</div>
            <div class="ansys-calc-values"><span>Expected centerline velocity</span><strong>4.0 m/s</strong></div>
          </div>
          <div class="ansys-calc-card">
            <h4>Heat Transfer Validation</h4>
            <div class="ansys-equation">Nu<sub>D</sub> = 3.66 &nbsp;→&nbsp; h = 36.6 W/(m²·K)</div>
            <div class="ansys-calc-values"><span>Analytical outlet temperature</span><strong>366.65 K</strong></div>
            <div class="ansys-calc-values"><span>50×200 CFD outlet</span><strong>374.57 K · 2.16%</strong></div>
            <div class="ansys-calc-values"><span>50×200 CFD Nusselt</span><strong>3.6595 · 0.01%</strong></div>
          </div>
        </div>
      </div>

      <div class="ansys-feature-grid">
        <figure class="ansys-figure ansys-figure-wide"><a href="{{ '/assets/images/ansys/pipe-mesh.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/pipe-mesh.png' | relative_url }}" alt="Structured computational mesh for heated pipe"></a><figcaption><strong>Model and Mesh.</strong> Structured two dimensional grid used for the internal flow simulation.</figcaption></figure>
        <figure class="ansys-figure ansys-figure-wide"><a href="{{ '/assets/images/ansys/static-temperature-contour.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/static-temperature-contour.png' | relative_url }}" alt="Static temperature contour in heated pipe"></a><figcaption><strong>Thermal Development.</strong> Fluid heats from 300 K as the thermal boundary layer develops against the 400 K wall.</figcaption></figure>
      </div>

      <div class="ansys-gallery ansys-project-gallery">
        <figure class="ansys-card ansys-card-emphasis"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/theoretical-vs-cfd-velocity.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/theoretical-vs-cfd-velocity.png' | relative_url }}" alt="Theoretical and CFD exit velocity profiles"></a></div><figcaption><h3>Velocity Validation</h3><p>Computed outlet velocity nearly overlaps the fully developed analytical parabolic profile.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/average-temperature-along-pipe.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/average-temperature-along-pipe.png' | relative_url }}" alt="Average temperature along heated pipe"></a></div><figcaption><h3>Bulk Temperature Development</h3><p>Mass weighted average temperature rises from 300 K at the inlet to approximately 374.57 K at the outlet.</p></figcaption></figure>
        <figure class="ansys-card ansys-card-emphasis"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/nusselt-number-validation.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/nusselt-number-validation.png' | relative_url }}" alt="Nusselt number validation"></a></div><figcaption><h3>Nusselt Validation</h3><p>The 50×200 grid predicts Nu<sub>D</sub> = 3.6595 versus 3.6600 theoretical, a 0.01% difference.</p></figcaption></figure>
      </div>

      <div class="ansys-results-box">
        <h3>Verified the CFD solution through independent fluid and thermal benchmarks</h3>
        <p>The model matched the expected parabolic outlet velocity profile, captured the downstream temperature rise, and converged to the theoretical fully developed Nusselt number. Across all four grids, exit Nusselt values remained within approximately 1.1% of theory.</p>
      </div>
    </div>
  </section>

  <section class="ansys-project-block" id="boundary-layer">
    <div class="ansys-shell">
      <div class="ansys-project-intro">
        <div>
          <p class="ansys-label">Project 03</p>
          <h2>Laminar Boundary Layer CFD Analysis</h2>
          <p class="ansys-meta">ANSYS Fluent · Laminar Flow · Mesh Convergence · Blasius Validation</p>
        </div>
        <div class="ansys-project-copy">
          <p>Developed a two dimensional ANSYS Fluent model to study laminar boundary layer growth over a flat plate. A 2 m × 1 m domain and wall biased mesh were used to resolve the steep near wall velocity gradient while maintaining a practical element count away from the plate.</p>
          <p>Verified the expected laminar regime analytically, solved the model across four progressively refined grids, and validated the numerical results against the Blasius flat plate solution at x = 1 m and x = 2 m.</p>
        </div>
      </div>

      <div class="ansys-stats">
        <div><span>Domain</span><strong>2 m × 1 m</strong></div>
        <div><span>Free stream velocity</span><strong>0.5 m/s</strong></div>
        <div><span>Grid study</span><strong>50×60 → 300×360</strong></div>
        <div><span>Validation</span><strong>Blasius solution</strong></div>
      </div>

      <div class="ansys-calcs">
        <div class="ansys-calcs-header">
          <div><p class="ansys-label">Analytical Foundation</p><h3>Physics used to check the CFD model</h3></div>
          <p>The hand calculations establish the correct flow regime and provide a quantitative reference for boundary layer thickness at the same locations extracted from Fluent.</p>
        </div>
        <div class="ansys-calc-grid ansys-calc-grid-two">
          <div class="ansys-calc-card">
            <h4>Flow Regime</h4>
            <div class="ansys-equation">Re<sub>x</sub> = ρU<sub>∞</sub>x / μ</div>
            <div class="ansys-calc-values"><span>x = 1 m</span><strong>Re<sub>x</sub> ≈ 32,930</strong></div>
            <div class="ansys-calc-values"><span>x = 2 m</span><strong>Re<sub>x</sub> ≈ 65,860</strong></div>
            <p class="ansys-calc-note">Both values remain below the 5×10<sup>5</sup> transition criterion used in the study, supporting the laminar model.</p>
          </div>
          <div class="ansys-calc-card">
            <h4>Blasius Thickness and CFD Comparison</h4>
            <div class="ansys-equation">δ(x) ≈ 5x / √Re<sub>x</sub></div>
            <div class="ansys-calc-values"><span>x = 1 m</span><strong>27.55 mm theory · 20.79 mm CFD</strong></div>
            <div class="ansys-calc-values"><span>x = 2 m</span><strong>38.97 mm theory · 29.14 mm CFD</strong></div>
            <p class="ansys-calc-note">Percent differences were 24.53% and 25.21%, while both solutions showed the same downstream growth trend.</p>
          </div>
        </div>
      </div>

      <div class="ansys-feature-grid">
        <figure class="ansys-figure ansys-figure-wide"><a href="{{ '/assets/images/ansys/boundary-layer-mesh.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/boundary-layer-mesh.png' | relative_url }}" alt="Biased computational mesh for flat plate boundary layer simulation"></a><figcaption><strong>Mesh Strategy.</strong> Wall biased cells concentrate resolution where the boundary layer velocity gradient is largest.</figcaption></figure>
        <figure class="ansys-figure ansys-figure-wide"><a href="{{ '/assets/images/ansys/velocity-magnitude-contour.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/velocity-magnitude-contour.png' | relative_url }}" alt="Velocity magnitude contour for flat plate boundary layer"></a><figcaption><strong>Flow Field.</strong> Velocity magnitude contour showing the developing low speed boundary layer and its downstream growth.</figcaption></figure>
      </div>

      <div class="ansys-gallery ansys-project-gallery ansys-gallery-two">
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/x-velocity-grid-convergence.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/x-velocity-grid-convergence.png' | relative_url }}" alt="X velocity grid convergence plot"></a></div><figcaption><h3>Mesh Convergence</h3><p>Streamwise velocity across four grid resolutions demonstrates decreasing sensitivity to refinement.</p></figcaption></figure>
        <figure class="ansys-card ansys-card-emphasis"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/analytical-vs-cfd.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/analytical-vs-cfd.png' | relative_url }}" alt="Analytical Blasius solution compared with CFD results"></a></div><figcaption><h3>Analytical Validation</h3><p>Finest grid Fluent profiles compared directly with the analytical Blasius solution.</p></figcaption></figure>
      </div>

      <div class="ansys-results-box">
        <h3>Captured the correct boundary layer physics and quantified the model error</h3>
        <p>The CFD solution reproduced the expected profile shape and downstream growth. Using the 99% free stream velocity criterion, it predicted thicknesses of 20.79 mm and 29.14 mm at x = 1 m and x = 2 m, compared with Blasius values of 27.55 mm and 38.97 mm.</p>
      </div>
    </div>
  </section>
</div>