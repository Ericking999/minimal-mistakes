---
layout: single
title: "相簿"
permalink: /album/
author_profile: false
classes: "wide"
---

{% assign album_items = site.data.gallery %}

<div class="grid__wrapper" style="--grid-gap: 1.5rem; margin-top: 1.5rem;">
  {% for item in album_items %}
  <article class="grid__item" style="box-shadow: 0 10px 30px rgba(0,0,0,0.08); border-radius: 12px; overflow: hidden; background: #fff;">
    <figure style="margin: 0;">
      <img src="{{ item.image }}" alt="{{ item.alt }}" loading="lazy" style="display: block; width: 100%; height: auto;">
      <figcaption style="padding: 1rem 1.25rem;">
        <h3 style="margin: 0 0 0.35rem 0; font-size: 1.05rem;">{{ item.title }}</h3>
        <p style="margin: 0; color: #5f6c80;">{{ item.description }}</p>
      </figcaption>
    </figure>
  </article>
  {% endfor %}
</div>
