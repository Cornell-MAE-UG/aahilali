---
layout: default
title: Home
---

<div class="home-container">
  <section class="home-hero">
    <div class="home-photo-container">
      <img
        class="home-photo"
        src="{{ '/assets/images/profile-pic.jpg' | relative_url }}"
        alt="Aahil Ali">
    </div>

    <div class="home-intro">
      <h1 class="home-name">Aahil Ali</h1>

      <p class="home-bio">
        I am a Mechanical Engineering student at Cornell University with interests in mechanical design, manufacturing, testing, robotics, and engineering systems.
      </p>

      <p class="home-bio">
        My engineering experience has allowed me to work across design, analysis, prototyping, manufacturing, and technical problem solving. I am especially interested in developing real-world mechanical systems and products.
      </p>

      <p class="home-contact">
        Contact me at
        <a href="mailto:aaa387@cornell.edu">aaa387@cornell.edu</a>
      </p>

      <div class="home-links">
        <a
          class="resume-download"
          href="{{ '/assets/AahilAli-Resume.pdf' | relative_url }}"
          target="_blank"
          rel="noopener">
          <i class="bi bi-file-earmark-person"></i>
          Download Resume
        </a>

        <a
          class="linkedin-button"
          href="https://www.linkedin.com/in/aahil-ali/"
          target="_blank"
          rel="noopener"
          aria-label="Aahil Ali LinkedIn">
          <i class="bi bi-linkedin"></i>
        </a>
      </div>
    </div>
  </section>

  <section class="home-details">
    <div>
      <h2 class="home-section-heading">SKILLS</h2>

      <div class="skill-group">
        <div class="skill-title">CAD & Engineering Software:</div>
        <p class="skill-text">ADD SOFTWARE HERE</p>
      </div>

      <div class="skill-group">
        <div class="skill-title">Manufacturing:</div>
        <p class="skill-text">ADD MANUFACTURING SKILLS HERE</p>
      </div>

      <div class="skill-group">
        <div class="skill-title">Programming & Technical Tools:</div>
        <p class="skill-text">ADD PROGRAMMING AND TECHNICAL TOOLS HERE</p>
      </div>

      <div class="skill-group">
        <div class="skill-title">Engineering:</div>
        <p class="skill-text">ADD ENGINEERING SKILLS HERE</p>
      </div>
    </div>

    <div>
      <h2 class="home-section-heading">INTERESTS</h2>
      <ul class="home-list">
        <li>Mechanical Design</li>
        <li>Manufacturing Engineering</li>
        <li>Automotive Engineering</li>
        <li>Aerospace Engineering</li>
        <li>Robotics & Hardware</li>
      </ul>
    </div>
  </section>

  <section class="home-projects" id="projects">
    <h2 class="projects-title">PROJECTS</h2>

    <div class="projects-grid">
      {% assign homepage_projects = site.projects | sort: "path" | reverse %}

      {% for project in homepage_projects %}
        <a
          class="home-project-card{% if project.featured_home %} featured-project{% endif %}"
          href="{{ project.url | relative_url }}">

          {% if project.url == '/projects/ansys/' %}
            <img class="home-project-image" src="{{ '/assets/images/ansys/pressure-mach-1-3-compressible.png' | relative_url }}" alt="{{ project.title }}">
          {% elsif project.image %}
            {% assign image_name = project.image %}
            {% assign first_four = image_name | slice: 0, 4 %}
            {% assign first_character = image_name | slice: 0, 1 %}

            {% if first_four == "http" %}
              <img class="home-project-image" src="{{ image_name }}" alt="{{ project.title }}">
            {% elsif image_name contains "assets/" %}
              {% if first_character == "/" %}
                <img class="home-project-image" src="{{ image_name | relative_url }}" alt="{{ project.title }}">
              {% else %}
                {% assign full_asset_path = "/" | append: image_name %}
                <img class="home-project-image" src="{{ full_asset_path | relative_url }}" alt="{{ project.title }}">
              {% endif %}
            {% else %}
              {% assign image_path = "/assets/images/" | append: image_name %}
              <img class="home-project-image" src="{{ image_path | relative_url }}" alt="{{ project.title }}">
            {% endif %}
          {% else %}
            <div class="project-placeholder">{{ project.title }}</div>
          {% endif %}

          <div class="home-project-label">{{ project.title }}</div>
        </a>
      {% endfor %}
    </div>
  </section>
</div>
