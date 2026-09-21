# CookCloud Landing Page

Single-file static landing page for CookCloud (the meal-planning SaaS that's currently offline). No build step — `index.html` is the whole site.

## What's on the page

- Hero with the YouTube demo embed
- Full shipped-feature list (vs. roadmap items that never got built)
- The real tech stack (Django, Postgres, Redis, Celery, Channels, Stripe, OpenAI, Spoonacular, AbacusAI) — goes deeper than the [original launch article](https://bryanheadrick.com/ai-powered-culinary-alchemy-transmuting-recipe-torment-into-cookcloud-magic/), which only covered the AI coding tools used to build it
- An honest breakdown of why it got shut down (revenue never got off the ground — a demand and prioritization problem, not a technical one)
- An EmailOctopus signup for anyone who wants to know if/when it relaunches
- Hosted at [cookcloud.me](https://cookcloud.me)

## Deploy

Any static host works — no build step, no dependencies. Options:

- **Cloudflare Pages / Netlify / Vercel**: point at this repo, no build command, publish directory `/`
- **GitHub Pages**: enable Pages on this repo, serve from `main` branch root

## Analytics

Uses [GoatCounter](https://www.goatcounter.com) (free, cookieless, no consent banner required) — the script tag is right before `</body>`. Sign up for a site code and replace `YOUR-CODE` in the `data-goatcounter` URL before deploying, or the beacon just won't record anything.

## Editing

It's one HTML file with inlined CSS. Sections are marked with comments (`<!-- ---------- Nav ---------- -->` style) inside the `<style>` block matching the section IDs in the markup (`#features`, `#stack`, `#closed`, `#reopen`).
