---
layout: archive
title: "Gallery"
permalink: /gallery/
---

Explore images and visuals from some of our events.

<style>
  .gallery-section {
    margin-bottom: 40px;
  }
  .gallery-title {
    font-size: 24px;
    margin-bottom: 10px;
  }
  .gallery-images {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
  }
  .gallery-images img {
    width: 300px;
    height: 200px;
    object-fit: cover;
    border-radius: 8px;
    border: 2px solid #ddd;
    transition: transform 0.3s;
  }
  .gallery-images img:hover {
    transform: scale(1.05);
    border-color: #007bff;
  }
</style>

---

## Summer School
Highlights from our exciting annual summer school program in The Netherlands.

{% for section in site.data.gallery %}
<div class="gallery-section">
  <div class="gallery-title">{{ section.year }}</div>
  <div class="gallery-images">
    {% for photo in section.photos %}
      <img src="/images/holland/{{ photo.file }}" alt="{{ photo.alt }}" loading="lazy">
    {% endfor %}
  </div>
</div>
{% endfor %}
