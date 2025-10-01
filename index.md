---
layout: base
title: Home
description: Field-proven IT tools for real work.
---

<section class="hero">
  <h1>SilentByte Labs — Field-Proven IT Tools</h1>
  <p>Minimal, robust tools for real work. Offline-first. Privacy-first. Clear flows.</p>
  <p><a class="btn primary" href="/products/">Explore Products</a>
     <a class="btn" href="/blog/">Read Blog</a></p>
</section>

<section>
  <h2>Products</h2>
  <div class="grid cols-3">
    {% for p in site.products %}
      {% include product-card.html product=p %}
    {% endfor %}
  </div>
</section>

<section>
  <h2>From the Blog</h2>
  <div class="grid cols-3">
    {% assign posts = site.posts | slice: 0,3 %}
    {% for post in posts %}
      <article class="card">
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p><small>{{ post.date | date: "%Y-%m-%d" }}</small></p>
        <p>{{ post.excerpt | strip_html | truncate: 140 }}</p>
        <p><a href="{{ post.url }}">Read more →</a></p>
      </article>
    {% endfor %}
  </div>
</section>
