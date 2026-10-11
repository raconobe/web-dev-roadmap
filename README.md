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



Only if the folder isn't initialized as a Git repository yet!

Run this command inside your folder to check:

```bash
ls -la

```

* **If you see a `.git` folder in the list:** You do **not** need `git init`. Jump straight to staging and pushing.
* **If you DO NOT see a `.git` folder:** Run `git init` first, then link your GitHub repository.

---

Yes! That is the beauty of Jekyll on GitHub Pages: no complex build configs or Node dependencies needed—just clean Markdown files processed automatically.

Here is how to expand your `web-dev-roadmap` project into a multi-page site with an updated, polished theme.

---

### Step 1: Upgrade to a Polished Theme (`jekyll-theme-architect` or `cayman`)

Update `_config.yml` in your repository root to use the modern, styled **`architect`** theme (or **`cayman`**):

```yaml
title: "Web Development Roadmap"
description: "A multi-page developer vault powered by Jekyll"
theme: jekyll-theme-architect

```

---

### Step 2: Create `frontend.md`

Create a file named `frontend.md` in your repository root:

```markdown
---
layout: default
title: "Frontend Development"
---

[← Back to Home](./)

# 🎨 Frontend Development Roadmap

Welcome to the Frontend module! Below are the core foundational technologies for building modern user interfaces.

---

## 🏗️ 1. HTML5
* **Semantic Elements:** Standardized document layout (`<header>`, `<nav>`, `<article>`, `<footer>`).
* **Accessibility (a11y):** ARIA roles, image alt texts, and keyboard navigation.

## 🎨 2. CSS3
* **Layout Engines:** Master **Flexbox** for 1D alignments and **CSS Grid** for 2D page layouts.
* **Responsive Design:** Media queries and fluid units (`rem`, `vw`, `%`).

## ⚡ 3. JavaScript (ES6+)
* **Core Syntax:** Variables (`const`/`let`), arrow functions, destructuring, and modules.
* **DOM & Async:** Modifying elements, handling events, and `fetch()` API for backend integration.

---

[Explore Backend Module →](./backend)

```

---

### Step 3: Create `backend.md`

Create a file named `backend.md` in your repository root:

```markdown
---
layout: default
title: "Backend Development"
---

[← Back to Home](./)

# ⚙️ Backend Development Roadmap

Welcome to the Backend module! This guide covers server-side architectures, API design, and database integration.

---

## 🟢 1. Node.js
* **Event Loop & Runtimes:** Non-blocking I/O operations and asynchronous execution.
* **REST APIs:** Building server endpoints using Express.js or Fastify.

## 🐘 2. PHP
* **Server-Side Scripting:** Processing forms, session handling, and database integration via PDO.
* **Object-Oriented Design:** OOP principles and modern MVC framework patterns (Laravel).

## 🐹 3. Go
* **High Performance:** Compiled binaries, strong typing, and minimal memory footprint.
* **Concurrency:** Managing parallel operations effortlessly using Goroutines and Channels.

---

[Explore Frontend Module →](./frontend)

```

---

### Step 4: Update `index.md` with Multi-Page Navigation

Update your root `index.md` to link everything together cleanly:

```markdown
---
layout: default
title: "Home"
---

# 🚀 Web Development Roadmap Vault

Welcome to the central hub! Click any module below to dive into structured learning paths and core developer topics.

---

## 📚 Vault Modules

* 🎨 **[Frontend Development Roadmap](./frontend)**  
  *HTML5, CSS3, JavaScript, Responsive Design, and UI Frameworks.*

* ⚙️ **[Backend Development Roadmap](./backend)**  
  *Node.js, PHP, Go, REST APIs, and Databases.*

---

## 🧪 Jekyll Dynamic Feature Test

This page was generated automatically by GitHub Pages on **{{ "now" | date: "%B %d, %Y" }}**.

```

---

### Step 5: Stage, Commit, and Push

Run these commands in your terminal to deploy the update:

