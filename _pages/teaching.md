---
layout: academic
title: "Teaching"
permalink: /teaching/
author_profile: false
---

My teaching at the University of Southern California includes teaching assistantships and substitute lecturing in econometrics and economic development.

## Courses

{% if site.data.teaching.courses.size > 0 %}
<ul class="teaching-course-list">
{% for course in site.data.teaching.courses %}
  <li>
    <strong>{{ course.code }}</strong> {{ course.title }}
    <span class="entry-meta">{{ course.role | default: 'Teaching Assistant' }}{% if course.term %} &middot; {{ course.term }}{% endif %}</span>
  </li>
{% endfor %}
</ul>
{% else %}
Course details will be added here.
{% endif %}

## Student Feedback

Since joining the PhD program, I have collected student feedback about my performance to improve my teaching skills. I use these surveys to reflect on my explanations, discussion sections, and support for students.

{% assign feedback = site.data.teaching_feedback %}
{% if feedback %}
<p>The summary below uses {{ feedback.sample_size }} responses with valid ratings on all six teaching questions, collected from {{ feedback.period_start }} to {{ feedback.period_end }}.</p>

<dl class="teaching-metrics">
  <div>
    <dt>Overall TA performance</dt>
    <dd>{{ feedback.overall.mean_display }}<span class="teaching-metrics__unit">/5</span><small>{{ feedback.overall.n }} valid ratings</small></dd>
  </div>
  <div>
    <dt>Good or very good overall</dt>
    <dd>{{ feedback.overall.positive_display }}%<small>{{ feedback.overall.positive_n }} of {{ feedback.overall.n }} rated 4 or 5</small></dd>
  </div>
  <div>
    <dt>Good or very good communication</dt>
    <dd>{{ feedback.communication.positive_display }}%<small>{{ feedback.communication.positive_n }} of {{ feedback.communication.n }} rated 4 or 5</small></dd>
  </div>
</dl>

<figure class="teaching-feedback-chart">
  <picture>
    <source media="(max-width: 600px)" srcset="{{ '/images/teaching-feedback-mobile.png' | relative_url }}">
    <img src="{{ '/images/teaching-feedback.png' | relative_url }}" alt="Teaching ratings grouped as 1, 2 or 3, and 4 or 5, using the same sample across six dimensions. The full numerical results are in Survey details below." loading="lazy">
  </picture>
  <figcaption>All questions use the same {{ feedback.sample_size }} responses. Ratings of 1 are shown separately from ratings of 2 or 3; no ratings of 1 occur in this sample. Percentages are rounded.</figcaption>
</figure>

Across the courses I have taught, students have appreciated my responsiveness, availability, and flexibility in making time to meet and help them. I draw on my knowledge of the material to explain concepts in different ways, combining theory, visual explanations, and examples to help students build their understanding. I aim to create an approachable and supportive environment where students feel comfortable asking questions. Students have also valued my willingness to adapt my teaching to their needs and the encouragement I provide along the way.

<details class="feedback-method">
  <summary>Survey details and full statistics</summary>
  <p>These results come from my own student feedback survey. Responses are included only when all six rating questions have valid scores from 1 to 5. Open-ended comments are optional.</p>
  <div class="feedback-table-wrap" role="region" aria-label="Teaching survey statistics" tabindex="0">
    <table>
      <thead><tr><th scope="col">Dimension</th><th scope="col">Mean /5</th><th scope="col">Rated 4 or 5</th><th scope="col">Valid n</th></tr></thead>
      <tbody>
        {% for metric in feedback.metrics %}
        <tr><th scope="row">{{ metric.label }}</th><td>{{ metric.mean_display }}</td><td>{{ metric.positive_n }}/{{ metric.n }}</td><td>{{ metric.n }}</td></tr>
        {% endfor %}
      </tbody>
    </table>
  </div>
</details>
{% endif %}
