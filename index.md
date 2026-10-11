---
layout: home
title: "Frontend & Backend Hub"
---

# 🚀 Web Development Roadmap (Jekyll Edition)

Welcome to the vault! Below is a comparison of Frontend vs. Backend core technologies compiled with Jekyll and Liquid tags.

---

## 🎨 Frontend Technologies

Jekyll handles lists using standard Markdown or embedded Liquid loops:

* 🏗️ **HTML5** — Document structure and semantic web.
* 🎨 **CSS3** — Flexbox, CSS Grid, and responsive design.
* ⚡ **JavaScript** — DOM manipulation, ES6+ features, and dynamic web components.

---

## ⚙️ Backend Technologies

* 🟢 **Node.js** — Event-driven JavaScript runtime for scalable network applications.
* 🐘 **PHP** — Server-side engine for dynamic web apps and database management.
* 🐹 **Go** — Compiled, concurrent backend services and microservices.

---

## 🧪 Liquid Template Test

This site was compiled at: **{{ "now" | date: "%Y-%m-%d %H:%M" }}**

{% assign tools = "Git, Debian Linux, Docker, VitePress, Jekyll" | split: ", " %}

### Developer Environment Tools:
{% for tool in tools %}
- {{ tool }}
{% endfor %}