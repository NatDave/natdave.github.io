---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
last_updated: "September 2026"
cv_file: "https://natdave.github.io/files/NatDaveCV.pdf"
cv_pages: 6
cv_size: "314 KB"
---

{% include base_path %}

<style>
  /* Scoped to the CV page. Accent matches the blue already used on the
     publications page (#0073e6) rather than introducing a fourth shade.
     Chips and buttons are left-aligned to share the axis of the page heading
     rendered by the archive layout. */
  .cv-meta {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 0.5em 0.75em;
    margin: 0 0 1.25em;
    font-size: 0.85em;
    color: #5a6570;
  }
  .cv-chip {
    display: inline-flex;
    align-items: center;
    gap: 0.4em;
    padding: 0.3em 0.75em;
    border: 1px solid #e3e7eb;
    border-radius: 999px;
    background: #f7f9fb;
    white-space: nowrap;
  }
  .cv-chip strong { font-weight: 600; color: #2f3941; }

  .cv-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75em;
    margin-bottom: 1.75em;
  }
  .cv-btn {
    display: inline-flex;
    align-items: center;
    gap: 0.5em;
    padding: 0.7em 1.4em;
    border-radius: 8px;
    font-weight: 600;
    font-size: 0.95em;
    line-height: 1;
    text-decoration: none !important;
    transition: transform 0.15s ease, box-shadow 0.15s ease, background-color 0.15s ease;
  }
  .cv-btn--primary {
    background: #0073e6;
    color: #fff !important;
    box-shadow: 0 2px 6px rgba(0, 115, 230, 0.28);
  }
  .cv-btn--primary:hover,
  .cv-btn--primary:focus {
    background: #005bb8;
    transform: translateY(-1px);
    box-shadow: 0 5px 14px rgba(0, 115, 230, 0.34);
  }
  .cv-btn--ghost {
    background: #fff;
    color: #0073e6 !important;
    border: 1px solid #cfdae6;
  }
  .cv-btn--ghost:hover,
  .cv-btn--ghost:focus {
    border-color: #0073e6;
    background: #f2f8ff;
    transform: translateY(-1px);
  }
  /* Keyboard users get a visible focus ring; mouse users do not. */
  .cv-btn:focus-visible { outline: 3px solid #9ecbff; outline-offset: 2px; }

  /* Hidden by default and revealed by the script below, only on wide screens.
     Two reasons this is JS-gated rather than CSS-gated:
       1. A display:none iframe still downloads its src, so a CSS-only hide
          would cost phone users the full 303 KB for a viewer they never see.
       2. The frame must have its final width before the PDF viewer initialises.
          With loading="lazy" it did not, and the viewer then mis-computed its
          zoom (137%, then 102%) and clipped the right edge of the document.
     With no src until the frame is laid out, the viewer sizes itself correctly.
     No JS means no embedded preview, which is fine - the buttons above work. */
  .cv-viewer {
    display: none;
    border: 1px solid #e3e7eb;
    border-radius: 12px;
    overflow: hidden;
    background: #f4f6f8;
    box-shadow: 0 6px 24px rgba(15, 30, 50, 0.10);
  }
  .cv-viewer iframe {
    display: block;
    width: 100%;
    height: 85vh;
    min-height: 620px;
    border: 0;
  }

  @media (max-width: 768px) {
    .cv-btn { width: 100%; justify-content: center; }
  }
</style>

<div class="cv-meta">
  <span class="cv-chip">Last updated <strong>{{ page.last_updated }}</strong></span>
  <span class="cv-chip">{{ page.cv_pages }} pages</span>
  <span class="cv-chip">PDF &middot; {{ page.cv_size }}</span>
</div>

<div class="cv-actions">
  <a class="cv-btn cv-btn--primary" href="{{ page.cv_file }}" target="_blank" rel="noopener">
    Open in new tab
  </a>
  <a class="cv-btn cv-btn--ghost" href="{{ page.cv_file }}" download>
    Download PDF
  </a>
</div>

<div class="cv-viewer" id="cv-viewer">
  <iframe data-src="{{ page.cv_file }}"
          title="Curriculum Vitae of Nathan David Obeng-Amoako (PDF, {{ page.cv_pages }} pages)">
  </iframe>
</div>

<script>
  (function () {
    var wrap = document.getElementById('cv-viewer');
    if (!wrap) return;
    var frame = wrap.querySelector('iframe');
    var wide = window.matchMedia('(min-width: 769px)');

    function sync() {
      if (!wide.matches) return;              // phones keep the buttons only
      wrap.style.display = 'block';           // lay the frame out first...
      if (!frame.getAttribute('src')) {       // ...then give it a src, so the
        frame.setAttribute('src', frame.dataset.src);  // PDF viewer measures a
      }                                       // frame of its final width
    }

    sync();
    if (wide.addEventListener) {
      wide.addEventListener('change', sync);
    } else if (wide.addListener) {
      wide.addListener(sync);                 // Safari < 14
    }
  })();
</script>
