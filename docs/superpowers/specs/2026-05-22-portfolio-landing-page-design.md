# vojneski.dev — Personal Portfolio Landing Page

**Date:** 2026-05-22
**Status:** Approved

## Overview

A single-page personal portfolio and landing page for Vladimir Vojneski, a DevOps Engineer. Hosted on GitHub Pages via the `main` branch root. No build step, no dependencies — plain HTML and CSS only.

## Goals

- Present Vladimir as a DevOps engineer specializing in IaC, Terraform, Kubernetes, AWS, and GCP
- Provide a minimal, clean, professional first impression
- Link to professional profiles (GitHub, LinkedIn, email)

## Non-Goals

- Blog or CMS functionality
- Contact form
- JavaScript interactivity
- Multiple pages

## Page Structure

Single vertical scroll with four sections:

### 1. Hero
- Full name: Vladimir Vojneski
- Title: DevOps Engineer
- One-line tagline summarizing focus (e.g., "Building reliable infrastructure with Terraform, Kubernetes, and cloud-native tools.")

### 2. About
- 2–3 sentences on background, experience focus, and approach
- Written in first person

### 3. Skills
- Tag/badge list of core technologies: Terraform, Kubernetes, AWS, GCP, IaC, CI/CD, Docker, Linux
- No ratings or progress bars — just clean labels

### 4. Links
- GitHub
- LinkedIn
- Email
- Icon + text or icon-only with accessible labels

## Visual Style

- Background: white (`#ffffff`)
- Text: dark (`#111111` or `#1a1a1a`)
- Accent: monospace font for name or skill tags (e.g., `JetBrains Mono`, `Fira Code`, or system monospace fallback)
- Generous whitespace, no images
- Responsive: readable on mobile and desktop without a CSS framework

## File Structure

```
index.html
style.css
```

## Deployment

GitHub Pages serves `index.html` from the root of the `main` branch. Enable via repository Settings → Pages → Source: `main` / `root`. Custom domain `vojneski.dev` configured via a `CNAME` file in the repo root.

## Success Criteria

- Page loads at `vojneski.dev` with correct content
- All four sections visible on scroll
- Links to GitHub, LinkedIn, and email work
- Page is readable on mobile and desktop
