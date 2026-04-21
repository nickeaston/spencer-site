# Spencer — Landing Site

**Live:** `https://nickeaston.github.io/spencer-site/` (pre-domain)
**Future:** `https://usespencer.com` once DNS is wired to GitHub Pages.

## What this is

A single-page site for **Spencer** — Easton Enterprises' AI-operations consulting service, positioned as *Spencer as a Service*. Purpose: inbound-lead capture via 30-min discovery calls.

## Structure

One file (`index.html`). Vanilla HTML + CSS. No framework, no build step, no JS dependencies. Sections:

1. **Hero** with eyebrow ("Spencer as a Service"), H1, CTA, meta stats
2. **Live Ops Ticker** — terminal-style widget showing today's Spencer job schedule (currently static; Phase 1.5 wires it to live data from the Mac mini)
3. **What Spencer Does** — three audience tracks (Personal / Financial / Business)
4. **Callout** — "what you saw is running right now, for us"
5. **How It Works** — 4 steps (Discovery / Plan / Build / Run)
6. **Proof** — public links + referenced private samples (dashboard, morning brief, edge bet, investment scan)
7. **Pricing** — Project / Integration / Executive tiers from the locked framework doc
8. **Book** — Cal.com embed slot (placeholder until account wired)
9. **Footer** — minimal legal (only mention of Easton Enterprises, in small type)

## To finish Phase 1 — 3 things outside this repo

### 1. Domain (your job)

- Register `usespencer.com` + `usespencer.ai` (Namecheap / Cloudflare ~$25-30 AUD/yr total)
- Once registered, tell Stu → I'll wire the custom domain into GitHub Pages (5 min config change: adds a `CNAME` file here + you add A records at the registrar)

### 2. Cal.com account (your job)

- Go to **cal.com**, sign up with your soon-to-exist business Gmail
- Create an event type: **"Discovery Call"** — 30 min, business hours, 15-min buffers either side
- Connect your Google Calendar
- Copy your booking URL (looks like `cal.com/your-handle/discovery-call`)
- Send the URL to Stu → I swap the placeholder in `index.html` for the iframe embed (2-min change)

### 3. Business email (your job, eventual)

- Set up Google Workspace under Easton Enterprises → create `hello@usespencer.com` (or similar)
- Forward to your personal until volume warrants a separate inbox
- Update the email link in index.html footer + the booking fallback text

## Phase 1.5 (after domain + Cal.com live)

- Live ops-ticker widget — auto-generated from Mac mini cron logs, pushed daily as JSON to this repo, fetched on page load via vanilla JS
- Custom OG image for social sharing
- robots.txt + sitemap for indexing
- Plausible Analytics (or similar privacy-first) for traffic visibility

## Phase 2 (later)

- Audience-track sub-pages (`/for-personal`, `/for-founders`, `/for-business`) with deeper use-case content
- Case study page for Easton Enterprises — screenshots + walkthrough of each system
- Hero video loop (45-sec muted auto-play showing morning brief + dashboards in motion)
- Written client testimonials once first engagements ship

## Deploying changes

```bash
git add -A
git commit -m "Update: <what changed>"
git push
```

GitHub Pages rebuilds on each push to `main`. Usually live within 30-60 sec.

## Design system

- **Fonts:** Inter (body), Playfair Display (display italics), JetBrains Mono (terminal panel)
- **Palette:** Cream backgrounds (`#BFB09A` / `#B3A38C`), ink text (`#1A1814`), gold accent (`#7A5C2E`), terminal panel green-on-black for the ops widget
- **Typography:** Generous sizing, italic display headlines, uppercase micro-labels with 0.16em letter-spacing

All styles are inline in `index.html` for simplicity. If the stylesheet grows beyond ~800 lines we'll extract to `styles.css`.
