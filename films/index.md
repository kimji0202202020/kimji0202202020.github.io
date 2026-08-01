---
title: Films
layout: default
section: films
permalink: /films/
---

<h1 class="entry-title">Films</h1>
<p class="entry-meta">
  본 영화에 대한 개인적인 기록.
  더 많은 목록은 <a href="https://letterboxd.com/kmjs/" target="_blank" rel="noopener">letterboxd</a>에서.
</p>

<ul class="entry-list">
  {% assign entries = site.films | sort: "order" %}
  {% for entry in entries %}
  <li>
    <span class="rating" style="min-width:1.8rem;height:1.8rem;font-size:0.8rem;">{{ entry.rating }}</span>
    <a href="{{ entry.url | relative_url }}">{{ entry.title }}</a>
    <span class="entry-list-sub">{{ entry.creator }} · {{ entry.genre }}</span>
  </li>
  {% endfor %}
</ul>
