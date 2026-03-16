---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

<div class="research-note">
This page collects my published research.
</div>

{% if author.googlescholar %}
  <p>You can also find my articles on <a href="{{author.googlescholar}}"><u>my Google Scholar profile</u></a>.</p>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}


