---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
redirect_from:
  - /resume
last_updated: "September 2026"
cv_file: "https://natdave.github.io/files/NatDaveCV.pdf"
cv_pages: 6
---

{%- comment -%}
  Styles for this page (.chips, .cv-actions, .cv-viewer) live in
  assets/css/site.css with the rest of the site, so the dark theme applies.
  Update last_updated and cv_pages when a new CV is uploaded. There is no
  file-size chip: typed in by hand, it went stale on every upload.
{%- endcomment -%}

<div class="chips">
  <span class="chip">Last updated <strong>{{ page.last_updated }}</strong></span>
  <span class="chip">{{ page.cv_pages }} pages</span>
</div>

<div class="cv-actions">
  <a class="btn btn-primary" href="{{ page.cv_file }}" target="_blank" rel="noopener"><svg class="icon"><use href="#i-external"/></svg>Open in new tab</a>
  <a class="btn" href="{{ page.cv_file }}" download><svg class="icon"><use href="#i-download"/></svg>Download PDF</a>
</div>

<div class="cv-viewer" id="cv-viewer">
  <iframe data-src="{{ page.cv_file }}"
          title="Curriculum Vitae of Nathan David Obeng-Amoako (PDF, {{ page.cv_pages }} pages)">
  </iframe>
</div>

<script>
  (function () {
    /* The viewer starts hidden with no src. On wide screens it is laid out
       first and only then given its src, so the PDF viewer measures a frame
       of its final width (otherwise it mis-zooms and clips the document) and
       phones never download the PDF for a viewer they cannot use. */
    var wrap = document.getElementById('cv-viewer');
    if (!wrap) { return; }
    var frame = wrap.querySelector('iframe');
    var wide = window.matchMedia('(min-width: 769px)');

    function sync() {
      if (!wide.matches) { return; }
      wrap.style.display = 'block';
      if (!frame.getAttribute('src')) { frame.setAttribute('src', frame.dataset.src); }
    }

    sync();
    if (wide.addEventListener) { wide.addEventListener('change', sync); }
    else if (wide.addListener) { wide.addListener(sync); }
  })();
</script>
