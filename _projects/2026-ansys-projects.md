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

  <section class="ansys-project-block ansys-next-section" id="pipe-flow">
    <div class="ansys-shell">
      <div class="ansys-project-intro">
        <div>
          <p class="ansys-label">Project 02</p>
          <h2>Laminar Pipe Flow &amp; Heat Transfer</h2>
          <p class="ansys-meta">ANSYS Fluent · Internal Flow · Convective Heat Transfer · Grid Convergence · Analytical Validation</p>
        </div>
        <div class="ansys-project-copy">
          <p>Modeled laminar internal flow and heat transfer through a 3 m long, 0.2 m diameter circular pipe with a 2 m/s inlet velocity and a constant 400 K wall temperature. The analysis tracked the development of the velocity and thermal fields from a 300 K inlet condition through the pipe exit.</p>
          <p>Compared the CFD exit velocity profile with the fully developed laminar solution, evaluated pressure and temperature contours, and calculated the axial evolution of bulk temperature, wall heat flux, local convection coefficient, and Nusselt number.</p>
          <p>Repeated the solution on four computational grids to assess mesh sensitivity. Velocity and temperature profiles were nearly coincident across the grid set, while the largest remaining sensitivity occurred in wall heat flux close to the inlet where thermal gradients were steepest.</p>
        </div>
      </div>

      <div class="ansys-stats">
        <div><span>Pipe geometry</span><strong>3.0 m × 0.2 m</strong></div>
        <div><span>Inlet velocity</span><strong>2.0 m/s</strong></div>
        <div><span>Wall temperature</span><strong>400 K</strong></div>
        <div><span>Grid study</span><strong>25×100 → 150×600</strong></div>
      </div>

      <div class="ansys-calcs">
        <div class="ansys-calcs-header">
          <div>
            <p class="ansys-label">Analytical Foundation</p>
            <h3>Closed-form calculations used to check the Fluent solution</h3>
          </div>
          <p>The simulation was benchmarked against classical laminar pipe-flow and constant-wall-temperature heat-transfer relations. These calculations established the expected flow regime, entrance lengths, velocity profile, fully developed heat-transfer coefficient, and outlet temperature before comparing against CFD.</p>
        </div>

        <div class="ansys-calc-grid">
          <div class="ansys-calc-card">
            <span class="ansys-calc-number">01</span>
            <h4>Flow Regime &amp; Entrance Length</h4>
            <div class="ansys-equation">Re<sub>D</sub> = ρVD / μ = 200</div>
            <div class="ansys-calc-values"><span>Hydrodynamic</span><strong>L<sub>h</sub> ≈ 0.05Re<sub>D</sub>D = 2.00 m</strong></div>
            <div class="ansys-calc-values"><span>Thermal, Pr = 1</span><strong>L<sub>t</sub> ≈ 2.00 m</strong></div>
            <p class="ansys-calc-note">Because the 3 m pipe exceeds both entrance lengths, the exit is expected to be hydrodynamically and thermally developed.</p>
          </div>

          <div class="ansys-calc-card">
            <span class="ansys-calc-number">02</span>
            <h4>Fully Developed Velocity Profile</h4>
            <div class="ansys-equation">u(r) = 2V[1 − (r/R)<sup>2</sup>]</div>
            <p>With V = 2 m/s and R = 0.1 m:</p>
            <div class="ansys-equation">u(r) = 4[1 − (r/0.1)<sup>2</sup>] m/s</div>
            <div class="ansys-calc-values"><span>Centerline</span><strong>u(0) = 4.0 m/s</strong></div>
            <div class="ansys-calc-values"><span>Wall</span><strong>u(0.1) = 0 m/s</strong></div>
            <p class="ansys-calc-note">The computed exit profile closely overlaps this theoretical parabola.</p>
          </div>

          <div class="ansys-calc-card">
            <span class="ansys-calc-number">03</span>
            <h4>Heat Transfer &amp; Outlet Temperature</h4>
            <div class="ansys-equation">Nu<sub>D</sub> = 3.66 &nbsp;→&nbsp; h = Nu<sub>D</sub>k/D = 36.6 W/(m²·K)</div>
            <div class="ansys-equation">T<sub>out</sub> = T<sub>s</sub> − (T<sub>s</sub> − T<sub>in</sub>)e<sup>−hA<sub>s</sub>/(ṁc<sub>p</sub>)</sup></div>
            <div class="ansys-calc-values"><span>Analytical outlet</span><strong>366.65 K</strong></div>
            <div class="ansys-calc-values"><span>50×200 CFD outlet</span><strong>374.57 K</strong></div>
            <p class="ansys-calc-note">The CFD outlet temperature is 2.16% above the analytical value because the theoretical estimate assumes a fully developed heat-transfer coefficient along the entire pipe.</p>
          </div>
        </div>
      </div>

      <div class="ansys-feature-grid">
        <figure class="ansys-figure ansys-figure-wide">
          <a href="{{ '/assets/images/ansys/pipe-mesh.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/pipe-mesh.png' | relative_url }}" alt="Computational mesh for heated pipe flow"></a>
          <figcaption>Structured mesh for the two-dimensional pipe-flow model.</figcaption>
        </figure>
        <figure class="ansys-figure ansys-figure-wide">
          <a href="{{ '/assets/images/ansys/static-temperature-contour.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/static-temperature-contour.png' | relative_url }}" alt="Static temperature contour in heated pipe"></a>
          <figcaption>Temperature field showing thermal development from the 300 K inlet toward the 400 K wall condition.</figcaption>
        </figure>
      </div>

      <div class="ansys-gallery ansys-project-gallery">
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/pipe-mesh-detail.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/pipe-mesh-detail.png' | relative_url }}" alt="Detailed heated pipe mesh"></a></div><figcaption><h3>Mesh Detail</h3><p>Close-up of the structured computational grid.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/velocity-magnitude-contour.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/velocity-magnitude-contour.png' | relative_url }}" alt="Velocity magnitude contour for heated pipe flow"></a></div><figcaption><h3>Velocity Magnitude</h3><p>Development of the laminar velocity field toward the parabolic fully developed profile.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/static-pressure-contour.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/static-pressure-contour.png' | relative_url }}" alt="Static pressure contour for heated pipe flow"></a></div><figcaption><h3>Static Pressure</h3><p>Pressure decrease along the pipe produced by viscous losses.</p></figcaption></figure>
        <figure class="ansys-card ansys-card-emphasis"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/theoretical-vs-cfd-velocity.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/theoretical-vs-cfd-velocity.png' | relative_url }}" alt="Theoretical and CFD exit velocity profiles"></a></div><figcaption><h3>Theoretical vs. CFD Velocity</h3><p>Exit velocity profile nearly coincident with the fully developed laminar analytical solution.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/average-temperature-table.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/average-temperature-table.png' | relative_url }}" alt="Average temperature values along pipe"></a></div><figcaption><h3>Bulk Temperature Data</h3><p>Mass-weighted average fluid temperature sampled along the pipe.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/average-temperature-along-pipe.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/average-temperature-along-pipe.png' | relative_url }}" alt="Average temperature along pipe"></a></div><figcaption><h3>Temperature Development</h3><p>Bulk temperature rises from 300 K at the inlet to approximately 374.57 K at x = 3 m.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/thermal-quantities-table.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/thermal-quantities-table.png' | relative_url }}" alt="Thermal quantities table"></a></div><figcaption><h3>Thermal Quantities</h3><p>Axial variation of bulk temperature, wall heat flux, and convection coefficient.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/thermal-quantities-along-pipe.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/thermal-quantities-along-pipe.png' | relative_url }}" alt="Thermal quantities along pipe"></a></div><figcaption><h3>Axial Thermal Trends</h3><p>Near-inlet heat flux decays as the thermal boundary layer develops downstream.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/nusselt-number-table.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/nusselt-number-table.png' | relative_url }}" alt="Nusselt number values along pipe"></a></div><figcaption><h3>Nusselt Number</h3><p>Local Nusselt number decreases toward the fully developed theoretical value of 3.66.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/exit-velocity-grid-convergence.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/exit-velocity-grid-convergence.png' | relative_url }}" alt="Exit velocity grid convergence"></a></div><figcaption><h3>Velocity Grid Convergence</h3><p>Exit velocity profiles from all four grids nearly overlap.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/exit-temperature-grid-convergence.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/exit-temperature-grid-convergence.png' | relative_url }}" alt="Exit temperature grid convergence"></a></div><figcaption><h3>Temperature Grid Convergence</h3><p>Exit temperature profiles remain nearly unchanged with refinement.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/wall-heat-flux-grid-convergence.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/wall-heat-flux-grid-convergence.png' | relative_url }}" alt="Wall heat flux grid convergence"></a></div><figcaption><h3>Wall Heat Flux Grid Study</h3><p>Most mesh sensitivity is concentrated near the inlet where the thermal gradient is steepest.</p></figcaption></figure>
        <figure class="ansys-card"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/outlet-temperature-validation.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/outlet-temperature-validation.png' | relative_url }}" alt="Outlet temperature validation table"></a></div><figcaption><h3>Outlet Temperature Validation</h3><p>All four grids predict outlet temperature within approximately 2.1–2.2% of the analytical estimate.</p></figcaption></figure>
        <figure class="ansys-card ansys-card-emphasis"><div class="ansys-card-media"><a href="{{ '/assets/images/ansys/nusselt-number-validation.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/ansys/nusselt-number-validation.png' | relative_url }}" alt="Nusselt number validation table"></a></div><figcaption><h3>Nusselt Validation</h3><p>Exit Nusselt numbers from every grid remain within about 1.1% of the theoretical value.</p></figcaption></figure>
      </div>

      <div class="ansys-results-box">
        <p class="ansys-label">Key Result</p>
        <h3>CFD reproduced both the laminar velocity profile and fully developed heat-transfer behavior</h3>
        <p>The computational exit velocity closely matched the theoretical parabolic profile, and the local Nusselt number approached the expected constant-wall-temperature value of 3.66 downstream. For the 50×200 grid, the exit calculation gave Nu<sub>D</sub> = 3.6595, only 0.01% from theory. Across all four grids, exit Nusselt numbers ranged from 3.6393 to 3.7003, remaining within approximately 1.1% of the analytical value.</p>
      </div>
    </div>
  </section>

  <section class="ansys-next-section">
    <div class="ansys-shell">
      <p class="ansys-label">Project 03</p>
      <h2>Compressible Airfoil CFD coming next</h2>
      <p>The next study will cover compressible flow over a NACA 0012 airfoil across multiple Mach regimes, including pressure, temperature, local Mach number, aerodynamic forces, and compressibility effects.</p>
    </div>
  </section>
</div>
