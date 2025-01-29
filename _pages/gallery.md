---
layout: archive
title: "Gallery"
permalink: /gallery/
---

Explore images and visuals from various some events.

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

<div class="gallery-section">
  <div class="gallery-title">Delft, The Netherlands (2024)</div>
  <div class="gallery-images">
    {% for i in (1..15) %}
      <img src="/images/holland/2024_netherlands{{ i }}.jpg" alt="Summer School 2024 {{ i }}">
    {% endfor %}
  </div>
</div>

---
