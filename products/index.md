---
layout: base
title: Products
---

<section class="card">
  <h1>Products</h1>
  <div class="grid cols-3">
    {% for p in site.products %}
      {% include product-card.html product=p %}
    {% endfor %}
  </div>
</section>
