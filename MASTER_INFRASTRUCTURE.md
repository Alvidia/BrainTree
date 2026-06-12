# ARTYZ — MASTER DEVELOPMENT INFRASTRUCTURE

## Personal Software Ecosystem · Zero-Cost Expert Path

-----

## THE VISION

You are building a personal software ecosystem — not just one app.
Current projects:

- **Brain Universe** — knowledge operating system
- **Financial Tools** — personal finance / investment layer
- **Creative Management App** — creative workflow & asset management
- **Nexus** — the connecting concept (TBD, likely the meta-layer tying all apps together)

Every decision below is made with all four projects in mind.

-----

## COST REALITY

|Tool        |Cost          |Purpose                                |
|------------|--------------|---------------------------------------|
|GitHub      |Free          |All code, all projects, version history|
|StackBlitz  |Free          |In-browser IDE + live preview          |
|Claude.ai   |Already paying|Code generation, debugging, design     |
|Vercel      |Free tier     |Deploy apps as live URLs               |
|Safari (iOS)|Free          |Browser + PWA runner                   |
|Working Copy|$20 one-time  |Git on iPhone/iPad (buy when ready)    |

**Total to start: $0**
**Total when serious: $20 (Working Copy)**

-----

## GITHUB STRUCTURE

Create one GitHub account. Structure your repos like this:

```
github.com/artyz/
│
├── brain-universe/          ← Knowledge OS (active now)
├── financial-tools/         ← Financial layer (next)
├── creative-manager/        ← Creative workflow app
├── nexus/                   ← Meta-connector layer
└── shared-components/       ← Design system shared across all apps
```

**Why a shared-components repo matters:**
Your apps will share a visual language — dark space aesthetic, monospace type,
glow effects, color theming. Build those once. Import them everywhere.
This is how professional studios operate.

-----

## PROJECT ARCHITECTURE (each app)

Every project follows this structure:

```
project-name/
├── index.html               ← Entry point
├── vite.config.js           ← Build config
├── package.json             ← Dependencies
├── .gitignore
└── src/
    ├── main.jsx             ← React mount
    ├── App.jsx              ← Root component
    ├── components/          ← UI components
    ├── hooks/               ← Custom React hooks (physics, storage, etc.)
    ├── data/                ← Static databases, seed data
    ├── services/            ← localStorage, API calls, AI layer
    ├── utils/               ← Pure functions, formatters
    └── styles/              ← Global CSS, design tokens
```

This structure scales from a one-file prototype to a full production app
without ever needing to reorganize.

-----

## DAILY WORKFLOW (iPhone/iPad · Zero Install)

### The Loop

```
1. THINK     →  Claude.ai (Safari PWA)        — generate / fix / design
2. CODE      →  StackBlitz (Safari)           — edit, see live changes
3. SAVE      →  GitHub (StackBlitz built-in)  — commit from browser
4. DEPLOY    →  Vercel (auto from GitHub)      — live URL in 30 seconds
5. TEST      →  Safari on device              — open your Vercel URL
```

No Mac. No Xcode. No terminal. Fully on device.

-----

## SETUP SEQUENCE (do this once)

### Step 1 — GitHub Account

1. Go to github.com → Sign up (free)
1. Create repos: `brain-universe`, then others as you build them
1. Each repo: set to Public or Private (both free)

### Step 2 — StackBlitz

1. Go to stackblitz.com → Sign in with GitHub
1. Click “Connect Repository” → select `brain-universe`
1. StackBlitz clones it and gives you a live editor + preview
1. Every save auto-syncs to GitHub

### Step 3 — Import Brain Universe

In StackBlitz, your file structure is already ready (see files delivered).
StackBlitz will auto-run `npm install` and `npm run dev`.
The app appears in the right panel instantly.

### Step 4 — Vercel Deploy

1. Go to vercel.com → Sign in with GitHub (free)
1. “Import Project” → select your GitHub repo
1. Vercel detects Vite automatically, deploys in ~30 seconds
1. You get a URL like: `brain-universe.vercel.app`
1. Every GitHub push auto-redeploys. Zero effort.

### Step 5 — Safari PWA (iPhone/iPad)

Open your Vercel URL in Safari → Share button → “Add to Home Screen”
Now Brain Universe is an icon on your home screen, full screen, no browser chrome.
This works for ALL your apps.

-----

## WORKFLOW WITH CLAUDE (this conversation)

The most efficient way to work with me across all projects:

**When starting a session:**

> “We’re working on [Brain Universe / Financial Tools / etc].
> Current state: [paste relevant code or describe what’s built].
> Today’s goal: [specific feature].”

**When you want a new feature:**

