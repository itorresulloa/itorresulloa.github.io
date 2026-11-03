---
layout: academic
title: "Research"
permalink: /research/
author_profile: false
---

{% assign working_papers = site.working_papers | sort: 'date' | reverse %}
{% if working_papers.size > 0 %}
<section class="research-section" aria-labelledby="working-papers">
  <h2 id="working-papers">Working Papers</h2>
  {% for post in working_papers %}
    {% include research-entry.html %}
  {% endfor %}
</section>
{% endif %}

{% if site.publications.size > 0 %}
<section class="research-section" aria-labelledby="publications">
  <h2 id="publications">Publications</h2>
  {% for post in site.publications reversed %}
    {% include research-entry.html %}
  {% endfor %}
</section>
{% endif %}

{% if site.author.googlescholar %}
<p class="research-profile-link"><a href="{{ site.author.googlescholar }}">Google Scholar</a></p>
{% endif %}


