---
layout: research
title: "Sitemap"
permalink: /sitemap/
description: "Main pages and publication details on Hongwei Yan's academic website."
---

<div class="page-intro">
  <p class="eyebrow">Site index</p>
  <h1>Sitemap</h1>
  <div class="page-links"><a href="{{ '/' | relative_url }}">About</a><a href="{{ '/publications/' | relative_url }}">Publications</a><a href="{{ '/cv/' | relative_url }}">CV</a></div>
</div>
<section class="home-section" aria-labelledby="paper-pages-title">
  <h2 id="paper-pages-title">Publication detail pages</h2>
  <ul>{% for paper in site.data.research.papers %}{% if paper.legacy %}<li><a href="{{ paper.legacy | relative_url }}">{{ paper.title | escape }}</a></li>{% endif %}{% endfor %}</ul>
  <p><a href="{{ '/sitemap.xml' | relative_url }}">XML sitemap</a></p>
</section>
