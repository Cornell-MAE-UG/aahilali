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
      <p class="ansys-subtitle">Selected CFD studies highlighting simulation setup, mesh convergence, analytical validation, and engineering interpretation.</p>
    </div>
  </section>

  <section class="ansys-project-block" id="boundary-layer">
    <div class="ansys-shell">
      <div class="ansys-project-intro">
        <div>
          <p class="ansys-label">Project 01</p>
          <h2>Laminar Boundary Layer CFD Analysis</h2>
          <p class="ansys-meta">ANSYS Fluent · Laminar Flow · Mesh Convergence · Blasius Validation</p>
        </div>
        <div class="ansys-project-copy">
          <p>Developed a two-dimensional ANSYS Fluent model of laminar flow over a flat plate using a wall-biased mesh to resolve near-wall velocity gradients. Refined the model across four grid resolutions and validated the numerical solution against the analytical Blasius boundary-layer solution at x = 1 m and x = 2 m.</p>
          <p>The CFD solution reproduced the expected downstream boundary-layer growth and velocity-profile behavior. The remaining difference from theory provided a quantitative measure of numerical/modeling error rather than relying on contour agreement alone.</p>
        </div>
      </div>

      <div class="ansys-stats">
        <div><span>Free-stream velocity</span><strong>0.5 m/s</strong></div>
        <div><span>Re at x = 2 m</span><strong>65,860</strong></div>
        <div><span>Grid study</span><strong>50×60 → 300×360</strong></div>
        <div><span>Validation</span><strong>Blasius solution</strong></div>
      </div>

      <div class="ansys-calcs">
        <div class="ansys-calcs-header">
          <div><p class="ansys-label">Analytical Validation</p><h3>Blasius theory vs. CFD</h3></div>
          <p>I first verified that the flow remained laminar, then used the Blasius flat-plate relation to establish an analytical boundary-layer thickness for comparison with the Fluent solution.</p>
        </div>
        <div class="ansys-calc-grid">
          <div class="ansys-calc-card">
            <h4>Flow Regime</h4>
            <div class="ansys-equation">Re<sub>x</sub> = ρU<sub>∞</sub>x / μ</div>
            <div class="ansys-calc-values"><span>x = 1 m</span><strong>Re<sub>x</sub> ≈ 32,930</strong></div>
            <div class="ansys-calc-values"><span>x = 2 m</span><strong>Re<sub>x</sub> ≈ 65,860</strong></div>
          </div>
          <div class="ansys-calc-card">
            <h4>Boundary-Layer Thickness</h4>
            <div class="ansys-equation">δ(x) ≈ 5x / √Re<sub>x</sub></div>
            <div class="ansys-calc-values"><span>x = 1 m</span><strong>27.55 mm theory · 20.79 mm CFD</strong></div>
            <div class="ansys-calc-values"><span>x = 2 m</span><strong>38.97 mm theory · 29.14 mm CFD</strong></div>
            <p class="ansys-calc-note">Percent differences: 24.53% and 25.21%, respectively.</p>
          </div>
        </div>
      </div>

      <div class="ansys-feature-grid">
        <figure class="ansys-figure ansys-figure-wide"><a href="{{ '/assets/images/ansys/boundary-layer-mesh.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/boundary-layer-mesh.png' | relative_url }}" alt="Biased computational mesh for flat plate boundary layer simulation"></a><figcaption>Wall-biased mesh used to resolve the near-wall velocity gradient.</figcaption></figure>
        <figure class="ansys-figure ansys-figure-wide"><a href="{{ '/assets/images/ansys/analytical-vs-cfd.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/analytical-vs-cfd.png' | relative_url }}" alt="Analytical Blasius solution compared with CFD results"></a><figcaption>Finest-grid CFD velocity profiles compared directly with the analytical Blasius solution.</figcaption></figure>
      </div>

      <div class="ansys-gallery ansys-project-gallery">
        <figure class="ansys-card ansys-card-emphasis"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/x-velocity-grid-convergence.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/x-velocity-grid-convergence.png' | relative_url }}" alt="X velocity grid convergence plot"></a></div><figcaption><h3>Mesh Convergence</h3><p>Streamwise velocity comparison across four progressively refined grids.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/velocity-profiles.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/velocity-profiles.png' | relative_url }}" alt="Boundary layer velocity profiles"></a></div><figcaption><h3>Boundary-Layer Growth</h3><p>Velocity profiles at x = 1 m and x = 2 m show downstream growth of the boundary layer.</p></figcaption></figure>
      </div>

      <div class="ansys-results-box">
        <p class="ansys-label">Key Result</p>
        <h3>Validated CFD against an analytical boundary-layer solution</h3>
        <p>The model captured the expected growth trend and profile shape while quantifying a 24.5–25.2% underprediction in boundary-layer thickness relative to Blasius theory.</p>
      </div>
    </div>
  </section>

  <section class="ansys-project-block ansys-next-section" id="pipe-flow">
    <div class="ansys-shell">
      <div class="ansys-project-intro">
        <div>
          <p class="ansys-label">Project 02</p>
          <h2>Laminar Pipe Flow &amp; Heat Transfer</h2>
          <p class="ansys-meta">ANSYS Fluent · Internal Flow · Convective Heat Transfer · Grid Convergence · Analytical Validation</p>
        </div>
        <div class="ansys-project-copy">
          <p>Modeled developing laminar flow and heat transfer through a 3 m long, 0.2 m diameter pipe with a 2 m/s inlet velocity, 300 K inlet temperature, and 400 K constant wall temperature. Benchmarked the CFD solution against closed-form laminar pipe-flow and heat-transfer relations.</p>
          <p>A four-grid refinement study showed nearly grid-independent outlet velocity and temperature profiles. The strongest validation came from the fully developed Nusselt number: the 50×200 grid predicted Nu<sub>D</sub> = 3.6595 versus the theoretical 3.6600.</p>
        </div>
      </div>

      <div class="ansys-stats">
        <div><span>Reynolds number</span><strong>200</strong></div>
        <div><span>Wall temperature</span><strong>400 K</strong></div>
        <div><span>Grid study</span><strong>25×100 → 150×600</strong></div>
        <div><span>Nusselt error</span><strong>0.01%</strong></div>
      </div>

      <div class="ansys-calcs">
        <div class="ansys-calcs-header">
          <div><p class="ansys-label">Analytical Validation</p><h3>Closed-form checks of the Fluent solution</h3></div>
          <p>The analytical model established the expected developed velocity profile and heat-transfer behavior, giving direct quantitative benchmarks for the CFD results.</p>
        </div>
        <div class="ansys-calc-grid">
          <div class="ansys-calc-card">
            <h4>Developed Flow</h4>
            <div class="ansys-equation">Re<sub>D</sub> = 200 &nbsp;·&nbsp; L<sub>h</sub> ≈ L<sub>t</sub> ≈ 2.00 m</div>
            <div class="ansys-equation">u(r) = 2V[1 − (r/R)<sup>2</sup>]</div>
            <div class="ansys-calc-values"><span>Centerline velocity</span><strong>u<sub>max</sub> = 4.0 m/s</strong></div>
          </div>
          <div class="ansys-calc-card">
            <h4>Heat Transfer</h4>
            <div class="ansys-equation">Nu<sub>D</sub> = 3.66 &nbsp;→&nbsp; h = 36.6 W/(m²·K)</div>
            <div class="ansys-calc-values"><span>Analytical outlet temperature</span><strong>366.65 K</strong></div>
            <div class="ansys-calc-values"><span>50×200 CFD outlet</span><strong>374.57 K · 2.16% difference</strong></div>
            <div class="ansys-calc-values"><span>50×200 CFD Nusselt</span><strong>3.6595 · 0.01% difference</strong></div>
          </div>
        </div>
      </div>

      <div class="ansys-feature-grid">
        <figure class="ansys-figure ansys-figure-wide"><a href="{{ '/assets/images/ansys/static-temperature-contour.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/static-temperature-contour.png' | relative_url }}" alt="Static temperature contour in heated pipe"></a><figcaption>Thermal development from the 300 K inlet toward the 400 K wall condition.</figcaption></figure>
        <figure class="ansys-figure ansys-figure-wide"><a href="{{ '/assets/images/ansys/theoretical-vs-cfd-velocity.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/theoretical-vs-cfd-velocity.png' | relative_url }}" alt="Theoretical and CFD exit velocity profiles"></a><figcaption>CFD outlet velocity nearly overlaps the theoretical fully developed parabolic profile.</figcaption></figure>
      </div>

      <div class="ansys-gallery ansys-project-gallery">
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/exit-velocity-grid-convergence.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/exit-velocity-grid-convergence.png' | relative_url }}" alt="Exit velocity grid convergence"></a></div><figcaption><h3>Grid Convergence</h3><p>Outlet velocity profiles from all four computational grids nearly overlap.</p></figcaption></figure>
        <figure class="ansys-card ansys-card-emphasis"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/nusselt-number-validation.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/nusselt-number-validation.png' | relative_url }}" alt="Nusselt number validation"></a></div><figcaption><h3>Nusselt Validation</h3><p>The 50×200 grid predicts Nu<sub>D</sub> = 3.6595, only 0.01% from the theoretical value of 3.6600.</p></figcaption></figure>
      </div>

      <div class="ansys-results-box">
        <p class="ansys-label">Key Result</p>
        <h3>CFD reproduced both the analytical velocity profile and fully developed heat-transfer behavior</h3>
        <p>The project demonstrates two independent validation paths: agreement with the theoretical parabolic velocity profile and an exit Nusselt number essentially identical to the analytical constant-wall-temperature solution.</p>
      </div>
    </div>
  </section>

  <section class="ansys-next-section">
    <div class="ansys-shell">
      <p class="ansys-label">Project 03</p>
      <h2>Compressible Airfoil CFD coming next</h2>
      <p>The next study will focus on the highest-value results from compressible flow over a NACA 0012 airfoil across subsonic and supersonic Mach regimes.</p>
    </div>
  </section>
</div>
