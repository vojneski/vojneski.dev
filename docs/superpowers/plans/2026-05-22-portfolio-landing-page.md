# vojneski.dev Portfolio Landing Page Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a minimal single-page personal portfolio and landing page for vojneski.dev, hosted on GitHub Pages.

**Architecture:** Two files — `index.html` (markup) and `style.css` (styles). No JavaScript, no build step, no dependencies. GitHub Pages serves `index.html` from the `main` branch root. A `CNAME` file configures the custom domain.

**Tech Stack:** HTML5, CSS3, GitHub Pages

---

## File Map

| File | Responsibility |
|------|----------------|
| `index.html` | Full page markup: hero, about, skills, links |
| `style.css` | All visual styles: reset, typography, layout, responsive |
| `CNAME` | Custom domain declaration for GitHub Pages |

---

### Task 1: Create base HTML scaffold and CSS foundation

**Files:**
- Create: `index.html`
- Create: `style.css`

- [ ] **Step 1: Create `style.css` with CSS reset, variables, and base typography**

```css
*, *::before, *::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

:root {
  --color-bg: #ffffff;
  --color-text: #111111;
  --color-muted: #666666;
  --color-border: #e5e5e5;
  --font-sans: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;
  --font-mono: 'JetBrains Mono', 'Fira Code', 'Cascadia Code', monospace;
}

body {
  background: var(--color-bg);
  color: var(--color-text);
  font-family: var(--font-sans);
  font-size: 1rem;
  line-height: 1.6;
}

main {
  max-width: 680px;
  margin: 0 auto;
  padding: 4rem 1.5rem;
}

section {
  margin-bottom: 4rem;
}

h2 {
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--color-muted);
  margin-bottom: 1rem;
}
```

- [ ] **Step 2: Create `index.html` scaffold**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Vladimir Vojneski — DevOps Engineer</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <main>
  </main>
</body>
</html>
```

- [ ] **Step 3: Open in browser and verify — white page, no layout shift, correct font rendering**

```bash
xdg-open index.html
# Or open index.html in your browser manually
```

Expected: blank white page, no scrollbars, no default margins

- [ ] **Step 4: Commit**

```bash
git add index.html style.css
git commit -m "feat: add base HTML scaffold and CSS foundation"
```

---

### Task 2: Hero section

**Files:**
- Modify: `index.html` (add hero section inside `<main>`)
- Modify: `style.css` (add hero styles)

- [ ] **Step 1: Add hero HTML inside `<main>`**

```html
<section class="hero">
  <h1>Vladimir Vojneski</h1>
  <p class="title">DevOps Engineer</p>
  <p class="tagline">Building reliable infrastructure with Terraform, Kubernetes, and cloud-native tools.</p>
</section>
```

- [ ] **Step 2: Add hero styles to `style.css`**

```css
h1 {
  font-family: var(--font-mono);
  font-size: 2rem;
  font-weight: 600;
  letter-spacing: -0.02em;
  margin-bottom: 0.25rem;
}

.hero .title {
  font-size: 1.125rem;
  color: var(--color-muted);
  margin-bottom: 0.75rem;
}

.hero .tagline {
  font-size: 1rem;
  max-width: 480px;
}
```

- [ ] **Step 3: Verify in browser**

Expected: Name appears in monospace, "DevOps Engineer" in muted grey below it, tagline in normal weight underneath. Generous whitespace around the section.

- [ ] **Step 4: Commit**

```bash
git add index.html style.css
git commit -m "feat: add hero section"
```

---

### Task 3: About section

**Files:**
- Modify: `index.html` (add about section after hero)
- No new CSS needed — base `section` and `h2` styles apply

- [ ] **Step 1: Add about HTML after the closing `</section>` of hero**

```html
<section class="about">
  <h2>About</h2>
  <p>I'm a DevOps engineer focused on infrastructure as code, container orchestration, and cloud platform engineering. I design and maintain scalable systems on AWS and GCP using Terraform and Kubernetes. I care about automation, reliability, and keeping infrastructure as maintainable as the applications it runs.</p>
</section>
```

- [ ] **Step 2: Verify in browser**

Expected: "ABOUT" label in small caps grey, paragraph text below it in normal weight. Clear visual separation from hero via margin.

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "feat: add about section"
```

---

### Task 4: Skills section

**Files:**
- Modify: `index.html` (add skills section after about)
- Modify: `style.css` (add tag styles)

- [ ] **Step 1: Add skills HTML after the closing `</section>` of about**

