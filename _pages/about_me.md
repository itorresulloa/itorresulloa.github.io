---
layout: academic
title: "About"
permalink: /about_me/
author_profile: false
---

## Background

Before starting my PhD in economics, I worked as a research assistant at the Poverty Action Lab (J-PAL), the International Initiative for Impact Evaluation (3ie), and as a research consultant on impact evaluations for the United Nations Development Programme (UNDP), the Inter-American Development Bank (IADB), and Chilean government offices.

At the same time, I collaborated on research with various professors, primarily from the University of Chile's Department of Industrial Engineering and the Pontifical Catholic University of Chile's Department of Economics and School of Government.

## Research experience

I have experience designing, implementing, and analyzing field and online randomized controlled trials. Some of the topics that I have been involved in include early childhood development, public procurement, household finance, housing and residential mobility, migration and beliefs, and consumption warning labels.

## Education and interests

I graduated from the University of Chile with a BA in Economics and later completed a Master's degree in Philosophy of Science at the University of Santiago, Chile.

Along with experimental research and development economics, I am motivated by philosophical questions about causal inference, evidence extrapolation, and generalizability, as well as how to improve our empirical strategies to support valid causal claims.

## Beyond Economics

Outside research, I enjoy travelling, swimming, and live music. Here are a few of the places and experiences I keep track of along the way.

<div class="personal-interests">
  <details class="personal-group">
    <summary>Travel, food &amp; coffee</summary>
    <div class="personal-group__body">
      <p>I enjoy travelling and discovering good restaurants, bars, and places to try good coffee. I keep track of these adventures in Google Maps lists, in the hope that others might enjoy them too.</p>
      <ul class="personal-links">
        {% for item in site.data.personal.travel %}
        <li><a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>
  <details class="personal-group">
    <summary>Swimming</summary>
    <div class="personal-group__body">
      <p>In my free time, I enjoy swimming and am trying to swim in as many places as possible. I keep a map of the pools and natural spots where I have swum.</p>
      <ul class="personal-links">
        {% for item in site.data.personal.swimming %}
        <li><a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>
  <details class="personal-group">
    <summary>Concerts<span class="personal-group__count">{{ site.data.personal.concerts.size }} playlists</span></summary>
    <div class="personal-group__body">
      <p>I enjoy going to concerts and keep playlists of the shows I have attended.</p>
      <ul class="personal-links personal-links--concerts">
        {% assign concerts = site.data.personal.concerts | sort: 'date' | reverse %}
        {% for concert in concerts %}
        <li>
          <a href="{{ concert.url }}" target="_blank" rel="noopener noreferrer" aria-label="{{ concert.artist | escape }} at {{ concert.venue | escape }}, {{ concert.date | date: '%B %-d, %Y' }}">{{ concert.artist | escape }}</a>
          <span class="personal-link__meta">{{ concert.venue | escape }} &middot; <time datetime="{{ concert.date }}">{{ concert.date | date: '%B %-d, %Y' }}</time></span>
        </li>
        {% endfor %}
      </ul>
    </div>
  </details>
</div>
