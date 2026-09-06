---
layout: default
title: Home
---


<div class="home-container">


  <!-- =====================================================
       TOP / INTRODUCTION
       ===================================================== -->

  <section class="home-hero">


    <!-- PROFILE PHOTO -->

    <div class="home-photo-container">

      <img
        class="home-photo"
        src="{{ '/assets/images/profile-pic.jpg' | relative_url }}"
        alt="Aahil Ali">

    </div>



    <!-- INTRODUCTION -->

    <div class="home-intro">


      <h1 class="home-name">
        Aahil Ali
      </h1>



      <!-- ================================================
           EDIT THIS: ABOUT PARAGRAPH 1
           ================================================ -->

      <p class="home-bio">

        I am a Mechanical Engineering student at Cornell University
        with interests in mechanical design, manufacturing, testing,
        robotics, and engineering systems.

      </p>



      <!-- ================================================
           EDIT THIS: ABOUT PARAGRAPH 2
           ================================================ -->

      <p class="home-bio">

        My engineering experience has allowed me to work across
        design, analysis, prototyping, manufacturing, and technical
        problem solving. I am especially interested in developing
        real-world mechanical systems and products.

      </p>



      <!-- ================================================
           EDIT THIS: EMAIL
           ================================================ -->

      <p class="home-contact">

        Contact me at

        <a href="mailto:YOUR_EMAIL@cornell.edu">
          YOUR_EMAIL@cornell.edu
        </a>

      </p>



      <div class="home-links">


        <!-- YOUR ACTUAL RESUME FILE -->

        <a
          class="resume-download"
          href="{{ '/assets/AahilAli-Resume.pdf' | relative_url }}"
          target="_blank"
          rel="noopener">

          <i class="bi bi-file-earmark-person"></i>

          Download Resume

        </a>



        <!-- ================================================
             EDIT THIS: LINKEDIN
             ================================================ -->

        <a
          class="linkedin-button"
          href="https://www.linkedin.com/in/YOUR-LINKEDIN/"
          target="_blank"
          rel="noopener"
          aria-label="LinkedIn">

          <i class="bi bi-linkedin"></i>

        </a>


      </div>


    </div>


  </section>



  <!-- =====================================================
       SKILLS / INTERESTS / HOBBIES
       ===================================================== -->

  <section class="home-details">


    <!-- LEFT COLUMN -->

    <div>


      <h2 class="home-section-heading">
        SKILLS
      </h2>



      <!-- EDIT THIS -->

      <div class="skill-group">

        <div class="skill-title">
          CAD & Engineering Software:
        </div>

        <p class="skill-text">
          YOUR SOFTWARE HERE
        </p>

      </div>



      <!-- EDIT THIS -->

      <div class="skill-group">

        <div class="skill-title">
          Manufacturing:
        </div>

        <p class="skill-text">
          YOUR MANUFACTURING SKILLS HERE
        </p>

      </div>



      <!-- EDIT THIS -->

      <div class="skill-group">

        <div class="skill-title">
          Programming & Technical Tools:
        </div>

        <p class="skill-text">
          YOUR PROGRAMMING / TECHNICAL TOOLS HERE
        </p>

      </div>



      <!-- EDIT / ADD MORE IF NEEDED -->

      <div class="skill-group">

        <div class="skill-title">
          Engineering:
        </div>

        <p class="skill-text">
          YOUR ENGINEERING SKILLS HERE
        </p>

      </div>


    </div>



    <!-- RIGHT COLUMN -->

    <div>


      <!-- INTERESTS -->

      <h2 class="home-section-heading">
        INTERESTS
      </h2>


      <ul class="home-list">

        <li>YOUR INTEREST</li>

        <li>YOUR INTEREST</li>

        <li>YOUR INTEREST</li>

        <li>YOUR INTEREST</li>

      </ul>



      <!-- HOBBIES -->

      <div class="hobbies">


        <h2 class="home-section-heading">
          HOBBIES
        </h2>


        <ul class="home-list">

          <li>YOUR HOBBY</li>

          <li>YOUR HOBBY</li>

          <li>YOUR HOBBY</li>

        </ul>


      </div>


    </div>


  </section>



  <!-- =====================================================
       PROJECTS
       ===================================================== -->

  <section
    class="home-projects"
    id="projects">


    <h2 class="projects-title">
      PROJECTS
    </h2>



    <div class="projects-grid">


      {% assign homepage_projects = site.projects | sort: "path" | reverse %}


      {% for project in homepage_projects %}


        <a
          class="home-project-card"
          href="{{ project.url | relative_url }}">


          <!-- PROJECT IMAGE -->

          {% if project.image %}


            {% assign image_name = project.image %}

            {% assign first_four = image_name | slice: 0, 4 %}

            {% assign first_character = image_name | slice: 0, 1 %}



            <!-- EXTERNAL IMAGE -->

            {% if first_four == "http" %}

              <img
                class="home-project-image"
                src="{{ image_name }}"
                alt="{{ project.title }}">



            <!-- IMAGE PATH ALREADY CONTAINS ASSETS -->

            {% elsif image_name contains "assets/" %}


              {% if first_character == "/" %}

                <img
                  class="home-project-image"
                  src="{{ image_name | relative_url }}"
                  alt="{{ project.title }}">

              {% else %}

                {% assign full_asset_path = "/" | append: image_name %}

                <img
                  class="home-project-image"
                  src="{{ full_asset_path | relative_url }}"
                  alt="{{ project.title }}">

              {% endif %}



            <!-- JUST A FILENAME -->

            {% else %}

              {% assign image_path = "/assets/images/" | append: image_name %}

              <img
                class="home-project-image"
                src="{{ image_path | relative_url }}"
                alt="{{ project.title }}">

            {% endif %}



          <!-- NO IMAGE FOUND -->

          {% else %}

            <div class="project-placeholder">

              {{ project.title }}

            </div>

          {% endif %}



          <!-- PROJECT NAME -->

          <div class="home-project-label">

            {{ project.title }}

          </div>


        </a>


      {% endfor %}


    </div>


  </section>


</div>