```bash
git add .
git commit -m "Upgrade Jekyll theme to Architect and add Frontend/Backend pages"
git push -u origin main

```

Once GitHub Pages builds the site (~1 minute), refresh `[https://raconobe.github.io/web-dev-roadmap/](https://raconobe.github.io/web-dev-roadmap/)` to see the polished theme and multi-page navigation in action!



---

### Step-by-Step for a New Repository

If this is a completely fresh folder on your machine, run these commands in order:

```bash
cd ~/Desktop/projects-vault-raco/web-dev-roadmap

# 1. Initialize local repository
git init

# 2. Stage all created files (_config.yml, index.md, etc.)
git add .

# 3. Create your first commit
git commit -m "Initialize Jekyll site structure and roadmap"

# 4. Set main as the default branch
git branch -M main

# 5. Connect your local folder to your remote GitHub repository
git remote add origin git@github.com-raco:raconobe/web-dev-roadmap.git

# 6. Push your files to GitHub
git push -u origin main

```

*(Note: If you created the repository on GitHub with HTTPS instead of SSH, use `[https://github.com/raconobe/web-dev-roadmap.git](https://github.com/raconobe/web-dev-roadmap.git)` in step 5).*

Once pushed, head over to **Settings -> Pages** in your GitHub repository and set the branch source to **`main`** / **`/(root)`**!



----


The **Architect** theme takes up huge vertical space with that header banner and handwritten font.

For a functional, space-efficient documentation layout, Jekyll's official **`jekyll-theme-primer`** (GitHub's standard design system) or **`jekyll-theme-slate`** gives you a much cleaner, compact presentation.

We can also add custom CSS to format your modules as **side-by-side functional cards** with top navigation links.

---

### Step 1: Switch to `jekyll-theme-primer` and Add Navigation Header

Update `_config.yml` in your project root:

```yaml
title: "Web Dev Vault"
description: "Structured Developer Roadmap & Knowledge Base"
theme: jekyll-theme-primer

```

---

### Step 2: Inject Custom CSS for Responsive Cards

Jekyll allows custom CSS overrides easily. Create a file at `assets/css/style.scss`:

```scss
---
---
@import "{{ site.theme }}";

/* Compact container max-width */
.container-lg {
  max-width: 1080px !important;
}

/* Custom Navigation Bar */
.top-nav {
  display: flex;
  gap: 15px;
  background: #24292e;
  padding: 12px 20px;
  border-radius: 6px;
  margin-bottom: 25px;
}

.top-nav a {
  color: #ffffff;
  font-weight: 600;
  text-decoration: none;
  font-size: 0.95rem;
}

.top-nav a:hover {
  color: #58a6ff;
}

/* Grid layout for Functional Cards */
.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  margin-top: 20px;
}

.card {
  border: 1px solid #e1e4e8;
  border-radius: 8px;
  padding: 20px;
  background: #f6f8fa;
  transition: transform 0.2s, box-shadow 0.2s;
}

.card:hover {
  transform: translateY(-3px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  border-color: #0366d6;
}

.card h3 {
  margin-top: 0;
}

.card p {
  color: #586069;
  font-size: 0.9rem;
}

```

---

### Step 3: Update `index.md` with Card Grid Layout

Update `index.md` to render the grid view:

```markdown
---
layout: default
title: "Home"
---

<div class="top-nav">
  <a href="./">🏠 Home</a>
  <a href="./frontend">🎨 Frontend</a>
  <a href="./backend">⚙️ Backend</a>
</div>

# 🚀 Web Development Roadmap Vault

Welcome to the central developer hub! Select a functional path below to explore structured learning modules.

<div class="card-grid">
  <div class="card">
    <h3>🎨 <a href="./frontend">Frontend Roadmap</a></h3>
    <p>Semantic HTML5, CSS layout engines (Flexbox/Grid), modern JavaScript (ES6+), and responsive UI design.</p>
  </div>

  <div class="card">
    <h3>⚙️ <a href="./backend">Backend Roadmap</a></h3>
    <p>Node.js runtime, PHP MVC engines, Go concurrency, REST API architectures, and SQL database management.</p>
  </div>
</div>

---

### 🛠️ Vault Information

* **Generated On:** {{ "now" | date: "%B %d, %Y" }}
* **Engine:** Jekyll Static Generator on GitHub Pages

```

