# Insighter Trader - Product Design Document

**Date:** February 4, 2026
**Status:** Validated
**Author:** Gabriel Curphey

---

## Executive Summary

**Insighter Trader** is a bold, visual-first stock research tool for young investors (ages 16-30) who want clarity, not complexity.

**Core promise:** "Stop guessing. Start knowing."

**What it is:**
- Free Progressive Web App (works on any device, installable on phones)
- Guided stock screener with simplified technicals, fundamentals, and news
- Revenue through brokerage affiliate links

**What it's NOT:**
- Not a trading platform (no executing trades)
- Not a portfolio tracker (not in MVP)
- Not for advanced traders (intentionally simplified)

---

## Target User

**Demographics:** 16-30 years old

**Psychographics:**
- Curious about investing, maybe owns a few stocks already
- Gets overwhelmed by TradingView, Webull, or similar tools
- Wants to find good stocks without a finance degree
- Lives on their phone, expects modern app experiences
- Shares discoveries on social media

---

## MVP Features

### Stock Screener (Core Feature)
Guided wizard, not open-ended filters:

1. **Step 1:** "What interests you?" - Sector selection (Tech, Healthcare, Energy, etc.) via visual cards
2. **Step 2:** "What's your style?" - Investment style (Growth, Value, Dividend, Trending) with one-sentence explanations
3. **Step 3:** "Your budget?" - Price range (Under $50, $50-200, $200+, Any)
4. **Results:** 5-10 matching stocks displayed as visual cards

### Stock Detail View
Progressive disclosure - simple at first, details on demand:

**Hero Section:**
- Company name, logo, current price
- One-line company description

**Vibe Check:**
- Color-coded sentiment indicator (green/yellow/red)
- Simple label: "Looking strong" / "Mixed signals" / "Caution"

**Three Tabs:**

| Tab | Contents |
|-----|----------|
| **Basics** | 4-5 key metrics as visual meters: P/E, Market Cap, 52-week range, Volume |
| **Chart** | Clean price chart with toggleable moving averages (50/200 day) and RSI |
| **News** | 5 recent headlines with source links |

**CTA:** "Want to buy? Compare brokers" (affiliate link)

---

## User Experience Principles

### 1. Guided Focus
- Step-by-step wizards, not open-ended dashboards
- Tell users what to look at, don't show everything at once
- "Duolingo for stock research" feel

### 2. Visual-First
- Color-coded cards over spreadsheets
- Simple charts over complex technical analysis
- Icons and meters over raw numbers
- Make it feel like Instagram, not Excel

### 3. Minimal Interface
- Maximum whitespace
- One action at a time
- Progressive disclosure (details only when tapped)
- No feature bloat

---

## Visual Design

### Brand Identity
- **Name:** Insighter Trader (or "Insighter")
- **Tagline:** "Stop guessing. Start knowing."
- **Tone:** Confident, punchy, no jargon, slightly irreverent

### Color Palette

| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| Primary | Electric Blue | #2563EB | CTAs, key actions |
| Positive | Neon Green | #10B981 | Gains, positive signals |
| Neutral | Amber | #F59E0B | Mixed signals |
| Negative | Red | #EF4444 | Losses, negative signals |
| Background | Near-black | #0F172A | Dark mode default |
| Text | White/Gray | #FFFFFF / #94A3B8 | High contrast |

### Typography
- **Headlines:** Bold sans-serif (Inter or Space Grotesk)
- **Body:** Clean, readable (Inter)
- **Numbers:** Monospace (JetBrains Mono)

### Visual Elements
- Dark mode by default
- Rounded cards with subtle glow effects
- Micro-animations on interactions
- Minimal icons, color conveys meaning

---

## Technical Architecture

### Tech Stack

| Layer | Technology | Rationale |
|-------|------------|-----------|
| Frontend | React + Next.js | Industry standard, huge learning resources, PWA-ready |
| Styling | Tailwind CSS | Rapid development, responsive by default |
| Backend | Next.js API routes | Same framework, no separate server needed |
| Database | Supabase (free tier) | PostgreSQL with auth, generous free tier |
| Hosting | Vercel (free tier) | One-click deploys, made for Next.js |

### Data Sources

| Data Type | Source | Cost |
|-----------|--------|------|
| Stock prices & fundamentals | Yahoo Finance API (unofficial) or Alpha Vantage | Free tier available |
| News | Finnhub or NewsAPI | Free tier available |
| Company logos | Clearbit Logo API | Free |

### PWA Features
- Installable on iOS/Android home screens
- Works offline (cached data)
- Fast loading, native-app feel
- One codebase for all platforms

### Estimated Running Costs
$0-20/month (domain + staying within free tiers)

---

## Monetization

### Model: Affiliate Revenue

Free tool with brokerage affiliate links. When users click "Compare brokers" and sign up for a brokerage, you earn a commission.

### Target Affiliate Programs

| Broker | Typical Commission | Appeal |
|--------|-------------------|--------|
| Robinhood | $20-50/signup | Brand recognition |
| Webull | $20-75/funded account | Generous payouts |
| Public | $10-20/signup | Gen Z friendly |
| Fidelity | Varies | Trusted name |

