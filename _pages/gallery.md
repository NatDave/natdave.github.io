---
layout: archive
title: "Gallery"
permalink: /gallery/
---

Explore images and visuals from various categories, including Summer School, Posters, and more.

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

## Summer School 🌞  
Highlights from our exciting summer school program in The Netherlands.

<div class="gallery-section">
  <div class="gallery-title">Delft, The Netherlands (2024)</div>
  <div class="gallery-images">
    {% for i in (1..15) %}
      <img src="/images/holland/2024_netherlands{{ i }}.jpg" alt="Summer Event {{ i }}">
    {% endfor %}
  </div>
</div>

---

## Posters 📜  
Check out some of our latest research posters.

<div class="gallery-section">
  <div class="gallery-title">Posters</div>
  <div class="gallery-images">
    <img src="/images/poster1.jpg" alt="Poster 1">
    <img src="/images/poster2.jpg" alt="Poster 2">
    <img src="/images/poster3.jpg" alt="Poster 3">
  </div>
</div>

---
