---
layout: single
title: "相簿"
permalink: /album/
classes: wide
---

<section class="page__content" aria-labelledby="album-title">
  <header>
    <h1 id="album-title">璞樹文旅相簿</h1>
    <p>從七感體驗到在地文化，以下照片精選了最新上傳的作品，方便於官網呈現或後續下載使用。</p>
  </header>
  <div class="feature__wrapper">
    {% assign gallery = site.data.albums.pushu %}
    {% for item in gallery %}
    <article class="feature__item">
      <div class="feature__media">
        <a href="{{ item.image | relative_url }}">
          <img src="{{ item.image | relative_url }}" alt="{{ item.alt | escape }}" loading="lazy">
        </a>
      </div>
      <div class="feature__content">
        <h3 class="feature__title">{{ item.title }}</h3>
        <p class="feature__excerpt">{{ item.description }}</p>
        <p class="feature__meta">檔案位置：<code>{{ item.image }}</code></p>
      </div>
    </article>
    {% endfor %}
  </div>
</section>
