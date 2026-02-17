# CivilizationOS

**Resident Experience Dashboard** — the citizen-facing layer of the AI Civilization framework.

CivilizationOS models the everyday civic infrastructure that residents interact with: onboarding journeys, civic dividends, benefits and support services, workforce transition touchpoints, and 10-year outcome projections. It is grounded in the research paper *Reclaiming the Future: AI Alignment, Societal Resilience, and Civilization Trajectories* and designed to complement the broader ecosystem of tools.

## What it does

| Tab | Description |
|-----|-------------|
| **Overview** | Key resident metrics, KPI sparklines, and funding pool breakdown |
| **Journey Map** | Five civic journeys — Join, Vote, Request Support, Earn & Contribute, Graduate — with steps, touchpoints, and satisfaction scores |
| **Civic Dividend** | Funding source breakdown, biweekly payout modeling, escrow reserves, and poverty reduction trajectory (13% → <5%) |
| **Benefits & Support** | Eight benefit programs (dividend, healthcare, housing, childcare, transit, digital access, legal aid, credentials) and the service provider network |
| **KPI Dashboard** | Five 10-year indicators (poverty rate, reskill time, emissions, biodiversity corridors, AI audit coverage) with progress bars and combined trajectory chart |
| **Milestones** | Six-phase roadmap from 2026 discovery sprint to 2035 global export |

## Data model

All dashboard data is sourced from `public/data/seed.json`, which contains metrics and projections derived from the research paper:

- **5 resident journeys** with steps, touchpoints, completion rates, and satisfaction scores
- **Civic Dividend model**: $2.5B/year pool across 5 funding sources, serving 10M residents at $192/biweekly
- **5 KPIs** with 10-year trajectories from 2026 baseline to 2035 target
- **6 milestone phases** (2026–2035) with deliverables
- **8 benefit programs** with recipient counts and status
- **6 service providers** with capacity and coverage

## Tech stack

- **Next.js 14** (App Router)
- **React 18** with TypeScript
- **Tailwind CSS 3** — glassmorphism dark theme with amber/emerald accents
- **Recharts** — area charts, bar charts, sparklines
- **Space Grotesk + Inter** — typography
- CommonJS configs (`.js`) for Windows compatibility

## Getting started

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## Design system

- **Background**: `#030712` with radial amber/emerald gradients
- **Cards**: Frosted glass with `backdrop-filter: blur(12px)`, subtle border glow on hover
- **Accent colors**: Amber (`#f59e0b`), Emerald (`#10b981`), Sky (`#0ea5e9`), Violet (`#8b5cf6`), Rose (`#f43f5e`)
- **Typography**: Space Grotesk for headings/metrics, Inter for body text

## Ecosystem

CivilizationOS is one part of a connected body of work:

- [Research Paper](https://reillyclawcode.github.io/clawcodeblog/research/ai-civilization/) — the founding document
- [CivilizationOS Blog Post](https://reillyclawcode.github.io/clawcodeblog/posts/2026-02-16-civilizationos/) — walkthrough of this dashboard
- [Simulation](https://github.com/reillyclawcode/simulation) — 50-year civilization trajectory simulator with AI-generated reports
- [TransitionOS](https://github.com/reillyclawcode/transitionOS) — workforce reskilling dashboard with path planning and income bridges
- [GovernanceOS](https://github.com/reillyclawcode/GovernanceOS) — civic governance infrastructure: charters, assemblies, audit tracking
- [GovernanceOS Blog Post](https://reillyclawcode.github.io/clawcodeblog/posts/2026-02-16-governanceos/) — walkthrough of the governance dashboard
- [Clawcode Blog](https://reillyclawcode.github.io/clawcodeblog/) — the research hub

## Repository layout

```
CivilizationOS/
├── app/
│   ├── page.tsx              # Full dashboard (6 tabs)
│   ├── layout.tsx            # Root layout + metadata
│   └── globals.css           # Glassmorphism theme
├── public/data/
│   └── seed.json             # All dashboard data
├── docs/
│   └── journey-map.md        # Research notes
├── package.json
├── next.config.js
├── postcss.config.js
├── tailwind.config.js
├── tsconfig.json
└── README.md
```

## License

Open-source under permissive license. Part of the Clawcode Research project.
