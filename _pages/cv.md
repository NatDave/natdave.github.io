---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
last_updated: "February 2025"
---

{% include base_path %}

<div style="text-align: center;">
    <h2>Curriculum Vitae</h2>
    <p>
        A PDF copy of my CV, <strong>last updated {{ page.last_updated }}</strong>, is available below:
    </p>
</div>

<!-- Desktop: Embedded PDF -->
<div class="pdf-container">
    <iframe src="https://natdave.github.io/files/NatDaveCV.pdf" width="90%" height="700px" style="border: 1px solid #ccc; border-radius: 5px;">
        Your browser does not support PDFs.
        Please <a href="https://natdave.github.io/files/NatDaveCV.pdf">download the PDF here</a>.
    </iframe>
</div>

<!-- Mobile: View & Download Button -->
<div class="mobile-view">
    <div style="text-align: center; margin-top: 20px;">
        <a href="https://natdave.github.io/files/NatDaveCV.pdf" target="_blank" 
           style="font-size: 18px; padding: 10px 20px; background-color: #007bff; color: white; 
                  text-decoration: none; border-radius: 5px;">
            📄 View CV
        </a>
    </div>
    <div style="text-align: center; margin-top: 10px;">
        <p>If the CV does not open, <a href="https://natdave.github.io/files/NatDaveCV.pdf" download>click here to download</a>.</p>
    </div>
</div>

<!-- Hide iframe on mobile, show buttons instead -->
<style>
    @media (max-width: 768px) {
        .pdf-container { display: none; }  /* Hide iframe for mobile */
    }
    @media (min-width: 769px) {
        .mobile-view { display: none; }  /* Hide buttons for desktop */
    }
</style>
