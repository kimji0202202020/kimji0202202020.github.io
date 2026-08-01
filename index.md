---
title: Home
layout: default
permalink: /
---

<p class="intro">
  요즘 생각하는 것들을 여기에 적어둔다. 그리고 요즘 보는 영화, 듣는 음악 취향도.
  포트폴리오는 아니고, 그냥 내가 통제하는 나만의 공간 — 나만의 SNS 같은 것.
</p>

<h2>최근 Journal</h2>
<ul class="entry-list">
  {% assign recent_journal = site.journal | sort: "date" | reverse | limit: 5 %}
  {% for entry in recent_journal %}
  <li>
    <span class="entry-list-date">{{ entry.date | date: "%Y-%m-%d" }}</span>
    <a href="{{ entry.url | relative_url }}">{{ entry.title }}</a>
  </li>
  {% endfor %}
</ul>
<p><a href="{{ '/journal/' | relative_url }}">전체 Journal 보기 &rarr;</a></p>

<h2>Films &amp; Music</h2>
<p>
  <a href="{{ '/films/' | relative_url }}">최근 본 영화</a> ·
  <a href="{{ '/music/' | relative_url }}">최근 들은 음악</a>
</p>
