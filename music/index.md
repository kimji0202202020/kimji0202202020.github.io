---
title: Music
layout: default
section: music
permalink: /music/
---

<h1 class="entry-title">Music</h1>
<p class="entry-meta">
  들은 음악에 대한 개인적인 기록.
  더 많은 목록은 <a href="https://rateyourmusic.com/~rlawltkd22" target="_blank" rel="noopener">rateyourmusic</a>에서.
</p>

<ul class="entry-list">
  {% assign entries = site.music | sort: "order" %}
  {% for entry in entries %}
  <li>
    <span class="rating" style="min-width:1.8rem;height:1.8rem;font-size:0.8rem;">{{ entry.rating }}</span>
    <a href="{{ entry.url | relative_url }}">{{ entry.title }}</a>
    <span class="entry-list-sub">{{ entry.creator }} · {{ entry.genre }}</span>
  </li>
  {% endfor %}
</ul>
