---
title: "Photo Gallery"
permalink: /gallery/
author_profile: true
---

{% include base_path %}

<style>
  .gallery {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }

  .image {
    width: 48%; /* Adjust the width as needed */
    margin-bottom: 1rem;
  }

  @media (max-width: 768px) {
    .image {
      width: 100%; /* Change to full width on smaller screens */
    }
  }
</style>

<div class="gallery">
  {% for image in site.data.gallery %}
    <div class="image">
      <a href="{{ image.path }}">
        <img src="{{ image.path }}" alt="{{ image.alt }}">
      </a>
      <div class="caption">{{ image.caption }}</div>
    </div>
  {% endfor %}
</div>
