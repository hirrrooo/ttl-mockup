# Take The Lead - Brand Guidelines

This project is a static SvelteKit single-page application built to showcase the brand identity and UI components for **Take The Lead**, a mockup pet fundraising platform. 

It is designed with a responsive, modern "stacked vertical flow" layout and includes print optimizations to naturally support high-fidelity PDF exports via native browser printing.

## Overview

The brand board includes:
- **Core Identity**: Custom "Earthy" color palette (Tailwind configured) and Typography scales using Google Fonts (Quicksand, Roboto Slab, Roboto Mono).
- **UI Components**: Reusable `Button`, `Input`, `Slider`, `Card`, and `MockNavbar` components.
- **Donation Form**: A sample interactive fundraising component showcasing Svelte 5 `$state` and `$bindable` runes.

## Development

To start a local development server:

```bash
npm install
npm run dev
```

## Deployment (GitHub Pages)

This project is configured to automatically deploy to GitHub Pages using **GitHub Actions**.

Whenever you push to the `main` branch, the `.github/workflows/deploy.yml` workflow will automatically:
1. Build the application using `@sveltejs/adapter-static`.
2. Map the base paths correctly.
3. Deploy the resulting static files to the `gh-pages` environment.

*Note: Ensure that GitHub Pages is enabled in your repository settings and set to source from "GitHub Actions".*