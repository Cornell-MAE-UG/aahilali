---
layout: default
title: Home
---

<div class="home-container">


  <!-- =====================================================
       INTRODUCTION
       ===================================================== -->

  <section class="home-hero">


    <!-- PROFILE PHOTO -->

    <div class="home-photo-container">

      <img
        class="home-photo"
        src="{{ '/assets/images/profile-pic.jpg' | relative_url }}"
        alt="Aahil Ali">

    </div>



    <!-- ABOUT ME -->

    <div class="home-intro">


      <h1 class="home-name">
        Aahil Ali
      </h1>


      <!--
        BIO:
        We can rewrite this later once you give me
        exactly what you want recruiters to know.
      -->

      <p class="home-bio">

        I am a Mechanical Engineering student at Cornell University
        with interests in mechanical design, manufacturing, testing,
        robotics, and engineering systems.

      </p>


      <p class="home-bio">

        My engineering experience has allowed me to work across
        design, analysis, prototyping, manufacturing, and technical
        problem solving. I am especially interested in developing
        real-world mechanical systems and products.

      </p>



      <!-- CONTACT -->

      <p class="home-contact">

        Contact me at

        <a href="mailto:aaa387@cornell.edu">
          aaa387@cornell.edu
        </a>

      </p>



      <!-- RESUME + LINKEDIN -->

      <div class="home-links">


        <!-- RESUME -->

        <a
          class="resume-download"
          href="{{ '/assets/AahilAli-Resume.pdf' | relative_url }}"
          target="_blank"
          rel="noopener">

          <i class="bi bi-file-earmark-person"></i>

          Download Resume

        </a>



        <!-- LINKEDIN -->

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



  <!-- =====================================================
       SKILLS / INTERESTS
       ===================================================== -->

  <section class="home-details">


    <!-- LEFT COLUMN: SKILLS -->

    <div>


      <h2 class="home-section-heading">
        SKILLS
      </h2>



      <!-- CHANGE LATER -->

      <div class="skill-group">

        <div class="skill-title">
          CAD & Engineering Software:
        </div>

        <p class="skill-text">
          ADD SOFTWARE HERE
        </p>

      </div>



      <!-- CHANGE LATER -->

      <div class="skill-group">

        <div class="skill-title">
          Manufacturing:
        </div>

        <p class="skill-text">
          ADD MANUFACTURING SKILLS HERE
        </p>

      </div>



      <!-- CHANGE LATER -->

      <div class="skill-group">

        <div class="skill-title">
          Programming & Technical Tools:
        </div>

        <p class="skill-text">
          ADD PROGRAMMING AND TECHNICAL TOOLS HERE
        </p>

      </div>



      <!-- CHANGE LATER -->

      <div class="skill-group">

        <div class="skill-title">
          Engineering:
        </div>

        <p class="skill-text">
          ADD ENGINEERING SKILLS HERE
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

        <li>Mechanical Design</li>

        <li>Manufacturing Engineering</li>

        <li>Automotive Engineering</li>

        <li>Aerospace Engineering</li>

        <li>Robotics & Hardware</li>

      </ul>



      <!-- =================================================
           HOBBIES

           I AM LEAVING THIS HIDDEN FOR NOW.

           When you're ready, remove the opening
           and closing comment markers and change
           the hobbies below.

      <div class="hobbies">

        <h2 class="home-section-heading">
          HOBBIES
        </h2>

        <ul class="home-list">

          <li>ADD HOBBY</li>

          <li>ADD HOBBY</li>

          <li>ADD HOBBY</li>

        </ul>

      </div>

           ================================================= -->


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


      <!--
        DO NOT MANUALLY ADD PROJECTS HERE.

        Every file inside _projects automatically
        becomes a project card on this homepage.
      -->


      {% assign homepage_projects = site.projects | sort: "path" | reverse %}


      {% for project in homepage_projects %}


        <a
          class="home-project-card"
          href="{{ project.url | relative_url }}">



          <!-- ===============================
               PROJECT IMAGE
               =============================== -->

          {% if project.image %}


            {% assign image_name = project.image %}

            {% assign first_four = image_name | slice: 0, 4 %}

            {% assign first_character = image_name | slice: 0, 1 %}



            <!-- ONLINE IMAGE -->

            {% if first_four == "http" %}


              <img
                class="home-project-image"
                src="{{ image_name }}"
                alt="{{ project.title }}">



            <!-- IMAGE ALREADY HAS assets/ IN PATH -->

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



            <!-- JUST AN IMAGE FILENAME -->

            {% else %}


              {% assign image_path = "/assets/images/" | append: image_name %}


              <img
                class="home-project-image"
                src="{{ image_path | relative_url }}"
                alt="{{ project.title }}">


            {% endif %}



          <!-- NO PROJECT IMAGE YET -->

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