```html
<section class="skills">
  <h2>Skills</h2>
  <ul class="tags">
    <li>Terraform</li>
    <li>Kubernetes</li>
    <li>AWS</li>
    <li>GCP</li>
    <li>Docker</li>
    <li>Helm</li>
    <li>ArgoCD</li>
    <li>CI/CD</li>
    <li>IaC</li>
    <li>Linux</li>
  </ul>
</section>
```

- [ ] **Step 2: Add tag styles to `style.css`**

```css
.tags {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tags li {
  font-family: var(--font-mono);
  font-size: 0.8125rem;
  padding: 0.25rem 0.625rem;
  border: 1px solid var(--color-border);
  border-radius: 3px;
}
```

- [ ] **Step 3: Verify in browser**

Expected: Tags appear as small monospace-font pills with a light border, wrapping naturally when they fill the line.

- [ ] **Step 4: Commit**

```bash
git add index.html style.css
git commit -m "feat: add skills section"
```

---

### Task 5: Links section

**Files:**
- Modify: `index.html` (add links section after skills)
- Modify: `style.css` (add link styles)

- [ ] **Step 1: Add links HTML after the closing `</section>` of skills**

Update the three href values with your actual URLs before committing:
- `https://github.com/vojneski` — update if your GitHub username differs
- `https://linkedin.com/in/vojneski` — update with your LinkedIn profile slug
- `mailto:` — update with your preferred contact email

```html
<section class="links">
  <h2>Links</h2>
  <nav aria-label="Social links">
    <a href="https://github.com/vojneski">GitHub</a>
    <a href="https://linkedin.com/in/vladimir-vojneski-sysadmin">LinkedIn</a>
    <a href="mailto:vladimir@vojneski.dev">Email</a>
  </nav>
</section>
```

- [ ] **Step 2: Add link styles to `style.css`**

```css
.links nav {
  display: flex;
  gap: 1.5rem;
}

.links a {
  color: var(--color-text);
  text-decoration: none;
  font-size: 0.9375rem;
  border-bottom: 1px solid var(--color-border);
  padding-bottom: 1px;
  transition: border-color 0.15s;
}

.links a:hover {
  border-color: var(--color-text);
}
```

- [ ] **Step 3: Verify in browser**

Expected: Three links in a row, dark text, subtle underline that darkens on hover. Click each link — GitHub and LinkedIn should open correct profiles in a new context; email should open your mail client.

- [ ] **Step 4: Commit**

```bash
git add index.html style.css
git commit -m "feat: add links section"
```

---

### Task 6: Responsive styles

**Files:**
- Modify: `style.css` (add mobile breakpoint at end of file)

- [ ] **Step 1: Add responsive styles at the end of `style.css`**

```css
@media (max-width: 600px) {
  main {
    padding: 2.5rem 1.25rem;
  }

  h1 {
    font-size: 1.5rem;
  }

  .links nav {
    flex-direction: column;
    gap: 0.875rem;
  }
}
```

- [ ] **Step 2: Verify on mobile viewport**

In Chrome/Firefox DevTools, toggle the device toolbar (F12 → Ctrl+Shift+M) and set width to 375px.

Expected: Page uses tighter padding, name is slightly smaller, links stack vertically.

- [ ] **Step 3: Commit**

```bash
git add style.css
git commit -m "feat: add responsive styles for mobile"
```

---

### Task 7: CNAME file and GitHub Pages setup

**Files:**
- Create: `CNAME`

- [ ] **Step 1: Create `CNAME` file in repo root**

```
vojneski.dev
```

The file must contain only the bare domain — no `https://`, no trailing slash.

- [ ] **Step 2: Commit**

```bash
git add CNAME
git commit -m "feat: add CNAME for custom domain"
```

- [ ] **Step 3: Enable GitHub Pages in repository settings**

1. Go to `https://github.com/<your-username>/vojneski.dev/settings/pages`
2. Under **Source**, select `Deploy from a branch`
3. Set branch to `main`, folder to `/ (root)`
4. Click **Save**
5. GitHub will show the published URL — it should pick up the `CNAME` and resolve to `vojneski.dev`

- [ ] **Step 4: Configure DNS at your domain registrar**

Add these DNS records at your registrar (exact steps depend on your provider):

```
Type    Name    Value
A       @       185.199.108.153
A       @       185.199.109.153
A       @       185.199.110.153
A       @       185.199.111.153
CNAME   www     vojneski.dev.
```

These are GitHub Pages' current IP addresses (correct as of 2026).

- [ ] **Step 5: Verify deployment**

After DNS propagates (up to 24h, usually faster):

```bash
curl -I https://vojneski.dev
# Expected: HTTP/2 200
```

Also visit `https://vojneski.dev` in a browser and confirm all four sections render correctly.

- [ ] **Step 6: Push to remote**

```bash
git push origin main
```
