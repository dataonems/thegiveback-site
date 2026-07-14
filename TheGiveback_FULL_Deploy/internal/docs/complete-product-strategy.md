# TheGiveback — Complete Product & Strategy Document
### "Small is Sacred: Turning Everyday Payments into Everyday Ministry"
### Version 1.0 · July 2026 · Owner: Chris Humphrey / DataOne

---

## Table of Contents

1. [The North Star](#1-the-north-star)
2. [Christian Values Foundation](#2-christian-values-foundation)
3. [The Economic Engine](#3-the-economic-engine)
4. [The Full Circle Ecosystem](#4-the-full-circle-ecosystem)
5. [Product Architecture](#5-product-architecture)
6. [POS Integration Strategy](#6-pos-integration-strategy)
7. [Loyalty & Rewards Program](#7-loyalty--rewards-program)
8. [Card Issuing Strategy](#8-card-issuing-strategy)
9. [E-Commerce Marketplace](#9-e-commerce-marketplace)
10. [Agent Channel Model](#10-agent-channel-model)
11. [Foundation & Givehub Partnership](#11-foundation--givehub-partnership)
12. [AI Layer](#12-ai-layer)
13. [Competitive Landscape](#13-competitive-landscape)
14. [Legal & Compliance](#14-legal--compliance)
15. [Build Roadmap](#15-build-roadmap)
16. [Go-To-Market Strategy](#16-go-to-market-strategy)
17. [Success Metrics](#17-success-metrics)
18. [Fixed Decisions — Do Not Relitigate](#18-fixed-decisions--do-not-relitigate)

---

## 1. The North Star

Every day, small and medium-sized businesses process millions of transactions through payment rails like DataOne — and every one of those transactions sheds a few cents of margin into someone's pocket. For decades that margin has flowed one way: from merchant, through the processor, into residuals for sales agents and profit for owners.

**TheGiveback exists to redirect a portion of that flow — quietly, automatically, and joyfully — toward the people and causes doing real good in the world**, without asking merchants to do anything extra and without cutting into the agents who built the book of business.

The thesis is simple: *the infrastructure for generosity should be as automatic as the infrastructure for commerce.* DataOne already built the pipe. TheGiveback is what flows through it.

### The Core Insight: Closed-Loop Commerce

Block/Square proved that sitting on both the acquiring side (merchants accept payments) and the issuing side (consumers spend with your card) creates a closed loop. At scale, closed-loop transactions generate ~3% economics vs ~1% on open-loop. TheGiveback builds this same closed loop — but every incremental dollar of economics it captures goes directly into foundation giving, not just profits.

The five-word summary of what's being built:

> **Payments with a purpose. Giving by design.**

---

## 2. Christian Values Foundation

The product principles are drawn from Scripture and translated directly into build decisions. Faith is stated plainly in the founder's story and the About page — not repeated on every slide or page, but never hidden.

| Principle | Scripture | Product Decision |
|---|---|---|
| Faithful in little, faithful in much | Luke 16:10 | Radical transparency — every penny traceable to every payout. No black boxes. Ever. |
| Don't muzzle the ox | Deut. 25:4 / 1 Tim. 5:18 | The tithe comes from **our** earnings, not 1099 agents' residuals. Their split stays untouched. |
| God loves a cheerful giver | 2 Cor. 9:7 | Giving is automatic infrastructure, not a guilt-trip checkout prompt. |
| Let your light shine | Matt. 5:16 | Every merchant gets a visible, shareable story of the specific good their transactions caused. |
| Seek the welfare of the city | Jer. 29:7 | Default causes are hyper-local to the merchant's zip code before anything global. |
| The widow's mite | Mark 12:41-44 | A $9 barbershop giveback has identical dignity to a $9,000 enterprise giveback. Never tier generosity by size. |

### Voice Rules Across All Assets

- Faith foundation is stated once, plainly — not repeated as decoration on every page
- Scripture appears where it genuinely earns its place: founder letter, covenant section, closing slides
- "Ministry" in contexts where "mission" works just as well should use "mission" — reserve "ministry" for the founder's personal voice
- Copy is warm, specific, and humble — never preachy, never salesy, never guilt-based
- The works speak before the words

### Brand Architecture

- **DataOne** — the quiet, trusted B2B engine. Payment processing, bank relationships, agent economics. Does not need to wear the mission on its sleeve.
- **TheGiveback.org** — the public soul. Mission, story, marketplace, the place consumers and foundations actually meet. A nonprofit-*feeling* brand sitting on top of a for-profit engine. The .org domain is intentional.

Approved taglines:
- *"Every swipe, somewhere sacred."*
- *"The pennies were never small."*
- *"Payments with a pulse."*

---

## 3. The Economic Engine

### Margin Structure

DataOne processes across three merchant categories with these economics:

| Category | Volume Share | Margin | Notes |
|---|---|---|---|
| Low-risk / dual pricing | 55% of book | ~1.8% | Market moving to 65% of low-risk |
| Low-risk / traditional | 30% of book | ~0.40% (40 bps) | Remainder of low-risk book |
| High-risk | 15% of book | 1.5–3.0% | Midpoint 2.25% blended |

**Blended gross margin: ~1.45% on total volume**

### The Waterfall

```
Transaction fee (100% gross revenue)
   └── Agent residuals (25–85% of gross — NEVER TOUCHED)
   └── Company retained margin
          └── 20–30% → The Giveback Pool (covenant, in writing)
          └── Remainder → Operations, growth, owner return
```

### Two Separate Pools — Never Conflated

| Pool | Source | Story | Structure |
|---|---|---|---|
| Company Giving | 20–30% of DataOne's retained margin | "We give because it's who we are" | Covenant — fixed in writing, holds in bad quarters |
| Consumer Round-Up | Optional at checkout — 100% pass-through, zero skimmed | "You can give too, if you want" | Invitation — routes through DAF intermediary (see legal section) |

### What the Numbers Produce

At a 50% blended agent split and 25% giveback rate:
- Every **$1M of monthly volume** generates ~**$21,765/year** into the Giveback Pool
- At **$25M/month** → ~$544K/year
- At **$100M/month** → ~$2.18M/year
- At **$250M/month** → ~$5.4M/year

The dual-pricing shift is a **structural tailwind**: moving from traditional (40bps) to dual pricing (180bps) is a 4.5× margin increase. The covenant gets easier to keep as the market moves, not harder.

---

## 4. The Full Circle Ecosystem

Six layers in a clockwise closed loop. Each feeds the next. The loop compounds with every merchant added and every cardholder enrolled.

```
DataOne Acquiring
       ↓
Certified Merchant Storefronts
       ↓
TheGiveback Marketplace
       ↓
Giveback Card (Issuing)
       ↓
Giveback Points
       ↓
Foundation Giving Pool
       ↓ (foundations promote certified merchants → more merchants join DataOne)
DataOne Acquiring [loop]
```

### The Closed-Loop Premium

| Transaction Type | Acquiring Revenue | Issuing Revenue | Total Economics | Giving Generated |
|---|---|---|---|---|
| Any card, any merchant | ~1.45% | — | ~1.45% | 20–30% of acquiring margin |
| Any card, certified merchant | ~1.45% | — | ~1.45% | 20–30% + marketplace story |
| Giveback Card, non-certified | — | ~1.5–2.0% | ~1.75% | Points → optional donation |
| **Giveback Card, certified merchant ✦** | **~1.45%** | **~1.5–2.0%** | **~3.0%** | **Covenant + points → ~3× giving per swipe** |

The starred row is the closed loop. It's the same transaction type Block/Square earns premium economics on — but every incremental dollar funds more giving.

### Four Non-Negotiable Design Rules

1. **TheGiveback never sells its own products.** The marketplace lists and sells merchant products only. You are infrastructure, never a competitor. This is permanent.
2. **Zero platform fee to certified merchants.** You earn acquiring margin on every marketplace transaction. A listing fee would turn a retention asset into an extraction mechanism.
3. **Marketplace before card.** The Giveback Card needs a live certified merchant network before it has a reason to exist. Build Phase 3 before pitching BaaS partners.
4. **Points stay inside the ecosystem.** Donate to foundations, redeem at certified merchants, or take a statement credit. No airline transfer partners. Ever. Complexity killed Bilt. Simplicity serves the mission.

---

## 5. Product Architecture

### The Five Layers Built in Order

#### Layer 1 — Transaction Intelligence Layer (Phase 1)
*The engine. No POS dependency.*

A cloud-based API that sits between DataOne's settlement reporting and the giveback ledger. Settlement data arrives as a batch file or webhook. The intelligence layer enriches it with:
- Merchant category and zip code
- Risk class (low-dual / low-traditional / high-risk)
- Giveback calculation (20–30% of company retained margin)
- Agent residual validation (input, never output — enforced structurally)
- Allocation to matched foundations

This layer feeds every dashboard, every impact story, and every foundation disbursement. It runs entirely in the cloud. Zero POS dependency.

#### Layer 2 — Merchant Impact Dashboard (Phase 1–2)
*Progressive web app. Works on any device.*

What it shows:
- **The Number** — monthly giveback in dollars, displayed with equal visual weight at $9 or $9,000
- **Where it went** — 1–3 cause cards with foundation name, mission, dollars given, and AI-generated equivalence ("≈ 64 meals")
- **Share your light** — AI-generated monthly impact post, ready for Instagram/Facebook
- **Penny-to-payout trail** — accordion expanding to show full calculation
- **Certification block** — badge, window decal files, web embed code

Design rules:
- Mobile-first, one screen, 5-minute session cadence
- Magic link auth via DataOne merchant email — no new password
- Small merchants never see a "starter" look — same layout at every size
- Two separate counters for company giving and consumer round-up — never share a number

#### Layer 3 — Consumer Mobile App (Phase 3)
*iOS + Android. Built in React Native for single codebase.*

What it does:
- Browse certified merchants by zip code and category
- See real-time giving generated by those merchants
- Track Giveback Points balance (Phase 4)
- Round-up add-on before POS integration exists: consumer taps "add $1 to my giving for this visit," shows merchant a QR code — zero POS API, zero terminal modification, zero PCI scope
- Redeem points at certified merchants (Phase 4–5)

This is also the round-up delivery mechanism in Phase 3 before any POS integration exists. It lives entirely outside the payment flow — no PCI scope expansion.

#### Layer 4 — Public Ledger API (Phase 2)
*Read-only. Anyone can verify.*

Endpoints:
- `GET /ledger/summary` — lifetime + monthly totals, two pools never merged
- `GET /ledger/periods/{month}` — per-cause disbursements, receipts, checkpoint hash
- `GET /ledger/merchants/{slug}` — giveback totals and causes (no volume, no margin, no pricing)
- `GET /ledger/causes/{id}` — vetting status and disbursement history

The merchant dashboard "penny-to-payout" accordion reads these same endpoints. The merchant sees exactly what the public sees.

#### Layer 5 — Foundation Portal (Phase 3–4)
*Self-serve. Powered by Givehub API integration.*

Built on top of Givehub's nonprofit software rather than from scratch. TheGiveback's Transaction Intelligence Layer sends enriched giveback events to Givehub's API when a disbursement is confirmed. Givehub handles:
- Foundation management
- Disbursement reporting
- Tax receipts
- Impact tracking
- Donor reporting for foundations

TheGiveback's portal handles:
- Foundation application and vetting workflow
- AI-powered 90-day rolling forecasts
- Public impact page per foundation
- Vetting expiry tracking and re-vetting alerts

Integration point: a single webhook from TheGiveback ledger to Givehub when a disbursement batch is confirmed.

### The Append-Only Ledger

Non-negotiable architecture:
- No row is ever updated or deleted. Corrections are new entries referencing what they correct.
- Two separate schemas: company giving ledger and consumer round-up ledger. They never share a table, a total, or an API response field.
- SHA-256 hash chaining on checkpoint records. Anyone can verify entries haven't been altered.
- Two-person approval on every disbursement run (initiator ≠ approver).
- Minimum disbursement threshold: $25 per cause per period. Below that, funds carry forward visibly.
- Failed disbursements stay on the public record with their failure reason. We publish the misses.

---

## 6. POS Integration Strategy

### The Key Insight

The giving calculation happens in DataOne's settlement layer — not at the POS terminal. Settlement data is the source of truth for every giveback dollar. This means the entire platform works with **zero POS integration** through Phases 1 and 2.

POS integrations are only needed for two specific features:
1. **Consumer round-up prompt at the terminal** (Phase 3) — display a tapping prompt at checkout
2. **Giveback Points redemption at the terminal** (Phase 4–5) — redeem points as merchant discount

Everything else — giving calculation, merchant dashboard, foundation disbursement, public ledger — runs entirely off settlement data.

### Build Order for POS Integrations

**Phase 3 — Before any POS integration:**
Use the consumer mobile app QR code flow for round-up. Consumer taps "add $1 to my giving for this visit" in the app, shows merchant a QR code. Merchant scans with any device. Done. No POS API, no terminal modification, zero PCI scope.

**Phase 3 — First POS integration: Clover**

Why Clover first:
- Open Android-based platform with a proper App Market — merchants can discover TheGiveback app the same way they discover any app
- Backed by Fiserv (processes 50%+ of global card transactions) — massive SMB reach
- Native Android app model means TheGiveback app is a standard APK
- App Market is the best organic acquisition channel in the POS world — merchants browsing for tools find TheGiveback

What to build:
- A Clover App Market app that adds the round-up prompt to any Clover device
- App sits **outside** the secure payment flow (no PCI scope expansion)
- Fires a webhook to TheGiveback's Transaction Intelligence Layer on round-up confirmation

**Phase 4 — The Agnostic Middleware Layer**

Rather than building four separate POS integrations, build one middleware layer with a normalized transaction event schema:

```
POS Webhook (Clover / Toast / Square / Lightspeed)
       ↓
Middleware (normalize to standard event schema)
       ↓
TheGiveback Transaction Intelligence Layer
```

Each POS fires its own webhook format. Middleware normalizes to a standard event. The platform processes identically regardless of which terminal sent it.

Priority after Clover:
1. **Square** — open API, large SMB retail base, good developer experience
2. **Lightspeed** — solid webhook support, strong in retail and restaurants, widely used
3. **Toast** — restaurant-specific, requires Toast Partner API approval (gated), read-only access — harder but reaches a large restaurant merchant base

### What Not to Build

- Don't build your own POS
- Don't intercept the payment itself to add the round-up — this triggers money transmission exposure and PCI scope expansion
- Don't build POS integrations before the merchant dashboard and consumer app are live — prove the value before adding the complexity

---

## 7. Loyalty & Rewards Program

### The Single Currency Rule

One unit. Three redemption paths. No exceptions.

| Redemption | Description | Why |
|---|---|---|
| **Donate to a foundation** | Convert points to direct giving to the merchant's matched cause | Primary path — serves the mission |
| **Merchant discount** | Redeem at any certified merchant storefront | Keeps money inside the ecosystem, feeds the flywheel |
| **Statement credit** | Standard cash-equivalent value | Simple fallback |

No travel transfer partners. No hotel points. No airline miles. The complexity of a points-transfer ecosystem is what caused Bilt's operational collapse and confused its customers. TheGiveback's brand promise is simplicity and local impact — a Chase Sapphire-style catalog is incoherent with that promise.

### Earning Rules

- Points earned on every purchase at certified merchants (bonus rate vs. non-certified)
- Points earned on every marketplace purchase
- Points earned on every purchase with the Giveback Card anywhere (Phase 4+)
- Closed-loop premium: Giveback Card + certified merchant = highest earn rate

### The Bilt Lesson

Bilt rewarded rent payments (near-zero interchange) while funding rich travel rewards — Wells Fargo lost $10M/month and exited the partnership. TheGiveback's version has the opposite structure: merchant-present card interchange (the highest interchange category) underneath a simple points currency with three redemption paths. The economics actually support the loyalty program.

### Build Sequence

- **Phase 3** — Enable Giveback Points via Pledge API (or similar card-linking API) on marketplace purchases using any existing card. No branded card needed. This generates behavioral data and consumer habit before committing to the full BaaS card program.
- **Phase 4** — Launch Giveback Card. Points now earned across all spend, with bonus rates at certified merchants.
- **Phase 5** — Full closed-loop closed: Giveback Card + certified merchant + marketplace = maximum giving per transaction.

### Points Liability Note

*(Not legal advice — CPA question before launch.)*
Unredeemed loyalty points are a liability on the balance sheet. The accounting treatment and reserve methodology need a CPA conversation before any points program launches.

---

## 8. Card Issuing Strategy

### The Architecture

A co-branded Visa or Mastercard debit card issued via a BaaS partner on top of a Durbin-exempt sponsor bank (to preserve higher interchange economics).

**Why debit, not credit:**
- Simpler regulatory path
- No credit underwriting required
- Durbin-exempt issuers preserve ~1.5–2% interchange on card-present transactions
- Lower operational complexity for Phase 4 launch

**BaaS partner candidates (US):**
- Marqeta — API-first, powers DoorDash and Uber, deep card controls, programmable spend rules
- Galileo (SoFi-owned) — strong neobank track record, national bank charter access, deep API
- Lithic / Highnote — developer-first, faster launch, good for early-stage programs

**Sponsor bank candidates:**
- Evolve Bank & Trust, Stride Bank, Celtic Bank, Lead Bank — all Durbin-exempt, established BaaS relationships

### Sequencing

Do not approach BaaS partners until Phase 3 is complete. The pitch to Marqeta or Galileo requires:
- A live certified merchant network with real transaction volume
- A real giving track record (at least 6 months of disbursements)
- Behavioral data from the Phase 3 points-via-Pledge layer
- A waitlist of consumers who've already engaged with the platform

The card program launches to a warm audience, not cold. Timeline: Phase 4 at months 12–18.

### The Closed-Loop Economics

When a Giveback cardholder purchases at a certified merchant on the marketplace:
- DataOne earns acquiring margin (~1.45%)
- Giveback Card program earns issuing interchange (~1.5–2.0%)
- Total economics: ~3.0% on the same transaction
- Giving generated: covenant share of acquiring margin + optional points donation by consumer

Compared to today's open-loop transaction generating ~0.36% in giving (at 1.45% margin × 25% covenant × 50% agent split), the closed loop potentially generates 3–5× more giving from the same transaction — without changing rates, without asking anyone to give more.

---

## 9. E-Commerce Marketplace

### What It Is

TheGiveback.org becomes a shop-local commerce platform — not just a directory but a place to actually buy from certified merchants. Not an Amazon competitor. A local commerce layer.

Each certified merchant gets:
- A free digital storefront (products, services, appointment booking, gift cards, digital offerings)
- DataOne processes all storefront payments, earning acquiring margin on each sale
- Zero platform fee to merchants — you earn through processing
- Every purchase generates the giving story

### What Merchants List

| Category | Examples |
|---|---|
| Physical products | Retail inventory, handmade goods, food items |
| Services | Haircuts, repairs, consulting, cleaning |
| Bookings | Appointments, reservations, classes |
| Gift cards | Digital gift cards redeemable in-store |
| Digital goods | Online classes, downloads, subscriptions |

### Consumer Discovery

- Browse by zip code (hyper-local default)
- Browse by category (food / retail / services / health / etc.)
- Browse by cause (merchants matched to food security / youth / housing / etc.)
- Each purchase page shows the giving generated per transaction in real time

### What the Marketplace Is Not

- Not a competitor to merchant's own website or other sales channels
- Not a marketplace with TheGiveback's own products
- Not a race-to-the-bottom pricing platform
- Not an Amazon-style review and ranking system that creates winners and losers among certified merchants

### Technical Foundation

The marketplace runs on DataOne's existing acquiring rails — no new payment infrastructure needed for Phase 3. Every marketplace transaction is a DataOne-acquiring transaction and generates the standard giveback calculation. The marketplace storefront is a lightweight product catalog and booking layer sitting on top of existing payment processing.

---

## 10. Agent Channel Model

### Two Separate Agent Channels

| Channel | Split | Merchants | Story | Leads |
|---|---|---|---|---|
| **DataOne Agents** (existing) | 25–85% blended | Outbound from agent relationships | Payment processing pitch with giveback added | Agent-sourced |
| **TheGiveback Agents** (new) | **20% flat** | Inbound from platform, foundation networks, community organizations | Mission-first certification pitch | Platform-generated |

### Why 20% Works for TheGiveback Agents

- TheGiveback agents are selling a differentiated product — not competing with other ISOs on rates
- Merchants who come through the certification channel have lower churn (they believe in the mission)
- 20% on a book of non-churning merchants outperforms 50% on a book with normal payment industry churn rates
- Agents self-select: those who sign up at 20% do so because they connect with the mission — they tell the story honestly and well

### Conflict Resolution Rule

- Merchants who come inbound through TheGiveback.org → TheGiveback agent account (20% split)
- Merchants who are approached cold by a DataOne agent and pitched the certification program → DataOne agent account (normal split, with certification added as a feature)
- Adding giveback certification to an existing DataOne merchant's account stays with the DataOne agent at their normal split — never routed to a TheGiveback agent

This protects existing agent relationships and creates clear channel rules.

### TheGiveback Agent Value Stack

Beyond the 20% split:

| Benefit | Description |
|---|---|
| Certification bonus | One-time payment per merchant onboarded (from marketing budget, not giving pool) |
| Foundation match bonus | Quarterly bonus when agent connects merchants to a new vetted foundation in a new zip code |
| Marketplace activation bonus | When a certified merchant goes live with a storefront |
| Agent Certified designation | Badge, impact dashboard showing total giving generated by their book |
| Public ledger attribution | Agent's name attached to the giving generated by their merchant relationships |

### TheGiveback Agent Needs (Build List)

1. **Agent portal** — their version of the merchant dashboard: book's total giving generated, merchant certification status, foundation matches, and their own income view
2. **Pitch kit** — the certification conversation is different from a payment processing pitch. Scripts, leave-behind materials, foundation relationships pre-baked
3. **Foundation referral pipeline** — foundations funded by the giving program become the best lead sources for agents. Make this loop explicit and rewarded

### Best Agent Profile

- People with existing relationships inside community organizations, churches, chambers of commerce, and nonprofits
- Faith-community networkers
- Former nonprofit fundraisers who understand mission-driven selling
- Local business advocates and chamber staff

---

## 11. Foundation & Givehub Partnership

### Division of Labor

| TheGiveback Builds | Givehub Handles |
|---|---|
| Transaction intelligence and giveback calculation | Foundation management software |
| Foundation application and vetting workflow | Disbursement processing |
| AI-powered 90-day rolling forecasts | Tax receipts |
| Public impact page per foundation | Impact tracking and reporting |
| Vetting expiry tracking | Donor reporting tools |
| Merchant-to-foundation matching (AI) | Nonprofit compliance infrastructure |

### Integration Architecture

Single webhook from TheGiveback ledger to Givehub API when a disbursement batch is confirmed. Givehub handles everything downstream. TheGiveback handles everything upstream.

### Vetting Standard

Before any foundation receives a disbursement:
1. **501(c)(3) status in good standing** — verified via IRS Tax Exempt Organization Search, re-checked annually
2. **Financial health check** — most recent 990 reviewed for reasonable overhead ratios and no unresolved audit findings. Charity Navigator-equivalent standards minimum.
3. **Mission alignment** — prioritize foundations serving food insecurity, youth, housing, and community development in the zip codes where certified merchants operate. Local first, always.
4. **Leadership conversation** — brief call with executive director or board chair. Human judgment stays in the loop.

### What Foundations Receive

- Predictable monthly disbursements (forecastable, not just reactive)
- AI-powered 90-day rolling forecast for program planning
- Public impact page visible to their board and donors
- Zero grant applications or reporting burden beyond the annual vetting renewal
- Every disbursement includes a receipt that appears on the public ledger

### The Three Giving Streams (Separately Labeled Forever)

| Stream | Source | Label in Dashboard |
|---|---|---|
| Covenant | 20–30% of DataOne's acquiring margin | "Given by [Business Name]" |
| Points redemption | Consumer Giveback Points converted to donations | "Given by [Business Name]'s customers" |
| Round-up | Optional consumer checkout addition | "Added by [Business Name]'s customers" |

These three streams are never combined into a single number. They have separate ledger entries, separate dashboard displays, and separate public records.

---

## 12. AI Layer

AI earns its keep at specific, load-bearing jobs — not as decoration:

| Function | What It Does | Where It Lives |
|---|---|---|
| **Cause-matching engine** | Suggests relevant local foundations to new merchants based on category + zip code. A bakery gets matched to food insecurity before arts foundations two states away. | Onboarding flow |
| **Vetting copilot** | Cross-references 990 filings, financial health, and mission claims to flag red flags for human review. Speeds vetting without removing human judgment. | Foundation application processing |
| **Impact story generator** | Turns "$412 given this month" into a short, specific, shareable post a merchant can drop straight onto Instagram. The "let your light shine" mechanism at scale. | Merchant dashboard (monthly) |
| **Onboarding concierge** | Conversational assistant that walks a new merchant or nonprofit through setup in minutes instead of a form. | Merchant + foundation onboarding |
| **Foundation forecasting** | Gives foundations a rolling 90-day estimate of expected funding for program planning. | Foundation portal |
| **Robotica AI integration (Phase 4)** | Video intelligence and computer vision (OTIS stack) instruments foundation programs to generate engagement/impact data. Turns "$412 given" into a measured outcome. | Foundation impact measurement (Tilmon partnership) |

### Robotica AI / OTIS Integration Notes

*(See separate document: robotica-ai-dataone-giving-synergy.md)*

The OTIS layer requires:
- At least one pilot foundation willing to instrument a real program before making public claims
- OTIS deployment funded from DataOne's giving-program margin, not sold to foundations separately
- IP and legal review with Derek Young before build — deal structure, IP carve-out between commercial (OTIS/DataOne) and defense (DVBE) use cases
- Separate consent/data governance review for biometric data collected on program participants

---

## 13. Competitive Landscape

### Category A — Payment Processors That Tithe Their Margin

| Company | Gives From | Causes | Marketplace | Dashboard |
|---|---|---|---|---|
| Pro-Life Payments | 15% of revenue | Single cause (pro-life) | None | None |
| EPS Processing | % of profits | Merchant-designated church | None | None |
| AdelFi | Member cardholder spend | Christian ministries | None | None |
| **TheGiveback ✦** | **20–30% of company margin** | **Multi-cause, vetted, hyper-local** | **Yes** | **Yes** |

Single-cause, single-beneficiary, no marketplace, no dashboard — that's every competitor. The three-sided system is the actual differentiation.

### Category B — Round-Up Infrastructure

| Company | Structure | Key Feature |
|---|---|---|
| Pennies (UK) | Registered charity itself | 190M donations, £45M raised since 2010 |
| RoundUp.org | Routes through DAF (Our Change Foundation) | 1.3M nonprofits available |
| DailyKarma / Shop for Good | Shopify app with co-venture compliance | Sells the compliance work as a feature |
| Mastercard Donate API | Card-network-level infrastructure | Licensable rails |

**The pattern that matters:** every working competitor in the consumer round-up space routes funds through either a registered charity or a DAF intermediary. This is not a coincidence — it's the legal solution to money transmission exposure on consumer funds. See Section 14.

### The Differentiation Table

| | Pro-Life Payments | Bilt | Pennies | RoundUp | **TheGiveback** |
|---|---|---|---|---|---|
| Gives from own margin | ✓ | — | — | — | **✓** |
| Multi-cause marketplace | — | — | — | — | **✓** |
| Merchant dashboard | — | — | — | — | **✓** |
| Foundation vetting | — | — | — | — | **✓** |
| AI impact layer | — | — | — | — | **✓** |
| Closed-loop card issuing | — | ✓ (failed) | — | — | **✓ (Phase 4)** |

---

## 14. Legal & Compliance

*Landscape only — not legal or financial advice. Everything in this section needs a fintech attorney and CPA before real dollars move.*

### What Is Legally Clear

Giving away 20–30% of your own profits is unambiguously legal. Newman's Own (100% of profits since 1982, $600M+ given away), Patagonia (100% to Holdfast Collective), and Pro-Life Payments all confirm this is normal territory. Nobody needs permission to be generous with money they own.

### The Two Things That Need Legal Review Before Money Moves

**Priority 1 — §162 vs. §170 characterization**

The One Big Beautiful Bill Act (signed July 2025) creates a 1% floor and 10% cap on C-corporation charitable deductions for tax years beginning after December 31, 2025. At 20–30% of margin, you'll likely exceed the 10% cap, meaning a large share of the giveback may not be currently deductible as a straight §170 charitable contribution.

The alternative: the IRS has an existing line of authority (LTR 9309006, a supermarket chain setting aside 1% of sales annually) treating an advertised, ongoing percentage-of-sales giving program as an ordinary and necessary **business expense under §162** — which has no caps. This structuring question is worth real money at your volume.

**→ CPA + tax attorney conversation before finalizing disbursement mechanics.**

**Priority 2 — Consumer round-up DAF structure**

Consumer funds collected for third-party nonprofits are closer to regulated money transmission than company-owned funds. Every working competitor (Pennies, RoundUp.org) resolves this by routing through either a registered charity or a donor-advised fund intermediary.

**→ DAF partner OR own 501(c)(3) decision must be made before round-up ships publicly. Cannot be skipped.**

### Commercial Co-Venturer Regulations

The moment you advertise "your purchase generates a donation" — which is the entire point of the Giveback Certified badge — you're operating in commercial co-venture territory in ~21–40 states (depending on definition).

Typical requirements:
- Written contract with each specific charity
- Registration in ~6 states (California: $500 fee, Form CT-5CF before working with any charity)
- Point-of-advertising disclosures stating actual dollar amount or percentage
- Post-campaign financial reporting
- Surety bonds in Massachusetts and Alabama ($10,000–$25,000)

**Practical path:** Use CogencyGlobal, Harbor Compliance, or Labyrinth for state filing management. This is a budgetable, solvable line item — not an open legal risk. Budget $15K–$30K/year for multi-state compliance management.

### Money Transmission

- **Company covenant (20–30% of own margin):** Not money transmission. You're donating money that is legally already yours. No MTL, no FinCEN MSB registration.
- **Consumer round-up funds:** Much closer to regulated activity. Resolve with DAF structure (see Priority 2 above).

### Additional Items

- **Board resolution or personal covenant in writing** — before the first disbursement. Protects the covenant from a future bad quarter and addresses fiduciary duty if any outside shareholders exist.
- **Charity due diligence** — IRS Tax Exempt Organization Search check on every foundation before first disbursement, and annually after. Already anticipated in the vetting_expires_at field in the ledger spec.
- **Merchant data sharing** — DataOne merchant data used in TheGiveback requires a data-sharing basis in the merchant agreement. Add a consent line to certification onboarding.

---

## 15. Build Roadmap

### Phase 1 — Prove the Plumbing (Days 1–90)

*Nothing public. Prove the math works.*

- [ ] Write the covenant in writing — board resolution or personal document before first disbursement
- [ ] Build the append-only ledger with hash chaining and dual-approval disbursement
- [ ] Wire accrual + disbursement logic into DataOne's settlement flow
- [ ] Select 5–10 pilot merchants from existing DataOne book (pick across sizes — protect widow's mite principle)
- [ ] Select 3–5 vetted local foundations tied to pilot merchants' communities
- [ ] Verify each foundation via IRS Tax Exempt Organization Search
- [ ] Run first complete settlement cycle end-to-end
- [ ] Confirm first real disbursement with receipt
- [ ] Internal ops dashboard only — no public site
- [ ] Definition of done: a stranger with database read access can trace every giveback dollar from merchant volume to foundation receipt

### Phase 2 — Tell the Story (Days 90–150)

*First public presence. Real numbers only.*

- [ ] TheGiveback.org launches with live giving counter (real number, even if $847)
- [ ] Merchant directory of certified pilot merchants
- [ ] Foundation application form + vetting workflow
- [ ] Merchant impact dashboard (web app, mobile-first)
- [ ] AI-generated monthly impact post for each certified merchant
- [ ] Public ledger API (read-only endpoints)
- [ ] Givehub API integration for foundation disbursement and reporting
- [ ] Begin commercial co-venture state filings
- [ ] Press pitch when giving counter goes live — lead with the real dollar number

### Phase 3 — Open the Marketplace (Days 150–240)

*Commerce layer goes live. Consumer app ships.*

- [ ] Certified merchant digital storefronts (product listings, services, bookings, gift cards)
- [ ] Consumer-facing directory + map
- [ ] iOS + Android consumer app (React Native)
- [ ] Round-up via consumer app QR code flow (no POS integration needed)
- [ ] Giveback Points via Pledge API card-linking (any existing card, certified merchant purchases)
- [ ] Clover App Market app (round-up prompt at terminal, outside payment flow)
- [ ] DAF partner OR own 501(c)(3) for round-up — must be in place before round-up ships
- [ ] Foundation self-serve portal with AI forecasting
- [ ] TheGiveback agent channel launch: agent portal, pitch kit, agent certification

### Phase 4 — Scale the Rails (Months 9–14)

*Card program launches. Ecosystem deepens.*

- [ ] BaaS partner selection (Marqeta or Galileo + Durbin-exempt sponsor bank)
- [ ] Giveback Card program launch to Phase 3 waitlist
- [ ] Closed-loop economics begin: acquiring + issuing on certified merchant transactions
- [ ] Agnostic POS middleware layer (Square + Lightspeed + Toast integrations)
- [ ] Partner ISO / bank onboarding (non-DataOne merchants join certification program)
- [ ] Foundation referral pipeline formalized as merchant acquisition channel
- [ ] Robotica AI / OTIS pilot at one foundation program
- [ ] B Corp certification application (6–12 months lead time)

### Phase 5 — Full Platform (Months 14–24)

*The flywheel at full speed.*

- [ ] Full closed-loop: Giveback Card + certified merchant + marketplace
- [ ] Robotica AI impact measurement layer (measured impact replaces reported impact)
- [ ] Aggregate impact benchmarks by program category (sector data product)
- [ ] Merchant-tier giving options gated by measured impact score
- [ ] Newman's Own / foundation ownership structure exploration (long-term legacy planning)
- [ ] Giveback Card credit product exploration (if debit program proves unit economics)

---

## 16. Go-To-Market Strategy

### Audience Priority Order

| Audience | Why First | Message | Channel |
|---|---|---|---|
| Existing DataOne merchants | Already processing — zero cold start | "You're already certified. Here's what your transactions gave back this month." | Direct outreach, no pitch needed |
| 1099 DataOne agents | They own the merchant relationships | "We don't touch your residuals. Ever. And now you have a story to sell nobody else in payments can tell." | Brief before Phase 2 launch |
| Local foundations in pilot zip codes | Easiest sell — predictable recurring revenue is what every nonprofit director dreams about | "Monthly check, public impact page, AI forecasting. Apply once. No grants." | Warm outreach to 3–5 before Phase 2 |
| Local and faith media | "Payment processor routes 25% of its own margin to local causes" writes itself | Lead with real dollar number, however small | Pitch day the giving counter goes live |
| Merchant-generated social content | Auto-generated monthly impact posts = organic word-of-mouth | "My haircuts helped stock the food pantry this month." | Automatic — ships with Phase 2 dashboard |
| Partner ISOs and banks | License the certification layer | "Your merchants get certified, your margin funds the giving, the marketplace benefits everyone." | Phase 4 only — need receipts first |
| B Corp / 1% for the Planet networks | Conscious-business switchers | 20–30% of margin is an extraordinary commitment | Phase 4 — after certification application starts |
| Investors | Differentiated payment business with structural covenant | Full pitch deck + financial model | Phase 2–3 once giving track record exists |

### The One Metric That Determines Everything

Did you keep the covenant in a bad quarter?

Not transaction volume. Not merchant count. Not foundation dollars. The product is the giving infrastructure. But the business — the thing that earns trust from merchants, foundations, agents, and the press — is the decision made when Q3 comes in light and someone suggests "temporarily" reducing the giveback rate.

Document the covenant in writing now, before the first bad quarter, so it can't be quietly re-litigated later.

---

## 17. Success Metrics

### North Star Metrics

| Metric | Why It Matters |
|---|---|
| Total $ given (cumulative + monthly velocity) | The whole reason this exists |
| Merchant voluntary retention rate | Are they staying *because* of TheGiveback, not despite it? |
| Foundation disbursement predictability score | Are foundations actually planning programs around the income? |
| Agent retention / satisfaction (both channels) | The model only works long-term if the sales force never feels shortchanged |
| Closed-loop transaction share (Phase 4+) | % of transactions where DataOne earns both acquiring and issuing — the flywheel efficiency metric |
| Public transparency score | The single number that proves this isn't give-washing |

### Operational Metrics

- Consumer app round-up opt-in rate (not just volume)
- Merchant dashboard monthly active rate (are merchants actually using it?)
- Impact post share rate (are merchants sharing their light?)
- Foundation vetting time from application to first disbursement
- Agent portal activation rate (are TheGiveback agents using their tools?)
- Clover App Market install rate (organic discovery working?)

### What Not to Measure

- No merchant leaderboards — violates widow's mite principle
- No foundation rankings by dollars received — not a competition
- No gamification streaks for merchants or consumers

---

## 18. Fixed Decisions — Do Not Relitigate

These are settled. If a new idea conflicts with any of these, say so directly and route around them rather than undoing them.

| Decision | Rationale |
|---|---|
| Agent residuals (25–85%) are permanently off the table for funding the giveback | Structural integrity — agents must never feel they're subsidizing the covenant |
| Two separate giving pools, never conflated | One is a covenant, one is an invitation. Different stories, different ledger entries, different dashboard lines. |
| DataOne is the quiet B2B engine. TheGiveback.org is the public soul. | Brand architecture is settled. |
| Giving comes from company retained margin only | Never from rates, never from merchant fees, never from agents |
| Marketplace never sells its own products | TheGiveback is infrastructure, never a competitor to its certified merchants |
| Zero platform fee to certified merchants | You earn through processing, not through listing fees |
| Giveback Card: no travel transfer partners, ever | Currency simplicity serves the mission. Complexity killed Bilt. |
| Round-up routes through DAF or registered charity | Every working competitor made this same legal choice for the same reason |
| Small merchant giveback has identical dignity to large merchant | Never deprioritize the little guy for efficiency |
| Default causes are hyper-local before global | Seek the welfare of the city. Always. |
| TheGiveback agent split is 20% flat — a new channel, not a change to existing agents | Protects existing agent relationships. Option B, not Option A. |
| Marketplace before card | Card program needs live merchant network to be meaningful to cardholders |
| Phase 1 completes before Phase 2 launches | The giving counter must show real dollars before the public website goes live |

---

## Appendix A — The Economic Model (Key Assumptions)

| Assumption | Value | Source |
|---|---|---|
| Dual pricing margin | 1.8% | Owner, July 2026 |
| Traditional processing margin | 0.40% (40 bps) | Owner, July 2026 |
| High-risk margin | 1.5–3.0% (2.25% midpoint) | Owner, July 2026 |
| Low-risk book: dual pricing share | 65% | Owner, July 2026 |
| Low-risk book: traditional share | 35% | Owner, July 2026 |
| High-risk share of total book | 15% | Owner, July 2026 |
| Blended gross margin (calculated) | ~1.45% | Model output |
| Blended agent split (placeholder) | 50% | Replace with actual DataOne blended figure |
| Giveback covenant rate | 25% (range: 20–30%) | Covenant |
| Annual giveback per $1M monthly volume | ~$21,765 | At 50% agent split, 25% giveback |

*Replace placeholder volume and blended agent split with actual DataOne figures before any investor or board meeting.*

---

## Appendix B — Key Vendor Relationships to Establish

| Vendor | Purpose | Phase |
|---|---|---|
| Givehub | Foundation software, disbursement, nonprofit reporting | Phase 1 |
| Pledge.to (or similar) | Points-to-charity DAF API, round-up DAF compliance | Phase 3 |
| CogencyGlobal / Harbor Compliance / Labyrinth | Commercial co-venture state filings | Phase 2–3 |
| Marqeta or Galileo | BaaS + card issuing | Phase 4 |
| Durbin-exempt sponsor bank | Card program banking | Phase 4 |
| Fintech attorney | §162 vs §170, round-up structure, commercial co-venture | Before Phase 1 money moves |
| CPA / tax advisor | Charitable deduction characterization, points liability | Before Phase 1 money moves |
| Robotica AI / Tilmon | OTIS video intelligence for foundation impact measurement | Phase 4 |

---

## Appendix C — Scripture Index

| Passage | Principle | Where Applied |
|---|---|---|
| Luke 16:10 | Faithful in little, faithful in much | Ledger transparency; closing slide of investor deck |
| Deut. 25:4 / 1 Tim. 5:18 | Don't muzzle the ox | Agent residuals permanently untouched |
| 2 Cor. 9:7 | God loves a cheerful giver | Giving is automatic, not a guilt-trip |
| Matt. 5:16 | Let your light shine | Merchant impact story and badge; merchant one-pager closing |
| Jer. 29:7 | Seek the welfare of the city | Hyper-local cause matching; foundation page closing |
| Mark 12:41-44 | The widow's mite | Equal dignity at every merchant size |
| James 1:17 | Every good and perfect gift is from above | Ecosystem strategy document closing |

---

*This document synthesizes all strategy, research, product decisions, legal landscape, and build specifications developed for TheGiveback as of July 2026. It is a living document — treat it as the north star to argue with, refine, and pressure-test with your team, your board, and whoever holds you accountable to the covenant.*

*Not legal or financial advice. Bring the §162/§170 question and the round-up DAF structure to a fintech attorney and CPA before real dollars move.*
