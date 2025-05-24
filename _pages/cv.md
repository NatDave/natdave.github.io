---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
last_updated: "May 2025"
---

{% include base_path %}

<div style="text-align: center; margin-top: 30px;">
  <h1 style="font-size: 2.2em; margin-bottom: 10px;">Curriculum Vitae</h1>
  <p style="font-size: 1.1em; color: #555;">
    Download or view my most recent CV, <strong>last updated {{ page.last_updated }}</strong>.
  </p>
</div>

<!-- Desktop View: Embedded PDF -->
<div class="pdf-container" style="text-align: center; margin-top: 30px;">
  <iframe 
    src="https://natdave.github.io/files/NatDaveCV.pdf" 
    width="85%" 
    height="700px" 
    style="border: 1px solid #e0e0e0; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.05);">
    Your browser does not support embedded PDFs.
    <a href="https://natdave.github.io/files/NatDaveCV.pdf">Click here to download.</a>
  </iframe>
</div>

<!-- Mobile View: Action Buttons -->
<div class="mobile-view" style="margin-top: 30px;">
  <div style="text-align: center;">
    <a href="https://natdave.github.io/files/NatDaveCV.pdf" target="_blank" 
       style="font-size: 18px; padding: 12px 24px; background-color: #0069d9; color: white; 
              text-decoration: none; border-radius: 6px; display: inline-block;">
      📄 View CV
    </a>
  </div>
  <div style="text-align: center; margin-top: 12px;">
    <p style="font-size: 0.95em; color: #555;">
      Or <a href="https://natdave.github.io/files/NatDaveCV.pdf" download>click here to download</a>.
    </p>
  </div>
</div>

<!-- Responsive Styling -->
<style>
  @media (max-width: 768px) {
    .pdf-container { display: none; }
  }
  @media (min-width: 769px) {
    .mobile-view { display: none; }
  }
</style>
