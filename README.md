# Handshake Liquidity Solutions

Marketing website for **Handshake Liquidity Solutions Ltd** — the settlement and automation layer for global platforms.

Handshake Liquidity provides three things through a single API:

- **Programmatic ad automation** — algorithmically manage and optimize real-time ad spend, bid adjustments, and campaign budgets across advertising networks.
- **Localized payouts & settlement** — a high-throughput settlement engine that ingests bulk API instructions and instantly routes local-currency payouts to bank accounts and mobile-money wallets.
- **Back-office infrastructure** — secure, high-uptime cloud data-routing, API processing, and transaction logging for international enterprise platforms.

Built as a fast, framework-free static site with **Vite** and **Tailwind CSS v4**, using a component-based architecture (`<Component>` partials).

## Tech stack

- **Vite** — dev server and optimized production build
- **vite-plugin-html-inject** — `<Component src="...">` HTML partial injection
- **Tailwind CSS v4** — utility-first styling (`@tailwindcss/vite`)
- **Vanilla JavaScript** — GSAP, Lenis smooth scroll, marquee, accordion, modal, counters
- **Terser** — vendor-script minification (Vite plugin in `vite.config.js`)

## Pages

Home, About, Services, Service details, Blog, Blog details, Case studies, Case study details, Team, Team details, Pricing, Contact, Integration, Testimonials, Login, Sign up, 404 — 17 pages total.

## Project structure

```
handshake-liquidity/
├── public/                 # Static assets (images, fonts, vendor JS, favicons)
├── src/
│   ├── components/         # <Component> partials
│   │   ├── home/           # Home page sections (hero, solutions, track-record, …)
│   │   ├── shared/         # navbar, footer, cta, cards, buttons, icons, modal
│   │   ├── about/ services/ blog/ team/ pricing/ …
│   ├── js/                 # animation/ + utils/ (vanilla JS)
│   ├── styles/             # main.css + variable.css (@theme) + section styles
│   └── main.js             # JS entry
├── *.html                  # 17 root pages (build entries)
├── vite.config.js
├── post-build.js
└── package.json
```

## Prerequisites

- **Node.js** v18+ (developed on v24)
- **npm**

## Getting started

```bash
npm install      # install dependencies
npm run dev      # dev server at http://localhost:5173 (host 0.0.0.0)
npm run build    # production build to dist/ (runs post-build.js)
npm run preview  # preview the production build
npm run format   # Prettier
```

## Customization

- **Brand theme** — colors, fonts, and type scale live in `src/styles/variable.css` (`@theme`).
- **Logos & favicon** — `public/images/shared/` (wordmarks + mark) and `public/favicon.svg`.
- **Components** — pages compose partials from `src/components/`; add a root `*.html` file and it becomes a build entry automatically.

---

© Handshake Liquidity Solutions Ltd. All rights reserved.
