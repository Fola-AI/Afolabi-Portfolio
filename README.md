# Afolabi Ajao — Portfolio

Personal portfolio site for **Afolabi Ajao**, a Copilot Studio, Power Platform and AI Engineer who builds AI copilots and automations that reach production.

The site is a single, self-contained `index.html`: no build step, no dependencies, no framework. The headshot is embedded directly in the file as a base64 image, so the whole portfolio is one file you can host anywhere.

> **Live site:** https://afolabi-portfolio.vercel.app  <!-- update this to your real Vercel URL once deployed -->

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/Fola-AI/Afolabi-Portfolio)

---

## What it is

A one-page portfolio tuned for Microsoft Copilot Studio and Power Platform roles. It leads with a solution-orchestration schematic (Copilot Studio into Power Automate, Dataverse, SharePoint and 365, and Azure AI), then backs it with real, shipped products and enterprise delivery experience.

Sections:

- **Hero** — positioning, availability, key stats, and a profile card with the orchestration schematic.
- **What I deliver** — capability cards mapped to the Microsoft stack, plus a code-first agent stack (OpenAI Agents SDK, CrewAI, LangGraph, AutoGen, MCP).
- **Selected work** — case studies (McLaren aftersales automation, Bellbite, FarmEyes, KudiLoop) plus KudifyNG and FleetIO.
- **Track record** — an experience timeline.
- **Credentials** — certifications and education.
- **Contact** — email, LinkedIn, GitHub, Hugging Face.

---

## Tech

- Plain **HTML5**, **CSS3** (custom properties, grid, flexbox), and a small amount of vanilla **JavaScript** (scroll reveals, mobile nav, current year).
- Type: **Space Grotesk**, **IBM Plex Sans**, **IBM Plex Mono** (loaded from Google Fonts).
- No frameworks, no bundler, no `node_modules`.
- Accessibility: semantic landmarks, visible keyboard focus, and `prefers-reduced-motion` support.
- Responsive from desktop down to mobile.

---

## Project structure

```
Afolabi-Portfolio/
├── index.html    # the entire site (markup, styles, script, embedded headshot)
└── README.md
```

That is the whole project. Everything renders from `index.html`.

---

## Run it locally

No install needed. Either:

- Open `index.html` directly in a browser, or
- Serve it locally so fonts and links behave exactly as in production:

```bash
# Python
python3 -m http.server 8000

# or Node
npx serve .
```

Then visit `http://localhost:8000`.

---

## Deploy to Vercel

### Dashboard (easiest)

1. Sign in at [vercel.com](https://vercel.com) with GitHub.
2. **Add New → Project**, then **Import** `Fola-AI/Afolabi-Portfolio`.
3. Configure:
   - **Framework Preset:** Other
   - **Build Command:** leave empty
   - **Output Directory:** leave default (root)
   - **Root Directory:** `./`
4. **Deploy**. You get a live `*.vercel.app` URL in seconds.

Because the project is linked to GitHub, every push to `main` redeploys automatically.

### CLI

```bash
npm i -g vercel
vercel         # first deploy, links the project
vercel --prod  # promote to production
```

### Custom domain

Project → **Settings → Domains → Add**, then point your domain (for example `afolabiajao.com`) at it.

---

## Customizing the content

Everything is editable inline in `index.html`.

- **Text and links:** search for the section comments (`<!-- Work -->`, `<!-- Credentials -->`, and so on) and edit the copy or `href` values directly.
- **Headshot:** the photo is a base64 data URI on the `<img class="avatar-lg" ...>` tag. To swap it, replace the `src` value with a new `data:image/jpeg;base64,...` string, or point it at a hosted image URL.
- **Colours and fonts:** all design tokens live in the `:root` block at the top of the `<style>` (accent colours, background, type families).
- **Projects:** each case study is an `<article class="case">`; the two smaller items are `<div class="mini">`.

After any edit, commit and push. Vercel redeploys on its own.

---

## Featured links

- **Bellbite** — https://www.bellbite.app
- **FarmEyes (live demo)** — https://huggingface.co/spaces/Fola-AI/FarmEyes
- **KudiLoop** — [App Store](https://apps.apple.com/gb/app/kudiloop/id6756009015) · [Google Play](https://play.google.com/store/apps/details?id=com.kudiloop.app)
- **FleetIO (prototype)** — https://fleet-io.vercel.app

---

## Contact

- **Email:** afolinks@outlook.com
- **LinkedIn:** https://www.linkedin.com/in/afolabi-ajao-ab8442a7
- **GitHub:** https://github.com/Fola-AI
- **Hugging Face:** https://huggingface.co/Fola-AI

---

## License

© Afolabi Ajao. All rights reserved. The code is provided as a personal portfolio; feel free to take inspiration, but please do not reuse the personal content, branding, or headshot.