---

### Step 4: Update `frontend.md` and `backend.md` Headers

In both `frontend.md` and `backend.md`, add the `<div class="top-nav">` snippet right under the frontmatter so navigation stays persistent across pages:

```markdown
<div class="top-nav">
  <a href="./">🏠 Home</a>
  <a href="./frontend">🎨 Frontend</a>
  <a href="./backend">⚙️ Backend</a>
</div>

```

---

### Step 5: Push Updates

```bash
git add .
git commit -m "Switch to compact Primer theme with CSS grid cards and top nav"
git push -u origin main

```

When GitHub Pages finishes building (~1 minute), do a hard refresh (**`Ctrl + Shift + R`**). The huge header banner will be replaced by a clean, space-optimized dashboard layout!



----


Finding themes for both Jekyll and VitePress is easy once you know where to look. Because Jekyll relies on CSS/Ruby templates and VitePress relies on Vue/Tailwind, their theme marketplaces operate differently.

---

### Where to Find Jekyll Themes

Since GitHub Pages natively supports Jekyll, the theme ecosystem is massive, offering thousands of free, open-source options ranging from minimal blogs to full documentation hubs.

1. **Top Directories & Marketplaces:**
* **[JekyllThemes.io](https://jekyllthemes.io/):** Curated list of high-quality portfolio, blog, and documentation themes.
* **[Dr. Jekyll’s Themes](https://drjekyllthemes.github.io/):** Over 200+ free open-source themes with live demos.
* **[Jamstack Themes (Jekyll)](https://jamstackthemes.dev/ssg/jekyll/):** Modern Jamstack-focused designs.
* **[GitHub Topic `#jekyll-theme](https://github.com/topics/jekyll-theme)`:** Direct open-source repositories you can fork or add to your `_config.yml`.


2. **Popular Jekyll Themes to Check Out:**
* **`Minimal Mistakes`:** The gold standard for Jekyll—highly customizable, dark mode, multi-author, and space-efficient.
* **`Just the Docs`:** Designed specifically for developer documentation, search indexing, and deep navigation trees.
* **`Chirpy`:** A sleek, modern, tech-blog/vault theme with built-in code highlighting and sidebar navigation.



---

### Where to Find VitePress Themes

VitePress ships with a flexible **Default Theme** that supports dark mode, automatic sidebars, top navs, and search out of the box. However, if you want completely different designs (like blogs, custom portfolios, or API docs), you can browse community themes.

1. **Top Directories & Search Channels:**
* **[GitHub Topic `#vitepress-theme](https://github.com/topics/vitepress-theme)`:** The primary hub where developers publish open-source VitePress themes.
* **[Awesome VitePress](https://www.google.com/search?q=https://github.com/vitepress-awesome/awesome-vitepress):** A community-curated list of plugins, themes, and showcase sites.


2. **Popular VitePress Custom Themes & Extensions:**
* **`vitepress-theme-blog` / `vitepress-theme-trigger`:** Transforms VitePress from a documentation layout into a clean personal tech blog.
* **`vitepress-theme-carbon`:** A dark-mode inspired theme built on IBM's Carbon design system.
* **`vitepress-theme-api`:** Specifically designed for displaying REST API routes, payloads, and code snippets side-by-side.



---

### How Theme Customization Fits with Your Backend (Node/PHP)

Whether you choose Jekyll or VitePress, remember that **the theme only affects the UI presentation layer**:

* **If using Jekyll:** You tweak CSS/SASS files inside `assets/css/` or Liquid templates in `_layouts/`.
* **If using VitePress:** You can customize styling using CSS variables or Tailwind CSS in `.vitepress/theme/index.js`, while still embedding Vue components that fetch live data from your Node.js or PHP REST API.