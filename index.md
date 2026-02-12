---
layout: page
title: Home
---

<!-- =========================
        HERO SECTION
========================= -->

<section class="hero-banner">
  <div class="hero-content">
    <div class="hero-subtitle">
      ICT • Security • AI • Automation • Robotics
    </div>

    <h1>
      Engineering Secure Infrastructure &
      Intelligent Systems
    </h1>

    <p class="hero-description">
      My work spans enterprise networking, defensive security, and applied artificial intelligence,
      with a growing focus on automation and robotics. Over time, my trajectory has moved from
      communication infrastructure to intelligent systems — emphasizing reliability,
      safety, and real-world deployment.
    </p>
  </div>
</section>

<!-- =========================
        WALL OF IMPACT
========================= -->

<section class="wall">
  <h2>My Impact</h2>

  <div class="wall-grid">
    <div class="wall-card">Enterprise Networking</div>
    <div class="wall-card">Secure Real-Time Applications</div>
    <div class="wall-card">Defensive Security</div>
    <div class="wall-card">Artificial Intelligence</div>
    <div class="wall-card">Automation Systems</div>
    <div class="wall-card">Robotics Integration</div>
  </div>
</section>

<!-- =========================
        CERTIFICATES SLIDER
========================= -->

<section class="slider-section">
  <h2>Credentials & Certifications</h2>

  <div class="slider-container">
    <div class="slider-track">

      {% assign cert_images = site.static_files | where_exp: "file", "file.path contains '/assets/images/certificates/'" %}

      {% for image in cert_images %}
        <div class="slide">
          <img src="{{ image.path | relative_url }}" alt="">
        </div>
      {% endfor %}

      {% for image in cert_images %}
        <div class="slide">
          <img src="{{ image.path | relative_url }}" alt="">
        </div>
      {% endfor %}

    </div>
  </div>
</section>

<!-- =========================
        HIGHLIGHTS SLIDER
========================= -->

<section class="slider-section">
  <h2>Highlights</h2>

  <div class="manual-slider">

    {% assign highlight_images = site.static_files | where_exp: "file", "file.path contains '/assets/images/highlights/'" %}

    {% for image in highlight_images %}
      <div class="manual-slide">
        <img src="{{ image.path | relative_url }}" alt="">
      </div>
    {% endfor %}

  </div>
</section>
