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
      <p class="ansys-subtitle">A collection of computational fluid dynamics projects focused on model setup, mesh quality, flow visualization, grid convergence, analytical validation, and interpretation of simulation results.</p>
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
          <p>Developed a two-dimensional ANSYS Fluent model to investigate laminar boundary-layer development over a flat plate. The model used a 2 m × 1 m computational domain with a wall-biased mesh to resolve the near-wall velocity gradient and capture boundary-layer growth downstream.</p>
          <p>Evaluated velocity magnitude, x- and y-velocity, static pressure, vectors, and streamlines to interpret the flow field. The simulation was repeated using four progressively refined grids to assess mesh sensitivity and verify that the predicted velocity profiles were approaching grid-independent behavior.</p>
          <p>Validated the numerical solution against the analytical Blasius boundary-layer solution at x = 1 m and x = 2 m. The CFD and analytical profiles showed the same physical trend and similar profile shapes, while the simulated boundary-layer thickness remained lower than the analytical prediction.</p>
        </div>
      </div>

      <div class="ansys-stats">
        <div><span>Domain</span><strong>2 m × 1 m</strong></div>
        <div><span>Free-stream velocity</span><strong>0.5 m/s</strong></div>
        <div><span>Grid study</span><strong>50×60 → 300×360</strong></div>
        <div><span>Validation</span><strong>Blasius solution</strong></div>
      </div>

      <div class="ansys-calcs">
        <div class="ansys-calcs-header">
          <div>
            <p class="ansys-label">Analytical Foundation</p>
            <h3>Hand calculations used to validate the CFD model</h3>
          </div>
          <p>Before comparing the Fluent solution to theory, I used the freestream conditions and flat-plate relations to verify the expected flow regime and estimate the boundary-layer thickness at the same downstream locations used for CFD validation.</p>
        </div>

        <div class="ansys-calc-grid">
          <div class="ansys-calc-card">
            <span class="ansys-calc-number">01</span>
            <h4>Reynolds Number</h4>
            <div class="ansys-equation">Re<sub>x</sub> = ρU<sub>∞</sub>x / μ</div>
            <p>Using U<sub>∞</sub> = 0.5 m/s, ρ = 1.225 kg/m³, and μ = 18.6×10<sup>−6</sup> kg/(m·s):</p>
            <div class="ansys-calc-values"><span>x = 1 m</span><strong>Re<sub>x</sub> ≈ 32,930</strong></div>
            <div class="ansys-calc-values"><span>x = 2 m</span><strong>Re<sub>x</sub> ≈ 65,860</strong></div>
            <p class="ansys-calc-note">Both values remain well below the 5×10<sup>5</sup> transition criterion used in the study, supporting a laminar-flow model.</p>
          </div>

          <div class="ansys-calc-card">
            <span class="ansys-calc-number">02</span>
            <h4>Blasius Boundary-Layer Thickness</h4>
            <div class="ansys-equation">δ(x) ≈ 5x / √Re<sub>x</sub></div>
            <p>The analytical flat-plate relation provides the reference thickness used to evaluate the numerical solution.</p>
            <div class="ansys-calc-values"><span>x = 1 m</span><strong>δ ≈ 0.02755 m</strong></div>
            <div class="ansys-calc-values"><span>x = 2 m</span><strong>δ ≈ 0.03897 m</strong></div>
            <p class="ansys-calc-note">Equivalent analytical thicknesses: 27.55 mm and 38.97 mm.</p>
          </div>

          <div class="ansys-calc-card">
            <span class="ansys-calc-number">03</span>
            <h4>CFD vs. Analytical Thickness</h4>
            <div class="ansys-equation">% difference = |δ<sub>CFD</sub> − δ<sub>theory</sub>| / δ<sub>theory</sub> × 100</div>
            <div class="ansys-calc-values"><span>x = 1 m</span><strong>20.79 mm CFD · 24.53%</strong></div>
            <div class="ansys-calc-values"><span>x = 2 m</span><strong>29.14 mm CFD · 25.21%</strong></div>
            <p class="ansys-calc-note">The numerical solution underpredicted thickness but reproduced the expected downstream growth and overall profile behavior.</p>
          </div>
        </div>
      </div>

      <div class="ansys-feature-grid">
        <figure class="ansys-figure ansys-figure-wide">
          <a href="{{ '/assets/images/ansys/boundary-layer-mesh.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/boundary-layer-mesh.png' | relative_url }}" alt="Biased computational mesh for flat plate boundary layer simulation"></a>
          <figcaption>Wall-biased computational mesh used to resolve near-wall velocity gradients.</figcaption>
        </figure>

        <figure class="ansys-figure ansys-figure-wide">
          <a href="{{ '/assets/images/ansys/velocity-magnitude-contour.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/velocity-magnitude-contour.png' | relative_url }}" alt="Velocity magnitude contour for flat plate boundary layer"></a>
          <figcaption>Velocity magnitude contour showing boundary-layer development along the plate.</figcaption>
        </figure>
      </div>

      <div class="ansys-gallery ansys-project-gallery">
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/x-velocity-contour.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/x-velocity-contour.png' | relative_url }}" alt="X velocity contour"></a></div><figcaption><h3>X Velocity</h3><p>Streamwise velocity field through the developing boundary layer.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/y-velocity-contour.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/y-velocity-contour.png' | relative_url }}" alt="Y velocity contour"></a></div><figcaption><h3>Y Velocity</h3><p>Normal velocity component associated with boundary-layer growth.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/static-pressure-contour.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/static-pressure-contour.png' | relative_url }}" alt="Static pressure contour"></a></div><figcaption><h3>Static Pressure</h3><p>Pressure field across the computational domain.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/velocity-vectors.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/velocity-vectors.png' | relative_url }}" alt="Velocity vector plot"></a></div><figcaption><h3>Velocity Vectors</h3><p>Vector visualization of local flow direction and magnitude.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/velocity-streamlines.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/velocity-streamlines.png' | relative_url }}" alt="Velocity streamlines"></a></div><figcaption><h3>Streamlines</h3><p>Flow trajectories through the flat-plate domain.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/velocity-profiles.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/velocity-profiles.png' | relative_url }}" alt="Velocity profiles at x equals 1 and 2 meters"></a></div><figcaption><h3>Velocity Profiles</h3><p>Velocity magnitude versus distance from the plate at two downstream locations.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/x-velocity-grid-convergence.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/x-velocity-grid-convergence.png' | relative_url }}" alt="X velocity grid convergence plot"></a></div><figcaption><h3>X Velocity Grid Study</h3><p>Comparison of streamwise velocity across four grid resolutions.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/y-velocity-grid-convergence.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/y-velocity-grid-convergence.png' | relative_url }}" alt="Y velocity grid convergence plot"></a></div><figcaption><h3>Y Velocity Grid Study</h3><p>Mesh-refinement comparison of the normal velocity component.</p></figcaption></figure>
        <figure class="ansys-card ansys-card-emphasis"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/analytical-vs-cfd.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/analytical-vs-cfd.png' | relative_url }}" alt="Analytical Blasius solution compared with CFD results"></a></div><figcaption><h3>Analytical vs. CFD Validation</h3><p>Comparison of the finest-grid Fluent results with the analytical Blasius velocity profiles.</p></figcaption></figure>
      </div>

      <div class="ansys-results-box">
        <p class="ansys-label">Key Result</p>
        <h3>Simulation captured the correct boundary-layer growth trend</h3>
        <p>The computational and analytical profiles showed similar shapes and both predicted an increase in boundary-layer thickness downstream. Using the 99% free-stream velocity criterion, the CFD solution predicted boundary-layer thicknesses of 20.79 mm at x = 1 m and 29.14 mm at x = 2 m, compared with analytical values of 27.55 mm and 38.97 mm.</p>
      </div>
    </div>
  </section>

  <section class="ansys-next-section">
    <div class="ansys-shell">
      <p class="ansys-label">Additional CFD Projects</p>
      <h2>More analyses coming next</h2>
      <p>Laminar pipe flow with heat transfer and compressible flow over a NACA 0012 airfoil will be added here as additional CFD studies.</p>
    </div>
  </section>
</div>
