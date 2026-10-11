---
layout: research
title: "Publications"
permalink: /publications/
section: publications
description: "Publications by Hongwei Yan in brain-inspired AI and AI for Science, including continual learning, foundation-model adaptation, and neural-data modeling."
---

<div class="page-intro">
  <h1>Publications</h1>
  <div class="page-links"><a href="{{ site.data.research.scholar }}">Google Scholar <span aria-hidden="true">↗</span></a><a href="#preprints">Preprints &amp; work under review ↓</a></div>
  <p class="section-note">* Equal contribution. My name is shown in bold.</p>
</div>

{% assign published = site.data.research.papers | where: 'status', 'published' %}
{% assign groups = published | group_by: 'year' %}
{% for group in groups %}
<section class="publication-year" aria-labelledby="year-{{ group.name }}">
  <h2 id="year-{{ group.name }}">{{ group.name }}</h2>
  <div class="paper-list">{% for paper in group.items %}{% include research-paper.html paper=paper %}{% endfor %}</div>
</section>
{% endfor %}

<section class="publication-year" id="preprints" aria-labelledby="preprints-title">
  <h2 id="preprints-title">Preprints &amp; work under review</h2>
  <div class="paper-list">
    {% assign preprints = site.data.research.papers | where: 'status', 'preprint' %}
    {% for paper in preprints %}{% include research-paper.html paper=paper %}{% endfor %}
  </div>
</section>

<section class="ongoing-section" aria-labelledby="ongoing-title">
  <h2 id="ongoing-title">Ongoing work</h2>
  <article><div class="entry-heading"><h3>CoSSR · AI for multiphoton calcium imaging</h3><p class="entry-date">Manuscript in preparation</p></div><p>Co-designing acquisition and self-supervised reconstruction for high-throughput calcium imaging. Related Chinese patent application: CN122018128A, published May 12, 2026.</p></article>
</section>
