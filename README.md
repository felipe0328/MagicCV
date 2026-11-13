# Personal Engineering Portfolio

Single-page personal landing page for **Felipe Puentes** — a Senior Backend / Software Engineer. The repository may be named MagicCV; the site itself is a personal introduction, not a product brand.

## Goals

1. Make a strong first impression.
2. Communicate who I am and what I do.
3. Show attention to detail and solid engineering practices.
4. Keep the experience memorable, fast, and easy to maintain.
5. Make contact simple (`mailto:` and professional links only — no contact API).

## Stack

| Concern | Technology |
| --- | --- |
| UI | React |
| Language | TypeScript |
| Build | Vite |
| Styling | Plain CSS or CSS Modules |
| Animation | GSAP + ScrollTrigger + `@gsap/react` |
| Content | Centralized TypeScript data |
| Deploy | Static hosting (chosen later) |

### Hard non-goals

Do not introduce: backend services, databases, auth, APIs/CMS, Next.js or Astro, Redux or other global state libraries, React Router, large UI kits, Tailwind, or unnecessary dependencies.

## Site structure

One landing page with four sections:

1. **Hero** — introduction and strongest visual moment
2. **About** — background and engineering philosophy
3. **Expertise** — principal capabilities (not a logo grid)
4. **Contact** — short invitation and links

## Content model

All personal and professional copy lives in one file:

`src/data/profile.ts`

Components consume that data. Do not invent employment history, accomplishments, metrics, contact details, or URLs. Use clear placeholders in `profile.ts` for anything not yet provided.

## Visual direction

Editorial **light / ink-on-paper** aesthetic: large expressive typography, strong negative space, one restrained cool accent, quiet systems motifs. Prefer three well-executed interactions over many mediocre animations. Motion quality may take inspiration from high-end product storytelling; branding and layout should remain original.

## Development approach

Vertical slices per section: content → composition → static layout → motion → browser check → refine → next section.

### Milestones

1. **Foundation** — Vite + React + TS, design tokens, `profile.ts`, motion storyboard, lint/typecheck/build
2. **Hero** — polished intro experience
3. **Storytelling** — About + Expertise
4. **Contact and navigation**
5. **Production** — a11y, performance, SEO, static deploy prep

Design notes (when added): [`design/motion-storyboard.md`](design/motion-storyboard.md)

## Agent guidance

Project conventions for Cursor and other agents: [`AGENTS.md`](AGENTS.md) and [`.cursor/rules/portfolio-brief.mdc`](.cursor/rules/portfolio-brief.mdc).

## Run locally

Once the Vite app is scaffolded:

```bash
npm install
npm run dev
```

Typical checks:

```bash
npm run build
npm run lint
npx tsc --noEmit
```

Exact script names may follow `package.json` after scaffold. The app is not initialized yet — Milestone 1 adds the toolchain.
