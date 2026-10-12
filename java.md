---
layout: doc
title: "Java Course"
permalink: /java/
---

# Java Course Overview
Welcome to the Java course module.
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