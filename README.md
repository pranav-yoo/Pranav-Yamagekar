# Pranav Yamagekar — Portfolio

A personal portfolio with an interactive 3D room, scroll-driven animations, and light and dark themes. The page introduces Pranav, shares career highlights and achievements, and provides contact links and a link to the blog at [pranavyamagekar.in](https://pranavyamagekar.in).

## Tech stack

| Technology | Purpose |
| --- | --- |
| HTML5 and CSS3 | Page content, responsive layout, and theme styling |
| JavaScript (ES modules) | Application logic and interactions |
| Three.js | WebGL rendering, cameras, lighting, and 3D models |
| GSAP and ScrollTrigger | Scroll-driven scene transitions and animations |
| ASScroll | Smooth scrolling integrated with ScrollTrigger |
| Vite | Local development server and production builds |
| Node.js 24 and npm | Build tooling and dependency management |
| GLB models and Draco | 3D assets and model compression support |

This is a browser-based portfolio; it does not include a backend service.

## Page content

- **About Me:** Personal introduction in Pranav's own words.
- **Highlights:** Software engineering at ICICI Lombard in Mumbai (August 2025–present), World Robot Olympiad participation, and a National Science Exhibition achievement.
- **Contact Me:** Blog, Instagram, X, LinkedIn, email, and WhatsApp information.

## Run locally

Install [Node.js 24](https://nodejs.org/) and npm. If you use nvm, the included `.nvmrc` selects Node.js 24:

```sh
git clone https://github.com/pranav-yoo/Pranav-Yamagekar.git
cd Pranav-Yamagekar
nvm install
nvm use
npm ci
npm run dev
```

If you installed Node.js directly, skip the two `nvm` commands. Open the URL printed by Vite, usually `http://localhost:5173`. Press `Ctrl+C` to stop the server.

## Build and preview

```sh
npm run build
npm run preview
```

The production files are generated in `dist/`. The preview command serves that build locally.

## Deploy on Vercel

Import the GitHub repository and use these settings:

| Setting | Value |
| --- | --- |
| Framework preset | Vite |
| Node.js version | 24.x |
| Install command | `npm ci` |
| Build command | `npm run build` |
| Output directory | `dist` |

For an existing project reporting an unsupported `16.x` version, open **Project Settings → Build and Deployment → Node.js Version**, select **24.x**, and redeploy. The `engines.node` field in `package.json` also pins deployment builds to `24.x`. See [Vercel's Node.js version documentation](https://vercel.com/docs/functions/runtimes/node-js/node-js-versions).

## Project structure

```text
index.html           Portfolio content
style.css            Layout, themes, and responsive styles
main.js              Application entry point
Experience/          3D scene, camera, renderer, theme, and loading logic
  Utils/             Asset definitions, loading, viewport sizes, and timing
  World/             Scene objects and scroll controls
public/models/       GLB room models
public/textures/     Video textures
public/draco/        Draco decoder assets
```

Update text and contact links in `index.html`, visual styles in `style.css`, and loaded model/video paths in `Experience/Utils/assets.js`.
