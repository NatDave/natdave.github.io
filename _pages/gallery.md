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
  /* Each thumbnail is wrapped in a link to the full-size photo; block display
     with no line-height stops the theme's inline link styling from adding a
     stray gap or underline under the image. */
  .gallery-images a {
    display: block;
    line-height: 0;
    text-decoration: none;
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

{% comment %}
  Thumbnails in images/holland/thumbs/ are 600x400 (2x the CSS display box, so
  they stay sharp on retina screens) and cut this page from ~18 MB to ~1.5 MB.
  Each one links to the full-resolution original, which is otherwise
  unreachable. Regenerate thumbs after adding a photo - see _data/gallery.yml.
{% endcomment %}
{% for section in site.data.gallery %}
<div class="gallery-section">
  <div class="gallery-title">{{ section.year }}</div>
  <div class="gallery-images">
    {% for photo in section.photos %}
      <a href="/images/holland/{{ photo.file }}" target="_blank" rel="noopener" title="View full-size photo">
        <img src="/images/holland/thumbs/{{ photo.file }}" alt="{{ photo.alt }}" width="300" height="200" loading="lazy" decoding="async">
      </a>
    {% endfor %}
  </div>
</div>
{% endfor %}
