---
layout: page
title: "Java Development Course"
permalink: /java/
---

# ☕ Java Development Course

<div class="java-chapters">
  {% assign sorted_chapters = site.java | sort: 'order' %}
  {% for chapter in sorted_chapters %}
    <div class="chapter-card">
      <h2>{{ chapter.title }}</h2>
      {{ chapter.content }}
    </div>
    <hr>
  {% endfor %}
</div>