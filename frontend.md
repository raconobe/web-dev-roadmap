---
layout: default
title: "Frontend Roadmap"
permalink: /frontend/
---

<div class="docs-layout">

  <!-- SIDEBAR NAVIGATION -->
  <aside class="side-sidebar">
    <h3>📌 Navigation</h3>
    <ul>
      <li><a href="./">🏠 Home</a></li>
      <li><a href="./frontend/">🎨 Frontend</a></li>
      <li><a href="./backend/">⚙️ Backend</a></li>
    </ul>
  </aside>

  <!-- MAIN CONTENT -->
  <main class="docs-content">
    <p><a href="./">← Back to Home</a></p>

    <h1>🎨 Frontend Development Roadmap</h1>
    <p>Welcome to the Frontend module! Below are the core foundational technologies for building modern user interfaces.</p>

    <hr>

    <!-- PROPERLY PARSED MARKDOWN INCLUDES -->
    {% capture html_section1 %}{% include frontend-html.md %}{% endcapture %}
    {{ html_section1 | markdownify }}

    {% capture html_section2 %}{% include frontend-css.md %}{% endcapture %}
    {{ html_section2 | markdownify }}

    {% capture html_section3 %}{% include frontend-js.md %}{% endcapture %}
    {{ html_section3 | markdownify }}

    <hr>
    <p><a href="./backend/">Explore Backend Module →</a></p>
  </main>

</div>