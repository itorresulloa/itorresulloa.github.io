---
layout: academic
permalink: /
title: ""
excerpt: ""
author_profile: false
redirect_from: 
  - /about/
  - /about.html
---

<div class="home-profile">
  <aside class="home-profile__identity" aria-label="Academic profile">
    <img class="home-profile__photo" src="{{ site.author.avatar | prepend: '/images/' | relative_url }}" alt="{{ site.author.name }}">
    <p class="home-profile__bio">{{ site.author.bio }}</p>
    <div class="home-profile__profiles">
      {% if site.author.googlescholar %}<a href="{{ site.author.googlescholar }}">Google Scholar</a>{% endif %}
      {% if site.author.orcid %}<a href="{{ site.author.orcid }}">ORCID</a>{% endif %}
    </div>
  </aside>
  <div class="home-intro">
    <h1 class="home-title">Hello, I am Ignacio Torres-Ulloa.</h1>
    <p>I am a fifth-year PhD candidate in the <strong>Department of Economics at the University of Southern California</strong>.</p>
    <p>My research connects migration, labor markets, and finance to understand firm behavior, productivity, and the mechanisms within firms.</p>
    <p>I also study questions about the state and civil servants. My broader interests include development and behavioral economics, causal inference, and philosophy of science.</p>
    <div class="home-contact">
      <a class="btn" href="{{ '/files/CV_Ignacio_Torres_Ulloa.pdf' | relative_url }}">Download CV</a>
      <a href="mailto:{{ site.author.email }}">{{ site.author.email }}</a>
    </div>
  </div>
</div>

<!--
Future section idea: featured papers or featured research.
<div class="feature__wrapper">
  Add one or two highlighted papers here when ready.
</div>
-->
