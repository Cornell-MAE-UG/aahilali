---
layout: mechatronics
title: "Mechatronics"
excerpt: "Autonomous cube-collecting robot integrating mechanical design, sensing, control, wiring, and testing."
permalink: /projects/mechatronics/
image: /assets/images/mechatronics-robot.jpg
---

<div class="mech-page">
  <section class="mech-hero">
    <div class="mech-shell">
      <p class="mech-kicker">MAE 3780 · Mechatronics</p>
      <h1 class="mech-title">Mechatronics</h1>
      <p class="mech-subtitle">A team-based autonomous robotics project combining mechanical design, sensing, control logic, wiring, testing, and iterative prototyping for a one-minute cube-collecting competition.</p>

      <div class="mech-actions">
        <a class="mech-btn mech-btn-primary" href="{{ '/assets/MAE 3780 Final Report.pdf' | relative_url }}" target="_blank" rel="noopener">View Technical Report</a>
      </div>
    </div>
  </section>

  <section>
    <div class="mech-shell mech-main-grid">
      <div class="mech-copy">
        <p class="mech-section-label">Project Overview</p>
        <h2 class="mech-heading">Autonomous Cube-Collecting Robot</h2>
        <p>For the MAE 3780 final project, my team designed and built an autonomous robot for a one-minute cube-collecting competition. The objective was to gather as many cubes as possible within the robot’s perimeter before time expired.</p>
        <p>We intentionally pursued a simple, lightweight, and reliable collection strategy. Cardboard walls enclosed the rear and sides of the chassis, while a V-shaped front guide funneled cubes toward side openings so they could enter and remain inside the robot’s perimeter without requiring a complicated active intake mechanism.</p>
        <p>The robot used a color sensor to identify the black boundary of the playing field. When the boundary was detected, the robot stopped, reversed, turned away from the edge, and resumed driving. Because we did not use dedicated cube-detection sensors, our control strategy emphasized reliable field coverage and boundary avoidance.</p>

        <p class="mech-section-label">My Contribution</p>
        <p>I contributed to the mechanical design, chassis construction, wiring, testing, troubleshooting, and code verification. I helped develop the final structure, mount components, validate wiring, and iterate on the robot’s behavior through repeated testing.</p>
        <p>I also helped evaluate different cardboard geometries, wall heights, and attachment methods. A major design challenge was keeping cubes securely inside the robot while it accelerated, turned, and changed direction. The project reinforced the importance of designing around reliability rather than adding complexity for its own sake.</p>

        <p class="mech-section-label">Design Iteration</p>
        <p>Early concepts included more complicated intake approaches such as sweeping and rotating mechanisms. After testing and discussion, our team simplified the design and focused on passive geometry that could guide cubes into the robot with fewer moving parts and fewer potential failure points.</p>
        <p>We also learned where the prototype could be improved. More rigid structural parts, stronger component mounts, and a better-secured color sensor would have increased repeatability and competition reliability.</p>
      </div>

      <figure class="mech-hero-card">
        <a href="{{ '/assets/images/mechatronics-robot.jpg' | relative_url }}" target="_blank" rel="noopener">
          <img src="{{ '/assets/images/mechatronics-robot.jpg' | relative_url }}" alt="MAE 3780 autonomous mechatronics robot">
        </a>
        <figcaption>Autonomous cube-collecting robot developed for the MAE 3780 final competition.</figcaption>
      </figure>
    </div>
  </section>

  <section class="mech-gallery-section">
    <div class="mech-shell">
      <div class="mech-gallery-header">
        <div>
          <p class="mech-section-label">Project Gallery</p>
          <h2 class="mech-heading">Design, Build, Code, Test</h2>
        </div>
        <p>This gallery is set up for the final robot, mechanical details, electronics and wiring, sensor setup, testing, code screenshots, and competition photos.</p>
      </div>

      <div class="mech-gallery">
        <figure class="mech-tile">
          <a href="{{ '/assets/images/mechatronics-robot.jpg' | relative_url }}" target="_blank" rel="noopener">
            <img src="{{ '/assets/images/mechatronics-robot.jpg' | relative_url }}" alt="Completed autonomous mechatronics robot">
          </a>
          <figcaption>Completed autonomous robot</figcaption>
        </figure>
      </div>

      <div class="mech-note">The page layout is ready for additional project images and code. Add the final gallery images under <strong>assets/images/mechatronics/</strong> and the source code under <strong>assets/code/mechatronics/</strong>; I can wire them into this layout as you upload them.</div>
    </div>
  </section>
</div>
