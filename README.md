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