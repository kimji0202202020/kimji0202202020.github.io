---
title: Journal
layout: default
section: journal
permalink: /journal/
---

<h1 class="entry-title">Journal</h1>
<p class="entry-meta">생각과 하루를 남겨두는 곳.</p>

<ul class="entry-list">
  {% assign entries = site.journal | sort: "date" | reverse %}
  {% for entry in entries %}
  <li>
    <span class="entry-list-date">{{ entry.date | date: "%Y-%m-%d" }}</span>
    <a href="{{ entry.url | relative_url }}">{{ entry.title }}</a>
  </li>
  {% endfor %}
</ul>
