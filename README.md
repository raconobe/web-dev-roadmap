Jekyll is GitHub’s original default static site generator, but those other options you see in GitHub Pages—**NuxtJS, Hugo, Gatsby, and Next.js**—are modern alternatives designed for different web development needs.

Here is how they break down, followed by a hands-on Jekyll template and resources to master it.

---

### What Are These Other Static Site Generators?

| Generator | Tech Base | Best For | Key Characteristic |
| --- | --- | --- | --- |
| **Jekyll** | Ruby | Documentation, Personal Blogs | Integrated natively into GitHub Pages without needing build actions. Uses Liquid templates + Markdown. |
| **Hugo** | Go | Massively Large Sites & Blogs | Extremely fast build speeds (compiles thousands of Markdown pages in seconds). |
| **Gatsby** | React / GraphQL | Enterprise Content Sites | Combines React components with a GraphQL data layer to pull content from headless CMSs. |
| **Nuxt.js** | Vue.js | Full-Stack Vue Web Apps | The Vue equivalent of Next.js. Supports Static Site Generation (SSG) and Server-Side Rendering (SSR). |
| **Next.js** | React | Modern Web Applications | The industry standard React framework for full-stack, dynamic, and static applications. |

---

### Hands-On Example: Building a Frontend/Backend Page with Jekyll

Jekyll uses **Liquid** markup instead of Vue components to insert dynamic logic into standard Markdown/HTML.

To test how Jekyll works, create the following two files in your `web-dev-roadmap` repository:

#### 1. Configuration File: `_config.yml`

Place this in your repository root to configure site metadata and enable Jekyll’s standard theme:

```yaml
title: "Web Dev Roadmap & Tech Vault"
description: "Comparing Static Generators with Jekyll"
theme: minima
plugins:
  - jekyll-feed

```

#### 2. Content Page: `index.md`

Create `index.md` in your repository root to see how Liquid template tags work inside Markdown:

```markdown
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

```

---

### How to Host This Jekyll Site on GitHub Pages

1. Go to your **`web-dev-roadmap`** repository on GitHub.
2. Click **Settings** -> **Pages**.
3. Under **Source**, select **Deploy from a branch**.
4. Choose the **`main`** branch and root **`/`** folder, then click **Save**.
5. GitHub will build the Jekyll site automatically (without requiring Node.js or `npm run build` commands).

---

### Where to Learn Jekyll

1. **Official Guides:**
* [Official Jekyll Documentation](https://jekyllrb.com/docs/) — Start with the *Step by Step Tutorial*.
* [Liquid Template Engine Documentation](https://shopify.github.io/liquid/) — Learn syntax for loops, variables, and filters (`{{ variable }}`, `{% for %}`).


2. **GitHub Integration:**
* [GitHub Pages & Jekyll Guide](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll) — Official step-by-step setup for GitHub-hosted Jekyll sites.



---