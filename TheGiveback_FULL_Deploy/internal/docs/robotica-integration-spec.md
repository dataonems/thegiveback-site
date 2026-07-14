# TheGiveback × Robotica AI — Integration Specification
### Measured Impact, Merchant Intelligence & Platform Moat
### Version 1.0 · July 2026 · Owner: Chris Humphrey / DataOne

---

## Table of Contents

1. [The Core Thesis](#1-the-core-thesis)
2. [Robotica AI Capability Stack — What It Can Actually Do](#2-robotica-ai-capability-stack--what-it-can-actually-do)
3. [Applications for Foundations](#3-applications-for-foundations)
4. [Applications for Merchants](#4-applications-for-merchants)
5. [Applications for Consumers](#5-applications-for-consumers)
6. [Platform Moat — Four Compounding Layers](#6-platform-moat--four-compounding-layers)
7. [The Spatial Intelligence Layer — Certified Merchant Stores](#7-the-spatial-intelligence-layer--certified-merchant-stores)
8. [TheGiveback Live × Robotica](#8-thegiveback-live--robotica)
9. [Data Architecture](#9-data-architecture)
10. [Build Sequence](#10-build-sequence)
11. [Constraints That Cannot Be Bypassed](#11-constraints-that-cannot-be-bypassed)
12. [Open Questions Before Build](#12-open-questions-before-build)
13. [Fixed Decisions for This Feature](#13-fixed-decisions-for-this-feature)

---

## 1. The Core Thesis

Every giving platform in the world has the same credibility problem: donors give money, money moves to a nonprofit, the nonprofit reports what it did with the money. That report is always self-generated, always self-serving, and almost never verifiable. The state of the art in philanthropic impact measurement is a survey handed to program participants on the way out the door asking "did you find this useful?" This is not measurement. It is testimony.

**Robotica AI turns reported impact into measured impact.** Not by replacing human judgment — by instrumenting the moments where programs actually happen and extracting objective engagement signals that no survey can capture and no foundation can fabricate.

When a food pantry's nutrition education session is instrumented by OTIS, the platform no longer needs to take the foundation's word for whether 87 youth were meaningfully engaged. It can show an attendance-weighted engagement curve, a comprehension proxy score for the most content-dense segments, a drop-off analysis identifying exactly where attention degraded and what was being taught at that moment, and a composite Program Effectiveness Score that is reproducible, comparable across sessions, and auditable.

This changes everything — not just for foundation reporting, but for merchant giving decisions, consumer trust, platform defensibility, and the entire flywheel. TheGiveback becomes the first giving platform where the chain of evidence runs from payment terminal to foundation program to measured human engagement. That chain is the moat.

### What Is Being Built

Not a surveillance system. Not biometric tracking of individuals. The outputs are:
- Aggregate attention curves (collective engagement, not individual identification)
- Anonymized engagement metrics at the program level
- A Program Effectiveness Score (PES) on a standardized scale
- Visualizations suitable for merchant sharing and public reporting

The instrumentation methodology, consent framework, and data governance architecture are as important as the technology itself. See Section 11.

---

## 2. Robotica AI Capability Stack — What It Can Actually Do

Understanding the three layers precisely matters for knowing which applications are ready now and which require more development.

### Layer 1 — OTIS Video Intelligence (Commercial Wedge — Closest to Deployment)

Real-time and post-hoc analysis of video content to extract structured engagement data:
- **Attention signals**: face orientation, gaze direction, body posture — individually anonymous, collectively meaningful
- **Drop-off curves**: when does collective attention decline, and at what rate
- **Emotional response proxies**: engagement states inferred from non-verbal cues
- **Session timeline mapping**: attention correlated against program content timeline

Originally built for podcast and content creators (a podcaster sees where listeners disengage and what was being said at that moment). The underlying signal-extraction is domain-agnostic — it works equally well on a financial literacy workshop, a mentorship session, a cooking class, or a live music show.

**What this is ready for today:** Foundation program instrumentation, TheGiveback Live show engagement analytics, content creator tools for artists in the live events module.

### Layer 2 — Computer Vision Infrastructure (Physical Space — Tilmon's Deeper Stack)

A more powerful and more sensitive layer built for physical-space analysis at scale:
- **Crowd density analysis**: how many people, where, how that changes over time
- **Demographic inference**: aggregate demographic patterns (not individual identification)
- **Gaze / line-of-sight tracking**: what do people look at in a physical space
- **Proprietary grid-based per-cell inference**: spatial precision — analysis broken down by location zones within a space
- **Millisecond-level temporal event tracking**: precise timing of behavioral changes
- **Ensemble quorum voting across models**: multiple CV models checked against each other for high-confidence classification — reduces false positives

Currently being positioned toward public safety / smart cities applications in Colombia via DVBE Technology Group. The same stack, applied to a certified merchant's retail space, becomes a merchandising and customer experience intelligence tool.

**What this is ready for:** Spatial analytics for certified merchant storefronts (Phase 5), foundation program physical-space analysis (Phase 4), live event venue analysis (Phase 4-5).

### Layer 3 — Biometric Signals (Early Stage — Most Sensitive)

Smartwatch and wearable integration for physiological response data:
- **Heart rate variance (HRV)**: a validated marker of cognitive engagement and stress
- **Stress signal detection**: physiological distress indicators
- **Physiological corroboration**: used alongside visual signals to confirm engagement states that gaze and posture alone cannot classify with confidence

This layer is the most powerful and the most legally sensitive. A youth mentorship program where participants wear fitness trackers can yield HRV data corroborating whether the mentorship session produced genuine engagement or merely physical presence. An addiction recovery program where HRV spikes indicate stress can identify which program elements are triggering rather than therapeutic.

**What this is ready for:** High-stakes program categories in Phase 5 with dedicated consent frameworks and clinical guidance. Not Phase 3 or 4. Not without explicit legal and clinical review.

---

## 3. Applications for Foundations

### 3.1 The OTIS Program Report — Impact Measurement as a Service

**The problem it solves:** Foundations currently report impact using activity metrics (attendance counts) and self-reported outcomes (participant surveys). These are the same for a program that transformed lives and one that wasted everyone's time. Nobody can tell them apart from the outside. OTIS can.

**What gets built:**

A standardized impact document generated automatically from OTIS instrumentation of a foundation's program session. Delivered to the foundation through the Givehub portal and surfaced on their TheGiveback public impact page.

```
PROGRAM EFFECTIVENESS REPORT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Foundation:      Midtown Food Pantry
Program:         Friday Nutrition Education Session
Date:            June 14, 2026
Participants:    43
Duration:        52 minutes

PROGRAM EFFECTIVENESS SCORE (PES):  84 / 100

ENGAGEMENT CURVE
100%│    ╭──────────────╮
    │   ╱               ╲
 80%│──╱─────────────────╲────────────────────
    │                     ╲          ╭───────
 60%│                      ╲        ╱
    │                       ╲──────╱
 40%│
    └─────────────────────────────────────────
    0        10        20        30       52min

KEY MOMENTS
  Min 8:   Topic shift to meal planning — attention +22%
  Min 19:  Sustained peak (94% engagement) — core content
  Min 34:  Drop-off begins — topic: reading nutrition labels
  Min 41:  Recovery — hands-on activity introduced (+18%)

PROGRAM BENCHMARKS (vs. similar programs in network)
  Sustained engagement (>60%):     41 of 52 minutes  (79%)
  Peak engagement:                 94%
  Category median PES:             71
  This program:                    +13 above median

METHODOLOGY NOTE
Aggregate attention signals derived from anonymized video
analysis. No individual identification. Participants
provided written consent. Data retained 24 months.
```

**Delivery:** Report generated within 24 hours of session. Foundation reviews before it publishes. Foundation can annotate the report with their own context ("the drop-off at minute 34 is expected — that's when we introduce the homework assignment").

**Who funds it:** TheGiveback pays for OTIS instrumentation from the giving-program margin — foundations do not pay. This is structured as a benefit of Verified Foundation Partner status in the network. Suggested allocation: a flat fee per session funded from a designated percentage of each foundation's monthly disbursement (e.g., up to 5% of the disbursement amount, capped at $200/session), drawn from DataOne's program overhead rather than from the foundation's spendable disbursement.

### 3.2 Foundation Qualification by Measured Effectiveness

Today, the TheGiveback vetting standard qualifies foundations on:
- 501(c)(3) status in good standing
- Financial health (990 review, overhead ratios)
- Mission alignment
- Leadership conversation

OTIS adds a fourth dimension: **demonstrated program effectiveness**.

After a foundation's first instrumented session, they receive an initial PES. After three sessions, they receive a rolling PES that represents their baseline program quality. This score becomes part of their foundation profile, visible to merchants who choose to review it.

This creates a qualification tier no competitor marketplace can replicate:

| Tier | Qualification | Merchant Routing Option |
|---|---|---|
| Foundation Partner | Financial + mission + leadership | Standard certified merchant giving |
| Verified Foundation Partner | Financial + mission + leadership + 1+ OTIS sessions completed | Eligible for Verified Impact badge on merchant |
| High-Impact Foundation Partner | All above + PES ≥ 75 across 3+ sessions | Eligible for "High-Impact" merchant giving tier |

The PES score is not a ranking or a competition between foundations. It is a quality floor that foundations can improve over time, with OTIS data helping them understand exactly where to improve. The drop-off at minute 34 in the report above is not a judgment — it is actionable intelligence that tells the program director "your hands-on activity in minute 41 saved the session; consider moving it earlier."

### 3.3 Foundation Forecasting Enhanced by Program Data

The existing AI forecasting layer gives foundations a 90-day rolling estimate of expected disbursements. OTIS adds a second dimension: program capacity planning.

A foundation that knows it will receive $2,400 in the next 30 days can plan programs accordingly. A foundation that also knows its Friday session averages 43 participants at 84 PES can calculate optimal session frequency and staffing ratios. Combined: "You have $2,400 coming in. Based on your session data, you can run 3 sessions efficiently at your current staffing, serving approximately 129 participants at your historical engagement level."

This is operational intelligence that most nonprofit executive directors have never had access to. It comes from the combination of DataOne's financial forecasting and Robotica's engagement measurement. Neither alone provides this. Together they give a small foundation the planning infrastructure of a much larger organization.

### 3.4 The Sector Benchmark Report (Phase 5 Data Product)

Once enough foundations have been instrumented — the threshold is approximately 50 sessions across 20 foundations across multiple program categories — the aggregate dataset becomes publishable.

TheGiveback publishes an annual Sector Impact Benchmark Report: median PES scores by program category, engagement curve patterns by intervention type, drop-off signatures that predict low-outcome sessions before they complete. This is research that has never existed because the data has never been collected objectively.

This report is:
- A fundraising asset for every foundation in the network ("our program scores above the median")
- A program design resource for foundations trying to improve
- A donor intelligence tool for major donors and institutional funders who want evidence before giving
- A public asset that establishes TheGiveback as a research institution, not just a giving platform

That last point is permanent and irreversible. The day TheGiveback publishes independent, objective research on nonprofit program effectiveness is the day it becomes impossible to characterize as a payments company that happens to give away margin. It becomes a civic infrastructure organization. That transition is worth more than any single product feature.

---

## 4. Applications for Merchants

### 4.1 The Verified Impact Badge

The Giveback Certified designation currently signals: "this merchant's transactions fund vetted local causes." The Verified Impact badge signals something categorically stronger: "the program this merchant's transactions fund has been independently measured and found to be effective."

Not all merchants care about this distinction initially. But the merchants who do — faith-based business owners, values-driven proprietors, merchants with strong community ties — care about it deeply. For them, the difference between "we give to charity" and "we fund programs that work, and here is the evidence they work" is the difference between cause marketing and genuine ministry.

The Verified Impact badge appears:
- On the merchant's Giveback Certified storefront in the marketplace
- In the consumer app merchant listing
- In the merchant's shareable badge kit (window decal, web embed)
- On the merchant's monthly impact post

Visual distinction: the standard Giveback Certified badge is green. The Verified Impact badge is green with a measurement icon — a small waveform or engagement curve symbol that signals "this has been measured."

### 4.2 OTIS-Generated Content for Merchant Social Sharing

The existing AI-generated monthly impact post converts "$412 given" into a shareable Instagram caption. OTIS generates a second category of content that the AI cannot produce alone: **evidence visualizations**.

**The Engagement Curve Card:** A 1080×1080 image (Instagram-optimized) showing the foundation's engagement curve from their most recent OTIS-instrumented session, branded with the merchant's name. Not the faces of participants. The aggregate attention signal — a wave that shows a room of people engaging with an educator. Caption: "This is what your haircuts did last month. 94% of participants were fully engaged during the most important part of the session. Your transactions made that room happen."

**The 15-Second Reel:** An animated version of the engagement curve building in real time, with the program timeline annotated. Designed for Instagram Reels and TikTok. No faces, no identifying information — just the visualization of collective human engagement with the text of what was being taught at each moment.

**The Impact Stat Card:** A single statistic from the OTIS report formatted as a shareable graphic. "73% sustained engagement. 43 participants. Your neighborhood showed up." These are the specific, honest, verifiable numbers the platform has always promised — now backed by objective measurement rather than self-report.

Merchants receive these assets in their dashboard alongside the standard monthly impact post. They can share any or all of them. The content library for a Verified Impact merchant is meaningfully richer than for a standard certified merchant — creating a tangible incentive to route giving to Verified High-Impact foundations.

### 4.3 The High-Impact Giving Tier

Merchants who want more control over their giving destination can opt into the High-Impact giving tier:

```
GIVING TIER SELECTION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
○ Standard Certified  — Hyper-local causes matched to your
                        community. Vetted for financial
                        health and mission alignment.

● Verified Impact     — Same as above, but only foundations
                        with active OTIS program measurement
                        and a PES score on file.
                        [Verified Impact badge included]

○ High-Impact Tier    — Only foundations with PES ≥ 75
                        across 3+ instrumented sessions.
                        Highest-quality verified programs only.
                        [High-Impact badge included]
```

This is a meaningful choice, not a marketing veneer. The PES score is objective. The routing is automatic. A merchant who selects High-Impact tier knows that every cent of their covenant giving goes to programs that have demonstrably engaged their participants. No other giving platform can offer this choice because no other platform has the measurement infrastructure.

### 4.4 Merchant Program Sponsorship

A natural extension of the High-Impact giving tier: merchants can sponsor specific OTIS-instrumented program sessions directly.

"Miller's Hardware is sponsoring Friday's nutrition education session at Midtown Food Pantry."

The merchant's name appears in the pre-session announcement to participants (with full transparency that they are a certified merchant funder). Post-session, the merchant receives the OTIS report from that specific session — not just aggregate monthly data. The merchant can share the engagement curve from "their" session specifically.

This creates a named, personal connection between the merchant and the specific program their business funded — the spiritual equivalent of building a well in a village and seeing the village use it, rather than donating to a water charity and receiving an annual letter.

Program sponsorship is funded from the merchant's existing covenant giving — it is a routing decision, not an additional cost. The merchant doesn't give more; they give more specifically.

---

## 5. Applications for Consumers

### 5.1 The Verified Impact Chain in My Impact Tab

The consumer's My Impact tab currently shows a giving journal: "Your purchase at Miller's Hardware contributed $0.43 to Midtown Food Pantry." With OTIS, that entry links forward to the measured outcome.

```
MY IMPACT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Miller's Hardware  ·  June
Your purchase contributed to Midtown Food Pantry.

Miller's total this month: $412 → 91 meals funded
Program Effectiveness Score: 84 ✓ Verified

[See what 84 means →]  [I witness this]  [I was there ✓]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

Tapping "See what 84 means" opens the foundation's most recent OTIS Program Report — the engagement curve, the key moments, the comparison to sector benchmarks. The consumer who spent $40 at a barbershop can trace that money all the way to a room of people fully engaged with a nutrition educator, with an objective score certifying that engagement was real.

This is the transparency promise at the deepest level it can currently be delivered. No other giving platform in the world offers this chain of evidence. Not Benevity. Not Causecast. Not any donor-advised fund. The chain runs from point-of-sale terminal to ledger entry to disbursement to OTIS-instrumented program session to measured engagement score — and every link is verifiable.

### 5.2 Impact Score as a Foundation Selection Tool for Consumers

In Phase 4, consumers who have Giveback Points to donate can sort and filter foundations by Program Effectiveness Score when choosing where to direct their points.

"I want to donate my points to a youth mentorship program with a PES above 75."

This is the first time a consumer has ever been able to make a giving decision based on objective program quality rather than marketing copy or a Charity Navigator overhead ratio. It respects the consumer's giving intent at a level of precision that has not previously been possible.

### 5.3 TheGiveback Live — Artist and Show Engagement Analytics

When a consumer watches a TheGiveback Live show, OTIS generates engagement analytics for that specific performance (from the video stream, not from viewer devices). After the show, viewers can see:

- When during the show was collective engagement highest
- Which song or moment produced the biggest viewer response
- How the giving meter correlated with engagement peaks (high-engagement moments tend to generate more tips)

This is presented to viewers as a "show story" — not as surveillance data but as the artistic record of what happened in that virtual room during that show. It reinforces the uniqueness of live events (each show has its own engagement signature) and gives artists data they cannot get from any other platform.

---

## 6. Platform Moat — Four Compounding Layers

These four moats are listed in order from shallowest (soonest to build, earliest competition possible) to deepest (takes longest to build, hardest to replicate).

### Moat 1 — Data Moat (Builds from Phase 4)

Every OTIS-instrumented program session generates a data point. The dataset compounds:

| Sessions | Foundations | Data Asset |
|---|---|---|
| 50 | 20 | First Program Effectiveness benchmarks by category |
| 200 | 60 | Statistically significant sector baselines |
| 500 | 150 | Publishable research on nonprofit program effectiveness |
| 1,000+ | 250+ | The only independent, objective dataset of its kind in the world |

This dataset does not exist anywhere. Benevity and Causecast have transaction data. Charity Navigator has financial ratios. Nobody has measured engagement data across foundation programs at scale. TheGiveback will.

The dataset is:
- A competitive intelligence asset (foundations that score above median can prove it)
- A fundraising tool for major donors and institutional funders wanting evidence
- A publishable research asset establishing TheGiveback as a civic institution
- Eventually a licensed data product for academic researchers, government funders, and corporate CSR programs

The moat depth: a competitor who starts building today needs 3–5 years of instrumented sessions to have a dataset comparable to TheGiveback's. The dataset lead is permanent for anyone who starts now.

### Moat 2 — Foundation Qualification Moat (Builds from Phase 4)

Today every giving marketplace qualifies foundations on financial governance — overhead ratios, audit findings, 501(c)(3) status. This is necessary but not sufficient. It tells you the organization is honest; it tells you nothing about whether the program works.

TheGiveback adds the dimension nobody else has: demonstrated program effectiveness as measured objectively. A foundation marketplace that qualifies on financial governance AND measured impact attracts categorically better foundations — those confident enough in their program quality to submit to measurement.

Foundations that are admitted to the Verified Foundation Partner tier have self-selected for quality. Foundations that would fail OTIS measurement don't apply. The marketplace becomes self-curating in a way that financial-governance-only vetting never achieves.

This qualification moat reinforces the data moat: better foundations produce better engagement data, which produces better benchmarks, which attracts more quality foundations to a marketplace where high PES is a public credential.

### Moat 3 — Merchant Retention Moat (Builds from Phase 4)

Payment processing is a commodity. Merchants switch processors when rates are better by a few basis points. The OTIS layer changes this calculus fundamentally.

A merchant who has:
- Three OTIS Program Reports showing impact from their giving
- A Verified Impact badge on their storefront and in their window
- An engagement curve card shared to their Instagram that their community engaged with
- A "I sponsored this session" story from the Friday nutrition class their business funded
- A named personal connection to a specific program participant cohort

— does not switch processors over 10 basis points.

The OTIS layer creates operational and emotional attachment to the platform that no competitor can purchase or replicate. The merchant who switches loses not just their badge but their entire verified impact story. That story does not transfer. It lives on TheGiveback's ledger and in TheGiveback's OTIS report archive, not on the merchant's hard drive.

Quantifying the moat: if the Verified Impact badge and OTIS content reduces merchant churn by 5 percentage points annually (a conservative estimate for a feature this differentiated), and the average certified merchant generates $21,765/year in giving (at $1M monthly volume), the retention value is roughly $1,088 per merchant per year in giving preserved — not counting the continued processing margin on their volume.

### Moat 4 — Spatial Intelligence Moat (Phase 5 — Deepest)

This is the application the original Robotica document does not fully develop. It is potentially the most powerful long-term moat because it embeds Robotica's technology directly into the certified merchant's physical business operations — not just their giving story.

Layer 2 of the Robotica stack — crowd density analysis, gaze tracking, spatial precision, temporal event tracking — was built for smart cities. The same technology applied to a certified merchant's retail space becomes a merchandising and customer experience intelligence tool available previously only to large retailers with tens of millions in technology budgets.

**What a small certified merchant learns from spatial analytics:**
- Which areas of their store customers naturally move toward (aggregate heatmap, no individual tracking)
- What customers look at and for how long (gaze attention zones)
- How dwell time in specific product areas correlates with transaction size
- When in the customer journey (entrance → browse → register) engagement drops
- How store layout changes affect these patterns over time

Walmart pays tens of millions for this. Target has entire teams dedicated to retail spatial analytics. For a barbershop, hardware store, or independent restaurant in the TheGiveback network, this capability arrives as a benefit of certification — funded from the platform's margin, not the merchant's budget.

Full section on spatial analytics is in Section 7 below.

---

## 7. The Spatial Intelligence Layer — Certified Merchant Stores

### What It Is

A lightweight hardware-and-software package installed in certified merchant locations that uses the Robotica Layer 2 computer vision stack to generate anonymous aggregate analytics about customer behavior in the physical space.

This is not surveillance. No individuals are identified. No faces are stored. The output is heatmaps, attention zones, dwell-time distributions, and traffic flow patterns — aggregate data that tells the merchant how customers experience their store, not who those customers are.

### Hardware

**Option A — Camera-based (existing infrastructure):**
If the merchant already has security cameras, the Robotica Layer 2 stack can process the existing feed. No new hardware. Edge processing (on a small local device) means no raw video leaves the store.

**Option B — Sensor array:**
A small set of depth sensors (LiDAR or structured light) that detect human presence and movement without capturing visual images. Less data-rich than camera-based but lower privacy sensitivity and simpler consent framework.

For Phase 5 pilot: start with Option A for merchants who already have cameras and are comfortable with the consent framework. Option B for merchants who want the analytics but have concerns about camera-based systems.

### What Gets Measured

| Metric | Description | Merchant Value |
|---|---|---|
| Traffic flow map | How customers move through the space | Identify dead zones, optimize layout |
| Attention heatmap | Which areas customers look at | Product placement, signage positioning |
| Dwell time by zone | How long customers spend in each area | Identify high-interest and low-interest zones |
| Conversion correlation | Dwell time vs. purchase behavior | Which browsing behaviors predict purchases |
| Peak traffic timing | When is the store most active by zone | Staffing, inventory, and promotion timing |
| Session journey | Entry → browse → purchase path | Remove friction from the customer journey |

### What Does Not Get Measured

- Individual identification of any kind
- Face recognition
- Demographic inference at the individual level (aggregate only, no individual profiling)
- Any data that links to a specific customer's purchase history

The consent framework (see Section 11) requires clear in-store signage that spatial analytics are in use. Customers can decline by staying in the signposted opt-out zone near the entrance. No purchase is denied to anyone who opts out.

### The Dashboard

Inside the merchant's existing TheGiveback dashboard, a new "Store Intelligence" tab:

```
STORE INTELLIGENCE  ·  Miller's Hardware  ·  June 2026
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TRAFFIC FLOW                        ATTENTION HEATMAP
[Store map with flow arrows]        [Store map with heat zones]
                                    🔴 High   🟡 Medium   🟢 Low

TOP PERFORMING ZONES                OPPORTUNITY ZONES
1. Power tools aisle    4.2min      1. Back wall display    0.8min
2. Checkout area        2.1min      2. Seasonal end-cap     0.6min
3. Paint section        3.8min      3. Service counter      1.1min

INSIGHT THIS MONTH
Customers who spend 3+ minutes in the paint section convert
at 2.1× the store average. Consider moving related accessories
(brushes, rollers, tape) into an adjacent display.

COMPARING TO LAST MONTH
Overall dwell time:  +8%  ↑    Conversion rate:  +3%  ↑
```

### Connection to the Giving Story

Spatial intelligence is presented as a benefit of the Giveback Certified network — not as a separate product or a separate fee. The framing to merchants: "Because your transactions fund verified community programs, and because we want to help your business thrive so those programs are funded for years to come, we give you the tools to run a better store."

This framing is honest and it serves the mission. A merchant whose store performs better generates more transactions, which generates more giving, which funds more programs. The spatial intelligence layer directly serves the foundation's interests even though it appears to serve only the merchant.

---

## 8. TheGiveback Live × Robotica

### Show Engagement Analytics for Artists

When a TheGiveback Live show is processed through OTIS, the artist receives a post-show engagement report analogous to the foundation's program report:

```
SHOW ENGAGEMENT REPORT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Artist:         Sarah J
Show:           Friday Night Live at Miller's Hardware
Date:           June 14, 2026
Peak Viewers:   247  ·  Avg Concurrent: 183

ENGAGEMENT CURVE
100%│         ╭─────────────╮
    │        ╱               ╲
 80%│───────╱─────────────────╲─────────────
    │      ╱                   ╲    ╭──────
 60%│─────╱                     ╲──╱
    │
 40%│
    └─────────────────────────────────────
    0       20       40       60       90min

PEAK MOMENTS
  Song 3 — "Hollow Ground":    peak viewer engagement (94%)
  Song 7 — "River Running":    second peak, most tips received
  Min 62 — "I'll be right back": largest drop-off (-31%)

GIVING CORRELATION
High-engagement songs generated 3.1× more tips on average.
Songs with sustained >80% engagement: 4 of 11 performed.

YOUR HIGHEST-IMPACT MOMENT
"Hollow Ground" (min 18–22): 94% engagement, $47 in tips.
Consider opening future sets with this song.
```

This is data no artist has ever had from any platform. StageIt shows a tip total. Twitch shows viewer count. OTIS shows the engagement signature of a specific performance — which songs held attention, when the room was in the palm of your hand, when you lost it, and how that correlated with giving behavior.

For a career musician trying to understand what connects with audiences, this is transformative. For an independent artist building a community show series on TheGiveback Live, it is the intelligence layer that turns guesswork into craft.

### Foundation Show Instrumentation

When a TheGiveback Live show specifically benefits a foundation with Verified Foundation Partner status, the foundation can optionally receive the engagement analytics from that show's audience. Not viewer identification — aggregate engagement data showing how the audience responded to the foundation's mission being discussed during the show.

Example: an artist who uses their TheGiveback Live set to briefly introduce the benefiting foundation at minute 15 can see the engagement spike (or dip) when they do so. This tells the foundation whether their mission narrative resonates with the merchant's customer community. Actionable intelligence for their own communications strategy.

### Live Show PES for Recurring Series

For merchants running recurring show series (Format 4 — subscription model), OTIS generates a cumulative Show Series Effectiveness Score — the equivalent of a foundation's Program Effectiveness Score for the live events themselves. This answers: is this recurring show building community engagement over time, or is it declining?

Factors in the score:
- Viewer retention across the series (are the same people coming back?)
- Average engagement per show
- Giving behavior trend (are tips increasing per viewer session?)
- Community layer engagement after shows (are "I witness this" and "I was there" rates growing?)

A merchant whose Friday night series has a growing Show Series Score gets a feature placement in the Moments tab of the consumer app — not as a paid promotion but as evidence-based curation. The highest-engagement recurring shows surface first because they demonstrate genuine community value.

---

## 9. Data Architecture

### New Tables

#### `otis_sessions`
```
id, entity_type (foundation_program|live_show|merchant_store),
entity_id, session_date, duration_seconds, participant_count,
pes_score (0-100, nullable until calculated), status (pending|processing|complete),
report_url, published_at, consent_verified_at, created_at
```

#### `otis_engagement_curves`
*Append-only. One row per time bucket per session.*
```
id, session_id, time_bucket_seconds (e.g. 60-second intervals),
engagement_level (0.0-1.0), participant_count_in_bucket,
annotation (nullable — "meal planning discussion", "song: Hollow Ground"),
created_at
```

#### `otis_key_moments`
```
id, session_id, moment_type (peak|drop|recovery|sustained),
time_seconds, engagement_delta (positive = increase, negative = decrease),
annotation, significance_score (0-100), created_at
```

#### `foundation_pes_history`
```
id, foundation_id, session_id, pes_score, program_category,
participant_count, session_date, cumulative_sessions_count,
rolling_pes_3session (calculated), created_at
```

#### `merchant_spatial_sessions`
*Separate schema — stricter access controls*
```
id, merchant_id, session_date, duration_hours, peak_visitor_count,
zones_json (aggregate zone data — no individual records),
insight_generated_at, consent_signage_verified, created_at
```

#### `merchant_spatial_zones`
```
id, merchant_id, zone_name, zone_polygon_json (physical coordinates),
avg_dwell_seconds, avg_attention_score, traffic_rank, created_at
```

#### `otis_content_assets`
*Generated visualizations for sharing*
```
id, session_id, asset_type (engagement_curve_card|animated_reel|stat_card|show_report),
generated_for (foundation|merchant|artist|consumer),
asset_url, thumbnail_url, share_caption_text, created_at
```

### Privacy Architecture

All OTIS data storage follows strict privacy-by-design principles:

- **No individual identification** — no faces stored, no biometric templates, only aggregate signals
- **Edge processing first** — raw video is processed at the source; only the extracted signals (engagement percentages, attention vectors) are transmitted to the platform. Raw video does not leave the site.
- **Retention limits** — raw signals retained 24 months, then purged. Aggregate scores (PES, engagement curves) retained indefinitely as they are non-personal.
- **Access controls** — foundation program data accessible only to: the foundation itself, TheGiveback admins with audit access, and the merchants who directly funded that session. Not to other foundations, not to the general public (only the PES score and general curve are public-facing, not the granular data).
- **Spatial data** — merchant spatial data accessible only to that merchant and TheGiveback admins. No cross-merchant comparison without explicit merchant consent to benchmarking program.

---

## 10. Build Sequence

### Phase 3 — Legal and Partnership Foundation (Months 5–8)

*No build yet. Resolve every prerequisite.*

- [ ] IP review with Derek Young — deal structure, carve-out between commercial (OTIS/DataOne) and defense (DVBE) use cases
- [ ] Consent framework legal review — separate from IP, focused specifically on consent requirements for program participants (especially minors and vulnerable populations)
- [ ] Identify pilot foundation — must be willing to instrument 3 real sessions and share results honestly
- [ ] Define OTIS funding model — flat fee per session OR % of disbursement, drawn from DataOne giving-program overhead (not from foundation's spendable disbursement)
- [ ] Document minimum viable PES methodology — what constitutes a valid session, what sample sizes are needed for statistical confidence

### Phase 4 — Pilot and Foundation Integration (Months 9–14)

*One real pilot. Prove the technology before any public claim.*

- [ ] Run first pilot OTIS session at pilot foundation — do not publicize
- [ ] Validate PES methodology against human observer assessment
- [ ] Generate first OTIS Program Report — review with foundation before any publication
- [ ] If pilot validates: integrate PES score into foundation portal (Givehub) and TheGiveback public impact pages
- [ ] Launch Verified Foundation Partner tier
- [ ] Launch Verified Impact badge for merchants whose matched foundations have active OTIS instrumentation
- [ ] Launch High-Impact giving tier for merchants who want PES-gated routing
- [ ] Generate first OTIS content assets for merchant social sharing (engagement curve cards)
- [ ] Begin building aggregate dataset (target: 50 sessions across 20 foundations before any public sector benchmarks)

### Phase 4 — TheGiveback Live Integration (Months 12–16)

*After standalone foundation OTIS is stable*

- [ ] OTIS integration with live show video stream via Mux/Cloudflare webhook
- [ ] Post-show engagement report for artists
- [ ] Show engagement correlation with tip behavior
- [ ] Consumer-facing "show story" in post-show recap screen
- [ ] Show Series Effectiveness Score for recurring series
- [ ] Moments tab curation by engagement evidence (no paid promotion)

### Phase 5 — Spatial Intelligence (Months 18–24)

*After OTIS foundation and live integrations are stable and legally validated*

- [ ] Dedicated legal review for in-store spatial analytics — consent signage requirements, opt-out mechanics, jurisdiction-specific rules
- [ ] Hardware pilot: 3–5 volunteer certified merchants (camera-based, existing infrastructure)
- [ ] Spatial analytics dashboard MVP: traffic flow map, attention heatmap, dwell time by zone
- [ ] Insight generation layer: AI-written recommendations based on spatial patterns
- [ ] Giving correlation: surface the connection between store performance and giving capacity
- [ ] Expand to sensor-based option (Option B) for merchants with camera concerns

### Phase 5 — Sector Benchmark Report (Month 24+)

*Only after sufficient data — do not rush*

- [ ] Minimum 50 sessions, 20 foundations, 5+ program categories before first report
- [ ] Academic or third-party review of methodology before publication
- [ ] Annual publication cadence
- [ ] Position as a public resource, not a TheGiveback marketing asset

---

## 11. Constraints That Cannot Be Bypassed

These are not suggestions. Every one of these must be resolved before any OTIS capability is deployed at any site.

### Constraint 1 — IP Structure Must Be Resolved First

The OTIS technology has active conversations in the DVBE/defense context via the Colombia partnership. Before any commercial deployment of the same technology stack for TheGiveback, Derek Young must review and formally document:
- What IP is being licensed to TheGiveback vs. owned jointly vs. remaining solely with Robotica
- How the commercial (TheGiveback) and defense (DVBE) use cases are legally separated
- What happens if the defense application advances in ways that create conflict with the commercial deployment

**Do not build until this is documented in writing.**

### Constraint 2 — Consent Framework Is Non-Negotiable

Using visual intelligence on program participants requires explicit, informed consent. The consent framework must address:
- Clear pre-session disclosure of what is being measured and why
- Written or documented verbal consent from participants (verbal for one-time sessions if documented; written for recurring programs)
- Special provisions for minors — parental or guardian consent required, not optional
- Special provisions for vulnerable populations (addiction recovery, mental health programs, trauma-informed care) — clinical guidance alongside legal guidance before any biometric (Layer 3) deployment in these contexts
- Right to withdraw consent mid-session without consequence
- Data retention and deletion rights

**The biometric layer (Layer 3 — HRV, stress signals) does not deploy in any program serving minors or vulnerable populations without explicit clinical guidance. This is not a Phase 3, 4, or 5 consideration. It is a separate workstream with its own timeline.**

### Constraint 3 — Pilot Before Public Claim

The first OTIS program report is reviewed by the foundation and the TheGiveback team before any public-facing claim about "measured impact" is made. If the pilot reveals the technology underperforms, overclaims, or produces results inconsistent with human observer assessment, the public claims are adjusted accordingly. The word "measured" appears in no marketing material, no investor deck, and no foundation application until at least one real pilot has been completed and validated.

### Constraint 4 — Foundations Do Not Pay

OTIS instrumentation is funded entirely from DataOne's giving-program overhead. Under no circumstances does the cost of instrumentation reduce the foundation's disbursable funds. The mechanism:
- Dedicated line in DataOne's giving-program budget: "OTIS instrumentation fund"
- Funded at a percentage of total disbursements (suggested: 3–5% of total giving-program overhead, not of individual foundation disbursements)
- Cap per session: established before Phase 4 launch based on Robotica's per-session pricing

### Constraint 5 — Spatial Analytics Require Separate Legal Review

In-store customer analytics is a materially different legal context from foundation program instrumentation. CCPA, state biometric privacy laws (Illinois BIPA, Texas CUBI, Washington My Health MY Data), and sector-specific regulations apply differently to retail environments than to nonprofit program settings. The consent framework for spatial analytics is separate from the consent framework for program instrumentation. Do not assume one covers the other.

---

## 12. Open Questions Before Build

From the original Robotica document, unresolved:

1. **Which foundation(s) in the DataOne marketplace would be the right pilot candidate for OTIS instrumentation?** Criteria: willing to be measured honestly, runs structured programs (not just services), has leadership who understands what the data will and won't show, ideally serves an adult population for the first pilot (simplifies consent).

2. **What is the minimum viable version of "measured impact" that can be shown to funders before the full CV stack is deployed?** OTIS Layer 1 alone (video engagement analysis) may be sufficient for the pilot. Layer 2 (spatial precision, crowd density) can be added in Phase 5 for the merchant store application.

3. **How does the OTIS funding model work precisely?** Flat fee per session (e.g., $150/session regardless of foundation size) OR percentage of disbursement (e.g., up to $150/session or 5% of disbursement, whichever is less). Recommend flat fee — cleaner accounting, no incentive to instrument larger disbursements over smaller ones (widow's mite principle).

4. **Does the consent/data governance review happen before or in parallel with the IP review with Derek?** In parallel — they address different questions and neither blocks the other. But both must be complete before any instrumentation at a real program site.

5. **What is Tilmon's capacity for Phase 4 instrumentation sessions?** Is OTIS currently able to process sessions asynchronously (upload after the fact) or does it require a live connection? This affects what equipment foundations need during sessions and what the operational overhead is.

---

## 13. Fixed Decisions for This Feature

| Decision | Rationale |
|---|---|
| IP structure reviewed by Derek Young before any build | The DVBE/defense context creates conflict-of-use risk that must be formally documented |
| Separate consent framework for program instrumentation vs. spatial analytics | Different legal contexts, different requirements, cannot be bundled |
| Biometric Layer 3 not deployed in programs serving minors or vulnerable populations without clinical guidance | The sensitivity of physiological data in therapeutic contexts requires clinical expertise alongside legal review |
| Foundations do not pay for OTIS instrumentation | Nonprofits have no tech budget. Charging them would exclude the foundations most in need of impact measurement tools. |
| No public "measured impact" claim before pilot validation | Intellectual honesty is the entire point. A false claim about measurement is worse than no measurement. |
| OTIS content assets show aggregate signals only — no individual identification, no faces, no biometric templates in any output | Privacy-by-design. The outputs are program-level and session-level, never individual-level. |
| Sector benchmark report not published until 50+ sessions, 20+ foundations, 5+ program categories | Statistical validity requires sufficient sample size. Early publication with insufficient data would produce misleading benchmarks that could harm foundations. |
| Spatial analytics are a Phase 5 workstream with their own dedicated legal review | Do not accelerate spatial into Phase 4 because foundation instrumentation is going well. They are separate tracks with separate legal requirements. |
| Merchants route to Verified High-Impact foundations by choice, not by default | The giving tier selection is a merchant decision. Default remains hyper-local cause matching. High-Impact routing is opt-in for merchants who want it. |
| OTIS Show Series Score drives Moments tab curation — no paid promotion | Evidence-based curation serves consumers. Paid promotion would corrupt the feed the same way paid placement in any other feed corrupts user trust. |

---

*This document is an addendum to TheGiveback Complete Product & Strategy Document (v1.0) and should be read alongside the Robotica AI × DataOne Giving Program — Strategic Synergy document (pre-build brainstorm). All risks identified in the original Robotica document remain open until formally resolved. Do not treat this specification as a green light — treat it as the roadmap to get to a green light by resolving the listed constraints in the correct order.*
