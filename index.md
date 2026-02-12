---
layout: page
title: Home
---

<section class="hero-banner">
  <div class="banner-overlay"></div>

  <div class="banner-collage">
    {% assign banner_images = site.static_files | where_exp: "file", "file.path contains '/assets/images/banner/'" %}
    {% for image in banner_images %}
      <div class="banner-item">
        <img src="{{ image.path | relative_url }}" alt="">
      </div>
    {% endfor %}
  </div>

  <div class="hero-content">
    <h1>ICT Engineer</h1>
    <p class="hero-subtitle">
      Networking · Cybersecurity · AI · Automation · Robotics
    </p>  

  <p class="hero-description">
    I work across communication infrastructure, secure systems, and applied
    artificial intelligence — with a focus on real-world deployment,
    reliability, and safety-critical environments.
  </p>
  
  </div>
</section>

<section class="wall">
  <h2>Wall of Impact</h2>

  <div class="wall-grid">
    <!-- image cards later -->
    <div class="wall-card">Enterprise Networks</div>
    <div class="wall-card">SOC & Security Ops</div>
    <div class="wall-card">AI & Automation</div>
    <div class="wall-card">Robotics Systems</div>
  </div>
</section>

<section class="cta">
  <h2>Explore</h2>
  <p>
    View my experience, education, publications, and professional affiliations.
  </p>
</section>