### Revenue Projections (Conservative)

| Monthly Users | Click Rate | Conversion | Signups | Revenue |
|---------------|------------|------------|---------|---------|
| 1,000 | 5% | 10% | 5 | $150 |
| 10,000 | 5% | 10% | 50 | $1,500 |
| 50,000 | 5% | 10% | 250 | $7,500 |

**Note:** Focus on growth first. Revenue follows traction.

### Legal Requirement
Clear affiliate disclosure on site: "We may earn a commission when you sign up for a brokerage through our links."

---

## Marketing Strategy

### Organic Growth (No Paid Ads)

| Platform | Content Type |
|----------|--------------|
| TikTok | 30-second demos, stock explainers, build-in-public |
| Instagram | Reels (repurposed), carousel educational posts |
| Reddit | Genuine participation in r/stocks, r/investing, r/GenZinvesting |
| Twitter/X | Market commentary, product updates, FinTwit engagement |
| YouTube | Longer tutorials (once traction exists) |

### Content Strategy

1. **Build in public** - Share journey learning to code, building product. People root for indie founders.
2. **Educate, don't sell** - "Here's how P/E ratio actually works" beats "Use my app"
3. **Show the product** - Screen recordings finding stocks with the tool
4. **Be consistent** - 3-5 posts/week minimum

### Growth Flywheel
1. Free tool provides value
2. Users share results ("Found this stock on Insighter")
3. New users discover tool
4. Repeat

---

## Roadmap

### Phase 1: Learn (Months 1-3)
- [ ] Complete HTML/CSS basics
- [ ] Learn JavaScript fundamentals
- [ ] Start React tutorials
- [ ] Set up development environment (VS Code, Git, Node.js)

### Phase 2: Build MVP (Months 4-7)
- [ ] Build guided screener wizard
- [ ] Integrate stock data API
- [ ] Create stock detail pages (basics, chart, news)
- [ ] Implement PWA functionality
- [ ] Design and polish UI

### Phase 3: Launch & Learn (Months 8-9)
- [ ] Soft launch to Reddit/Twitter for feedback
- [ ] Fix bugs, iterate on UX based on feedback
- [ ] Apply for affiliate programs
- [ ] Start consistent content creation

### Phase 4: Grow (Month 10+)
- [ ] Double down on what's working
- [ ] Add features based on user feedback
- [ ] Consider premium tier if affiliate revenue is slow

---

## Key Milestones

- [ ] First line of code written
- [ ] Screener prototype working locally
- [ ] Deployed to Vercel (live URL)
- [ ] First 100 users
- [ ] First affiliate commission

---

## Learning Path

### Order of Topics

1. **HTML/CSS basics** (2-3 weeks)
   - freeCodeCamp Responsive Web Design
   - Build simple static pages

2. **JavaScript fundamentals** (3-4 weeks)
   - freeCodeCamp JavaScript Algorithms
   - Practice with small projects

3. **React basics** (3-4 weeks)
   - Official React docs tutorial
   - Build 2-3 small React apps

4. **Next.js + Tailwind** (2-3 weeks)
   - Next.js official tutorial
   - Tailwind CSS docs

5. **Building Insighter** (ongoing)
   - Start simple, iterate
   - Use AI coding assistants to accelerate

### Recommended Resources
- freeCodeCamp (free)
- Scrimba React course (free tier)
- Next.js official docs
- YouTube tutorials (Fireship, Web Dev Simplified)

---

## Risks & Mitigations

| Risk | Mitigation |
|------|------------|
| Data API costs/limits | Start with free tiers, cache aggressively, upgrade only when needed |
| Affiliate programs reject you | Build traffic first, apply once you have users to show |
| Users don't convert to brokerages | Test different CTA placements, consider freemium as backup |
| Technical challenges | Use AI coding assistants, Stack Overflow, don't overcomplicate |
| Burnout at 15-25 hrs/week | Set realistic milestones, celebrate small wins |

---

## Success Metrics

### Leading Indicators
- Weekly active users
- Screener completions
- Stocks viewed per session
- Return user rate

### Lagging Indicators
- Affiliate link clicks
- Brokerage signups (conversions)
- Revenue

### MVP Success Criteria
- 100 users actively using the tool
- Positive qualitative feedback
- At least 1 affiliate conversion

---

## Open Questions for Future

- Portfolio tracking as premium feature?
- Watchlist functionality?
- Push notifications for price alerts?
- Community/social features?
- Mobile native apps (post-traction)?

These are explicitly NOT in MVP. Revisit after validating core product.

---

## Appendix: Competitive Analysis

### Why Existing Tools Fall Short for Target User

| Tool | Problem for Beginners |
|------|----------------------|
| TradingView | Overwhelming, complex interface, steep learning curve |
| Webull | Too many features, designed for active traders |
| Robinhood | Simple but lacks meaningful analytics |
| Yahoo Finance | Dated UX, not mobile-first |
| FINVIZ | Powerful but intimidating |

### Insighter's Positioning
"The middle ground" - Meaningful analytics presented simply. Not dumbed down, just thoughtfully designed.
