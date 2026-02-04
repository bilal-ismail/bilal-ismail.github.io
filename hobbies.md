---
layout: page
title: Hobbies & Interests
---

<div class="contact-card">
  
<p> <strong>Hardware Tools & Repairs, </strong>
  Collecting tools and performing hands-on technical repairs and builds
</p>

<p> <strong>Running & Hiking, </strong>
  Regular jogging, hiking, and endurance activities
</p>

<p><strong>Continuous Upskilling, </strong>
  Self-driven learning across the intersection of IT security, AI, Communication and Automation.
</p>

</div>

<section>

  {% assign items = site.data.hobbies %}
    
  {% endcase %}

  {% if items %}
    {% assign items = items | sort: "start" | reverse %}
    <div class="contact-card">
      <section>
      {% for item in items %}
        {% item.name %}        
        {% item.description %}        
      {% endfor %}
    </div>
  {% endif %}
</section>

