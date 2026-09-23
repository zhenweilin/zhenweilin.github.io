---
layout: academic
permalink: /
title: "Zhenwei Lin"
description: "Zhenwei Lin is a postdoctoral researcher at Purdue University working on first-order optimization methods, structured nonsmooth optimization, and scalable conic solvers."
redirect_from:
  - /about/
  - /about.html
---

<section class="hero" id="about" aria-labelledby="intro-title">
  <div class="hero-copy">
    <p class="eyebrow">Optimization · Theory &amp; Computation</p>
    <h1 id="intro-title">Zhenwei Lin<span class="name-dot">.</span></h1>
    <p class="hero-role">Postdoctoral Researcher <span aria-hidden="true">/</span> Purdue University</p>
    <p class="hero-lead">I develop first-order methods that adapt to unknown problem structure, and build scalable solvers for large-scale optimization.</p>
    <p class="hero-bio">At Purdue, I work with <a href="https://sites.google.com/view/jimmy-zhe-zhang/home">Zhe (Jimmy) Zhang</a>. Previously, I received my Ph.D. from Shanghai University of Finance and Economics, advised by <a href="https://www.acem.sjtu.edu.cn/en/faculty/dengqi.html">Qi Deng</a>.</p>
    <div class="hero-links">
      <a class="contact-link" href="mailto:{{ site.author.email }}">Get in touch <span aria-hidden="true">↗</span></a>
      <a href="{{ site.author.googlescholar | escape }}">Google Scholar <span aria-hidden="true">↗</span></a>
      <a href="{{ '/cv/' | relative_url }}">CV <span aria-hidden="true">↗</span></a>
    </div>
  </div>
  <figure class="hero-portrait">
    <img src="{{ '/images/profile.png' | relative_url }}" width="1086" height="960" alt="Zhenwei Lin by the sea" fetchpriority="high">
    <figcaption>Exploring structure.<br>Building better algorithms.</figcaption>
  </figure>
</section>

<aside class="recent-note" aria-label="Latest research">
  <span class="note-label">Latest · Sep 2026</span>
  <p>New preprints: <a href="https://arxiv.org/abs/2609.03251">APEX II for function-constrained optimization ↗</a> and <a href="https://arxiv.org/abs/2609.11480">linear convergence of the proximal bundle method ↗</a></p>
</aside>

<section class="home-section" id="research" aria-labelledby="research-title">
  <div class="section-heading"><div><p class="eyebrow">01 / Research</p><h2 id="research-title">From structure to algorithms.</h2></div></div>
  <div class="research-grid">
    <article>
      <span class="research-index" aria-hidden="true">01</span>
      <h3>Adaptive first-order methods</h3>
      <p>I study how algorithms can exploit unknown smoothness and growth conditions, with a focus on structured nonsmooth and function-constrained optimization.</p>
      <p class="research-keywords">Complexity guarantees · Bundle &amp; level methods</p>
    </article>
    <article>
      <span class="research-index" aria-hidden="true">02</span>
      <h3>Optimization at scale</h3>
      <p>I develop practical solvers for large-scale conic and semidefinite programs, connecting first-order algorithms with low-rank structure and GPU computation.</p>
      <p class="research-keywords">Conic programming · Low-rank methods · GPUs</p>
    </article>
  </div>
</section>

<section class="home-section" id="publications" aria-labelledby="publications-title">
  <div class="section-heading"><div><p class="eyebrow">02 / Selected work</p><h2 id="publications-title">Recent ideas &amp; results.</h2></div><a class="section-link" href="{{ '/publications/' | relative_url }}">All publications <span aria-hidden="true">↗</span></a></div>
  <div class="publication-list">
    {% assign selected_papers = site.publications | where_exp: 'paper', 'paper.selected_order != nil' | sort: 'selected_order' %}
    {% for paper in selected_papers %}{% include publication-entry.html paper=paper featured=true %}{% endfor %}
  </div>
</section>

<section class="contact-section" aria-labelledby="contact-title">
  <div><p class="eyebrow">Get in touch</p><h2 id="contact-title">Let’s talk optimization.</h2><p>For research discussions and potential collaborations.</p></div>
  <a href="mailto:{{ site.author.email }}">{{ site.author.email }} <span aria-hidden="true">↗</span></a>
</section>