> “Add [feature] to Brain Universe. Here’s the current BrainUniverse.jsx: [paste]”
> I return the full updated file. You paste it into StackBlitz. Done.

**When something breaks:**

> “This error: [paste error]. Relevant code: [paste component]”

**Keep your Master Project File updated** (like the one you already have).
Share it at the start of new conversations so I have full context instantly.

-----

## BRAIN UNIVERSE — IMMEDIATE NEXT STEPS

Priority order after this session:

1. **Import to StackBlitz** (today — use files delivered)
1. **Create GitHub repo** and connect
1. **Deploy to Vercel** → get your live URL
1. **Add to iPhone home screen** as PWA

Next features to build (in order):

- [ ] AI suggestion layer (Claude API inside the app — suggest connections)
- [ ] Infinite canvas (pan + zoom with d3-zoom or transform)
- [ ] Node clustering by world (visual grouping)
- [ ] Import/Export JSON (backup your universe)
- [ ] Mobile touch gestures (pinch zoom, tap-drag)

-----

## FINANCIAL TOOLS — ARCHITECTURE PREVIEW

When you’re ready to start this:

**What it likely needs:**

- Portfolio tracker (assets, allocation, P&L)
- Compound interest / scenario calculators
- Cash flow timeline visualization
- Net worth dashboard
- Connection to Brain Universe (cross-app node linking)

**Stack:** Same React/Vite. Add `recharts` for charts (already available in artifacts).
**Data:** localStorage first, then optionally a simple Supabase backend (free tier).

-----

## CREATIVE MANAGEMENT APP — ARCHITECTURE PREVIEW

**What it likely needs:**

- Project boards (not Trello-like, more spatial)
- Asset library (references, mood boards)
- Timeline / phases view
- Brief builder
- Connection to Brain Universe (ideas → projects)

**Stack:** Same React/Vite. Heavy on drag-and-drop (`@dnd-kit` — lightweight, excellent).

-----

## NEXUS — ARCHITECTURE PREVIEW

Nexus is likely the **meta-layer** that connects all your apps.
Think of it as a command center or hub:

```
Nexus
├── Open Brain Universe
├── Open Financial Tools
├── Open Creative Manager
├── Cross-app search
├── Unified notification / reminder layer
└── Personal OS dashboard
```

**Technical approach:** Nexus can be a parent React app that embeds the others
as iframes or micro-frontends, or simply a beautiful home screen linking to
your Vercel URLs. Start simple — a spatial launcher app.

-----

## SHARED DESIGN SYSTEM

All your apps should feel like one universe. Define these once:

```js
// design-tokens.js (shared across all projects)
export const TOKENS = {
  font:    "'Courier New', monospace",
  bg:      "#000010",
  surface: "rgba(255,255,255,0.05)",
  border:  "rgba(255,255,255,0.10)",
  text:    "rgba(255,255,255,0.85)",
  muted:   "rgba(255,255,255,0.35)",
  accent:  "#a78bfa",
  danger:  "#f87171",
  success: "#34d399",
  radius:  { sm:"8px", md:"12px", lg:"20px", full:"999px" },
  blur:    "backdrop-filter: blur(16px)",
}
```

Copy this file into every project’s `src/styles/` folder.
When you change a color, change it once. Updates everywhere.

-----

## LONG-TERM INFRASTRUCTURE (when you’re ready to go beyond free)

|When               |What      |Cost         |Why                                     |
|-------------------|----------|-------------|----------------------------------------|
|3+ apps live       |Supabase  |Free → $25/mo|Real database, auth, sync across devices|
|Sharing with others|Vercel Pro|$20/mo       |Custom domains, more bandwidth          |
|Selling access     |Stripe    |2.9% per txn |Payments for any of your tools          |
|Team collaboration |GitHub Pro|$4/mo        |Private repos with collaborators        |

None of this is needed now. The free stack handles everything for personal use
and even early user testing.

-----

## THE EXPERT MINDSET

You are not building apps. You are building **a personal software studio.**

The principles that separate 1% developers:

1. **One source of truth.** Code lives in GitHub. Nowhere else.
1. **Ship constantly.** Every Vercel deploy is a checkpoint.
1. **Design system first.** Shared tokens, shared components. Build once.
1. **Modular everything.** Each hook, each utility, each component is replaceable.
1. **Document as you go.** Your Master Project File is already proof of this.
1. **Let AI handle boilerplate.** You focus on vision and architecture.
1. **Cross-app thinking.** Every feature you build — ask: does Nexus need this too?

The goal is not to finish apps. The goal is to build a system
that lets you build any app in hours, not weeks.

-----

*Generated with Claude — update this document as your ecosystem evolves.*
*Version 1.0 · Brain Universe Project*