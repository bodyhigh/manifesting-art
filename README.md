
# Manifesting.Art – Web Application

> **Mobile-first, artist-friendly business management.**
>  
> This is the **Angular web front-end** for **Manifesting.Art**, an *Art Business Operating System* designed to empower artist-entrepreneurs with the tools they need to manage their work, exhibitions, consignments, and sales — anywhere, on any device.

---

## 🌟 Overview

Manifesting.Art is built for the realities of the modern artist:
- **On-the-go workflow** – Full mobile feature parity, optimized for fairs, exhibitions, and studio visits.
- **Creative control** – Customizable layouts, typography, colors, and public viewing rooms to match your brand.
- **Business clarity** – Integrated financial tools: COGS tracking, materials & framing costs, commission tracking.
- **Performance** – Fast, responsive UI with modern loading states and offline-friendly design.

This `web` app is the primary interface for artists, collectors, and galleries to interact with the Manifesting.Art platform.

---

## 🚀 MVP Features

- **Mobile-first** Angular UI with Material Design + Tailwind styling
- **Inventory & artwork management** with bulk editing and spreadsheet-style views
- **Exhibition & consignment tracking** with smart reminders
- **Integrated financials** for real-time profitability insights
- **Public outputs** – branded PDFs, viewing rooms, shareable pages
- **Secure API integration** with the `api` (Fastify) service

---

## 🛠 Tech Stack

- **Framework**: [Angular](https://angular.io/) + [Nx](https://nx.dev/) workspace
- **UI**: Angular Material + Tailwind CSS
- **Testing**: Jest (unit tests), no e2e configured yet
- **Bundler**: _(to be decided – esbuild/rspack/webpack)_
- **API**: Fastify backend (`apps/api`)

---

## 📦 Setup

### 1. Install Angular plugin (if not already installed)
```bash
npm i -D @nx/angular@latest
````

### 2. Generate the `web` app

```bash
npx nx g @nx/angular:application web \
  --style=scss \
  --routing \
  --e2eTestRunner=none \
  --unitTestRunner=jest \
  --directory=apps
```

### 3. (Optional) Add Tailwind + Angular Material

```bash
npx nx g @nx/angular:setup-tailwind --project=web
npx nx g @angular/material:ng-add --project=web --theme=custom --typography --animations
```

### 4. Run the app

```bash
npx nx serve web
# Open http://localhost:4200
```

---

## 🤝 Contribution Guidelines

* Follow the [Material Design](https://material.io/) principles with a **calm, creative, and professional** aesthetic.
* Use **semantic class names** and keep styling in SCSS, applying utility classes with `@apply` when using Tailwind.
* Align all UI components with **mobile-first** principles.
* Document all new components and services in the `/docs` folder.

---

## 🗺 Roadmap

**MVP (Sprint 0-1)**

* Scaffold Angular + Fastify apps in Nx workspace
* Implement core navigation, layout, and authentication UI
* Connect `/api` services for artwork and exhibition data

**Post-MVP**

* Advanced financial dashboard
* Offline-capable mobile features
* Multi-currency support
* AI-assisted Exhibition Application Assistant
* Public portfolio + e-commerce integrations

---

© 2025 Manifesting.Art. All rights reserved.
