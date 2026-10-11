---
layout: research
permalink: /
title: "Hongwei Yan"
section: about
description: "Hongwei Yan is a PhD student at Tsinghua University working on brain-inspired AI and AI for Science."
redirect_from:
  - /about/
  - /about.html
---

<div class="hero">
  <div class="hero-copy">
    <h1>Hongwei Yan <span class="name-zh" lang="zh">燕鸿伟</span></h1>
    <p class="hero-role">PhD student · School of Life Sciences, Tsinghua University</p>
    <p class="hero-bio">I am jointly advised by <a href="https://life.tsinghua.edu.cn/info/1035/2478.htm">Yi Zhong</a> and <a href="https://group.iiis.tsinghua.edu.cn/~maks/leader.html">Kaisheng Ma</a>. I also collaborate with <a href="https://lywang3081.github.io/">Liyuan Wang</a> in Tsinghua's Department of Psychological and Cognitive Sciences and am a research intern at the Beijing Academy of Artificial Intelligence (BAAI).</p>
    <p class="hero-bio">I trained in computer science in Tsinghua's Yao Class before starting my PhD in biology. This background shapes both sides of my research: translating mechanisms of learning and memory into machine-learning algorithms, and developing computational methods to study neural and biological data.</p>
    <div class="contact-links" aria-label="Contact and profiles">
      <a href="mailto:{{ site.data.research.email }}">Email</a>
      <a href="{{ site.data.research.scholar }}">Google Scholar</a>
      <a href="{{ site.data.research.github }}">GitHub</a>
      <a href="{{ site.data.research.cv_en | relative_url }}">CV · English</a>
      <a href="{{ site.data.research.cv_zh | relative_url }}" lang="zh">中文简历</a>
    </div>
  </div>
  <figure class="portrait">
    <img src="{{ site.data.research.portrait | relative_url }}" alt="Hongwei Yan" width="180" height="207" fetchpriority="high">
  </figure>
</div>

<section class="home-section" aria-labelledby="research-title">
  <div class="section-heading"><h2 id="research-title">Research</h2></div>
  <ul class="research-list">
    <li><strong>Brain-inspired AI.</strong> I explore how foundation models and agents can accumulate knowledge, reason, adapt over time, and improve through experience. My research draws on biological learning and memory, with published work in continual learning and generalization.</li>
    <li><strong>AI for Science.</strong> I build foundation models from neural and biological data and develop AI tools for neuroscience and computational biology, spanning multimodal representations, transcriptomics, and scientific data acquisition and analysis.</li>
  </ul>
</section>

<section class="home-section" aria-labelledby="selected-title">
  <div class="section-heading"><h2 id="selected-title">Selected publications</h2><a class="section-link" href="{{ '/publications/' | relative_url }}">All publications <span aria-hidden="true">↗</span></a></div>
  <p class="section-note">* Equal contribution.</p>
  <div class="paper-list">
    {% assign selected = site.data.research.papers | where: 'selected', true %}
    {% for paper in selected %}{% include research-paper.html paper=paper %}{% endfor %}
  </div>
</section>
