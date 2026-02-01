# LeftClick Services Page

## Project Overview

Comprehensive services page for LeftClick, an AI automation agency. This is a dedicated services landing page that provides detailed breakdowns of all service offerings. Single HTML file with embedded CSS and JavaScript.

## Related Sites

- **Main Landing Page**: leftclick-agency (https://leftclick-agency.netlify.app)
- **LeftClick.ai**: https://www.leftclick.ai

## Tech Stack

- **Framework**: Static HTML (no build step)
- **Styling**: Embedded CSS
- **JavaScript**: Vanilla JS, embedded
- **Hosting**: Netlify (recommended)
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
- **Weights**: 300-800
- **Letter spacing**: -0.03em (tight)

### Corner Radii
Squared/luxe aesthetic — avoid rounded pills:
- Small: `4px`
- Medium: `6px`
- Large: `8px`

### Logo
Plain text wordmark: "LeftClick" where "Click" is rendered in emerald green (`#10b981`).

## Page Structure

### index.html (Services)

1. **Hero** — Stats-focused hero with key metrics (50+ systems, $12M+ revenue, etc.)
2. **Lead Generation Systems** — AI Cold Email, Application Systems, Content Systems
3. **Project Management Systems** — Automated Fulfillment, Onboarding, PM Workflows
4. **Hiring Systems** — Intake Systems, AI Scoring, Trial Processes
5. **Sales Administration** — Custom CRMs, AI Asset Generators, Nurture Systems
6. **Who It's For** — Target personas (Agencies, SaaS, Professional Services, E-Commerce)
7. **Results/Testimonials** — Client success stories (1SecondCopy, AlterCall, Dad's Printing, XWECAN)
8. **Process** — 4-step timeline (Discovery, Design, Build, Launch)
9. **Pricing** — Three tiers (Single System, Growth Package, Retainer)
10. **CTA** — Final call-to-action

### Service Categories

| Category | Sub-Services |
|----------|--------------|
| Lead Generation | AI Cold Email Systems, Application Systems, Content Systems |
| Project Management | Automated Fulfillment, Onboarding Systems, PM Workflows |
| Hiring | Intake Systems, AI Scoring, Trial Processes |
| Sales Administration | Custom CRMs, AI Asset Generators, Nurture Systems |

### about.html (About)
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
- Smooth scroll navigation
- Fully responsive down to mobile

## Deployment

### Deploy to Production (if Netlify configured)
```bash
cd /Users/nicksaraev/leftclick-services && netlify deploy --prod
```

### Preview Deploy
```bash
cd /Users/nicksaraev/leftclick-services && netlify deploy
```

### Requirements
- Netlify CLI installed (`npm install -g netlify-cli`)
- Authenticated with Netlify (`netlify login`)

## File Structure

```
/Users/nicksaraev/leftclick-services/
├── index.html          # Main services page (all HTML, CSS, JS embedded)
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

### Update Pricing
Find the `.pricing-section` in index.html. Each tier has:
- `.pricing-name` — tier name
- `.pricing-amount` — price
- `.pricing-features` — feature list

### Add/Remove Services
Each service category has a `.services-detail-grid` containing `.service-detail-card` elements.

## Notes

- Keep the single-file architecture — no bundlers or build steps
- Maintain the squared corner aesthetic (no pills)
- Test scroll animations after content changes
- Counter animations trigger on scroll into view
- Page is designed to work as standalone services page or linked from main site
