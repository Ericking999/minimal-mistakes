---
layout: single
title: "品牌照片相簿"
permalink: /album/
classes: wide
excerpt: "精選旅宿照片與香氛展場畫面，完整呈現城市感官療癒體驗。"
toc: false
---

<section class="page__content" aria-labelledby="album-title">
  <header>
    <h1 id="album-title">品牌照片相簿</h1>
    <p class="page__lead">已將上傳的照片整理到 <code>/assets/images/pushu-gallery/</code>，並以 <code>_data/gallery.yml</code> 統一管理標題與描述。</p>
    <p>圖輯涵蓋香氛體驗、設計語言與在地文化場景，方便官網導覽與行銷素材使用。</p>
  </header>

  <div class="feature__wrapper">
    {% assign gallery = site.data.gallery %}
    {% for item in gallery %}
    <article class="feature__item">
      <div class="feature__media">
        <img src="{{ item.image | relative_url }}" alt="{{ item.alt | escape }}" loading="lazy">
      </div>
      <div class="feature__content">
        <h3 class="feature__title">{{ item.title }}</h3>
        <p class="feature__excerpt">{{ item.description }}</p>
      </div>
    </article>
    {% endfor %}
  </div>
</section>
