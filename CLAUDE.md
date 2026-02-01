# LeftClick Agency Website

## Project Overview

Premium marketing website for LeftClick, an AI automation agency targeting B2B companies. Static HTML files (~50-60KB each) with embedded CSS and JavaScript.

## Live URLs

- **Production**: https://leftclick-agency.netlify.app
- **Custom Domain**: go1secondcopy.com (pending/live)
- **Netlify Admin**: https://app.netlify.com/projects/leftclick-agency

## Tech Stack

- **Framework**: Static HTML (no build step)
- **Styling**: Embedded CSS
- **JavaScript**: Vanilla JS, embedded
- **Hosting**: Netlify
- **Fonts**: Inter (Google Fonts CDN)

## Design System

### Colors
| Token | Hex | Usage |
|-------|-----|-------|
| Black base | `#000000` | Background |
| Dark gray | `#0a0a0a`, `#111111` | Cards, sections |
| Emerald primary | `#10b981` | Accents, CTAs |
| Emerald light | `#34d399` | Hover states |
| Emerald dark | `#059669` | Active states |

### Typography
- **Font**: Inter
- **Weights**: 300 (light), 400 (regular), 500 (medium), 600 (semibold), 700 (bold), 800 (extrabold)
- **Letter spacing**: -0.03em (tight)

### Corner Radii
Squared/luxe aesthetic — avoid rounded pills:
- Small: `4px`
- Medium: `6px`
- Large: `8px`

### Logo
Plain text wordmark: "LeftClick" where "Click" is rendered in emerald green (`#10b981`).

## Page Sections

### Homepage (index.html)
1. **Hero** — Parallax floating tech icons, gradient orbs, headline + primary CTA
2. **Social Proof** — Infinite scrolling logo carousel (Make, n8n, Zapier, HubSpot, Airtable, etc.)
3. **Case Studies** — 3 cards with animated number counters showing client results
4. **How It Works** — 3-phase process (Growth Mapping → Scope → Delivery)
5. **Services** — 6-card grid of service offerings
6. **CTA** — Final call-to-action linking to Calendly

### About Page (about.html)
1. **Hero** — Company origin story headline with gradient orbs
2. **Story Section** — Company history and early AI adoption narrative
3. **Founders Section** — Profiles for Nick Saraev (CEO) and Noah Edis (COO)
4. **Timeline Section** — Key milestones from 2020-2025
5. **Values Section** — 6-card grid of company principles
6. **Press Section** — Featured media logos (Popular Mechanics, Apple News, Bloomberg, Indie Hackers)
7. **CTA** — Call-to-action linking to Calendly

## Interactive Features

- Scroll-triggered reveal animations via Intersection Observer
- Animated counters with easeOutQuart easing
- Mouse-following cursor glow effect (desktop only)
- Scroll progress indicator in header
- Fully responsive down to mobile

## Deployment

### Deploy to Production
```bash
cd /Users/nicksaraev/leftclick-agency && netlify deploy --prod
```

### Preview Deploy
```bash
cd /Users/nicksaraev/leftclick-agency && netlify deploy
```

### Requirements
- Netlify CLI installed (`npm install -g netlify-cli`)
- Authenticated with Netlify (`netlify login`)

## File Structure

```
/Users/nicksaraev/leftclick-agency/
├── index.html          # Homepage (all HTML, CSS, JS embedded)
├── about.html          # About page (founders, story, values)
├── netlify.toml        # Netlify configuration
├── .gitignore          # Git ignore rules
├── CLAUDE.md           # This file
└── .netlify/           # Netlify local state (gitignored)
```

## External Dependencies

- **Calendly**: Meeting booking at `calendly.com/leftclick-meeting-30`
- **Google Fonts**: Inter font family via CDN
- **No npm packages** — Zero build dependencies

## Common Tasks

### Update Content
Edit `index.html` directly. All content, styles, and scripts are in this single file.

### Change Colors
Search for hex codes in `index.html`:
- Primary green: `#10b981`
- Light green: `#34d399`
- Dark green: `#059669`

### Update Calendly Link
Search for `calendly.com/leftclick-meeting-30` and replace.

### Add/Remove Social Proof Logos
Find the `.logo-track` div in the social proof section. Logos are inline SVGs.

## Notes

- Keep the single-file architecture — no bundlers or build steps
- Maintain the squared corner aesthetic (no pills)
- Test scroll animations after content changes
- Counter animations trigger on scroll into view
