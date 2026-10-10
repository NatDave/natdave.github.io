---
layout: archive
title: "Gallery"
permalink: /gallery/
---

Explore images and visuals from some of our events.

---

## Summer School
Highlights from our exciting annual summer school program in The Netherlands.

{% comment %}
  Photos are listed in _data/gallery.yml. Thumbnails in images/holland/thumbs/
  are 600x400 (2x the display size, so they stay sharp on retina screens) and
  keep this page around 1.5 MB instead of ~18 MB. Each links to the
  full-resolution original. Regenerate thumbs after adding a photo.
  Styles (.gallery-*) live in assets/css/site.css.
{% endcomment %}
{% for section in site.data.gallery %}
<div class="gallery-section">
  <h3 class="gallery-title">{{ section.year }}</h3>
  <div class="gallery-images">
    {% for photo in section.photos %}
      <a href="/images/holland/{{ photo.file }}" target="_blank" rel="noopener" title="View full-size photo">
        <img src="/images/holland/thumbs/{{ photo.file }}" alt="{{ photo.alt }}" width="600" height="400" loading="lazy" decoding="async">
      </a>
    {% endfor %}
  </div>
</div>
{% endfor %}
