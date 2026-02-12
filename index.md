---
layout: page
title: Home
---

<!-- =======================================================
                        HERO
======================================================= -->

{% include header.html %}

<section class="hero-banner" id="heroBanner">
  <div class="hero-grid">

    <div></div>

    <div class="hero-panel">
      <div class="hero-subtitle">
        ICT • Security • AI • Automation • Robotics
      </div>

      <h1>
        Engineering Secure Infrastructure &
        Intelligent Systems
      </h1>

      <p>
        My work spans enterprise networking, defensive security,
        and applied artificial intelligence with a growing focus
        on automation and robotics — emphasizing reliability,
        safety, and real-world deployment.
      </p>
    </div>

  </div>
</section>


<script>
  const heroImages = [
    "/assets/images/banner/banner-1.jpg",
    "/assets/images/banner/banner-2.jpg",
    "/assets/images/banner/banner-3.jpg",
    "/assets/images/banner/banner-4.jpg",
    "/assets/images/banner/banner-5.jpg",
    "/assets/images/banner/banner-6.jpg",
    "/assets/images/banner/banner-7.jpg"
  ];

  let heroIndex = 0;
  const hero = document.getElementById("heroBanner");

  function rotateHero() {
    hero.style.backgroundImage = `url(${heroImages[heroIndex]})`;
    heroIndex = (heroIndex + 1) % heroImages.length;
  }

  rotateHero();
  setInterval(rotateHero, 6000);
</script>

<!-- =======================================================
                        IMPACT
======================================================= -->

<section class="impact-section">
  <div class="impact-grid">

    <div class="impact-text">
      <h2>My Impact</h2>
      <p>
        Enterprise networking, secure systems, AI-driven automation,
        and robotics integration — delivered across mission-critical
        and real-time environments.
      </p>
    </div>

    <div class="impact-images">
      {% assign impact_images = site.static_files | where_exp: "file", "file.path contains '/assets/images/impact/'" %}
      {% for image in impact_images %}
        <img src="{{ image.path | relative_url }}" alt="">
      {% endfor %}
    </div>

  </div>
</section>

<!-- =======================================================
                        CERTIFICATIONS
======================================================= -->

<section class="cert-section">
  <div class="cert-grid">

    <div class="cert-slider-wrapper">

      <button class="slider-btn left" onclick="moveSlide(-1)">&#10094;</button>

      <div class="cert-slider" id="certSlider">
        {% assign cert_images = site.static_files | where_exp: "file", "file.path contains '/assets/images/certificates/'" %}
        {% for image in cert_images %}
          <div class="cert-slide">
            <img src="{{ image.path | relative_url }}" alt="">
          </div>
        {% endfor %}
      </div>

      <button class="slider-btn right" onclick="moveSlide(1)">&#10095;</button>

    </div>

    <div class="cert-text">
      <h2>Certifications</h2>
      <p>
        Professional credentials and specialized training
        across cybersecurity, networking, and intelligent systems.
      </p>
    </div>

  </div>
</section>

<script>
  const slider = document.getElementById("certSlider");
  let slideIndex = 0;

  function moveSlide(direction) {
    const slides = document.querySelectorAll(".cert-slide");
    slideIndex += direction;

    if (slideIndex < 0) slideIndex = slides.length - 1;
    if (slideIndex >= slides.length) slideIndex = 0;

    slider.style.transform = `translateX(-${slideIndex * 100}%)`;
  }
</script>

<!-- =======================================================
                        HIGHLIGHTS
======================================================= -->

<section class="highlights-section">
  <h2>Highlights</h2>

  <div class="highlights-grid">
    {% assign highlight_images = site.static_files | where_exp: "file", "file.path contains '/assets/images/highlights/'" %}
    {% for image in highlight_images %}
      <div class="highlight-card">
        <img src="{{ image.path | relative_url }}" alt="">
      </div>
    {% endfor %}
  </div>
</section>
