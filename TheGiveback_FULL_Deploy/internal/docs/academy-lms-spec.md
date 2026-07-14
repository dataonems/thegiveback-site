# TheGiveback Academy — Learning Management System
### Kingdom Entrepreneurship · Modern Skills · English Access
### Feature Specification for Product Engineers
### Version 1.0 · July 2026 · Owner: Chris Humphrey / DataOne

---

## Table of Contents

1. [The Vision & Why This Changes Everything](#1-the-vision--why-this-changes-everything)
2. [Build vs. License Decision](#2-build-vs-license-decision)
3. [The Five Learning Tracks](#3-the-five-learning-tracks)
4. [Access Model & Pricing Architecture](#4-access-model--pricing-architecture)
5. [Content Strategy — License vs. Create](#5-content-strategy--license-vs-create)
6. [The English Access Track — Design Philosophy](#6-the-english-access-track--design-philosophy)
7. [Virtual & Live Events Layer](#7-the-virtual--live-events-layer)
8. [The Robotica AI Connection — Measuring Learning](#8-the-robotica-ai-connection--measuring-learning)
9. [Platform Integration with TheGiveback Ecosystem](#9-platform-integration-with-thegiveback-ecosystem)
10. [Data Architecture](#10-data-architecture)
11. [Technical Stack](#11-technical-stack)
12. [Build Sequence](#12-build-sequence)
13. [Content Partnerships to Pursue](#13-content-partnerships-to-pursue)
14. [Success Metrics](#14-success-metrics)
15. [Fixed Decisions for This Feature](#15-fixed-decisions-for-this-feature)

---

## 1. The Vision & Why This Changes Everything

### The Deepest Expression of the Mission

Every other feature of TheGiveback platform is about redirecting commercial activity toward good — routing margin to foundations, certifying merchants, measuring impact. All of it serves the mission by changing what happens to money that already moves.

TheGiveback Academy changes who moves the money.

A person who learns Kingdom entrepreneurship principles, builds a business, and becomes a certified merchant generates giving for their community for decades. A person who learns English opens doors to commerce, employment, communication, and opportunity that were previously closed to them. A person who learns how to use AI tools in their business multiplies their capacity to create value, hire people, and serve their community.

The Academy is not an adjacent product. It is the upstream investment that creates the merchants, the consumers, the community members, and eventually the foundations that the rest of the platform serves. Every graduate of TheGiveback Academy who builds a business is a potential certified merchant. Every certified merchant is a foundation funder. The Academy is the source of the river.

### The Two Doors

There is a profound, documented truth in the connection between English fluency and economic mobility — particularly in immigrant and underserved communities. People who combine English literacy with entrepreneurship knowledge experience a compounding effect on economic opportunity that neither alone produces:

- English alone: access to employment as an employee
- Entrepreneurship alone: business skills without market access
- English + Entrepreneurship: the ability to build, communicate, sell, negotiate, hire, and serve across the full range of the American economy

The Academy provides both doors simultaneously. This is the feature that most directly fulfills the mandate to seek the welfare of the city — not by giving money to people in need but by giving people the tools to generate their own.

### The Scripture at the Foundation

*"For the gifts and the calling of God are irrevocable."* — Romans 11:29

Every person in the Academy already has gifts. The calling is real. The Academy's job is not to give people purpose — it is to give them tools to fulfill the purpose they already carry.

---

## 2. Build vs. License Decision

### The Recommendation: License the Platform, Create the Content

Do not build an LMS from scratch. The problem you're solving is not "how do I host video courses" — it's "how do I deliver the right content to the right person at the right price in a way that connects to the rest of the TheGiveback ecosystem." Building LMS infrastructure is a solved problem. Building the content and the community around it is the unique value.

**Recommended Platform: Kajabi (white-label) for Phase 1, with migration path to custom-built LMS in Phase 4-5 if scale justifies it.**

### Why Kajabi for Phase 1

Kajabi is a business operating system, not just a course platform. It supports courses, coaching, memberships, and more from one dashboard, without requiring separate tools for email, funnels, or affiliate management.

For TheGiveback Academy's Phase 1 needs:

| Need | Kajabi Covers It |
|---|---|
| Video course hosting | ✓ Native |
| Free + paid tier access controls | ✓ Native |
| Membership / subscription model | ✓ Native |
| Email marketing to learners | ✓ Native (replaces ConvertKit) |
| Landing pages for course enrollment | ✓ Native |
| Affiliate/referral program | ✓ Native |
| Community spaces per track | ✓ Native (Communities feature) |
| Live session hosting | ✓ Native (Kajabi Live) |
| Certificate of completion | ✓ Native |
| Mobile app (white-label) | ✓ $199/month add-on |
| Multilingual content delivery | ✓ Via content in target language |

**What Kajabi does not do:**
- Deep integration with TheGiveback's ledger and giving ecosystem
- OTIS learning engagement measurement
- Giveback Points as a payment method for course access
- Merchant-linked enrollment (a certified merchant can sponsor their employee's enrollment)
- The English proficiency assessment and adaptive learning path

These gaps are Phase 3-4 build items, not Phase 1 blockers. Phase 1 launches on Kajabi. The custom integrations are built in parallel and connected progressively.

### Kajabi Pricing Context

White label LMS pricing ranges from $49/month to enterprise pricing on request. For full white labeling, most platforms require upgrading to mid-tier or enterprise plans.

Kajabi Basic plan: ~$179/month (annual). Branded mobile app add-on: $199/month. Total Phase 1 infrastructure cost: approximately $378/month — significantly less than building and maintaining custom LMS infrastructure.

### Phase 4-5 Migration Consideration

When Academy enrollment reaches 5,000+ active learners and the custom integrations (Giveback Points, ledger connection, OTIS measurement, merchant sponsorship) are proven, evaluate migrating to a custom-built LMS that natively integrates all of these. The migration decision is driven by: whether Kajabi's transaction economics become unfavorable at scale, whether the ecosystem integrations are worth the rebuild cost, and whether the Academy has become a revenue center that justifies the infrastructure investment.

---

## 3. The Five Learning Tracks

### Architecture Overview

The Academy is organized into five distinct learning tracks. A learner can enter through any track. Tracks are independent but intentionally connected — completing modules in one track unlocks bonus content in another.

```
THEGIVEBACK ACADEMY
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Track 1:  KINGDOM ENTREPRENEURSHIP
          The foundation. Who you are before what you do.

Track 2:  BUSINESS MASTERY
          The skills. How to build, run, and grow a business.

Track 3:  MODERN SKILLS
          The tools. AI, digital marketing, financial literacy.

Track 4:  LEADERSHIP & MINDSET
          The person. Maxwell, Robbins-inspired growth content.

Track 5:  ENGLISH FOR COMMERCE
          The key. Language as the door to economic participation.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Every track connects to certified merchants and foundations.
Graduates are invited to join the TheGiveback network.
```

---

### Track 1: Kingdom Entrepreneurship

**The identity and calling track. Who you are before what you do.**

This is the heart of the Academy. Everything else builds on a person's understanding of their God-given gifts, their calling as a steward of resources, and their responsibility to serve their community through commerce. Without this track, the Academy is just another business school. With it, it is formation.

**Core modules:**

| Module | Description | Length |
|---|---|---|
| Called to Create | Understanding business as a form of worship and service | 3 lessons |
| Stewardship Over Ownership | The biblical framework for resources, profit, and generosity | 4 lessons |
| Your Unique Assignment | Identifying your God-given gifts and the business that flows from them | 5 lessons |
| Building on the Rock | Why character, not strategy, determines long-term business outcomes | 4 lessons |
| Commerce as Ministry | How every business transaction is an act of service or exploitation | 3 lessons |
| The Giving Covenant | Why building a business that gives back is both scriptural and strategic | 4 lessons |
| From Employee to Entrepreneur | The identity shift required to move from wage-earning to value-creating | 5 lessons |

**Content approach:** Video-first with scripture integration that is contextual, not forced. Each module connects the Kingdom principle to a practical business decision. The tone is John Maxwell-style — accessible, story-driven, grounded in real examples, never preachy. The content challenges people to think differently, not to comply with a set of religious rules.

**Free access:** All of Track 1 is free. Giving the identity and calling content away is both the right thing to do and the best marketing. A person who completes Track 1 and experiences genuine transformation in how they think about their work is the most motivated buyer of Track 2-5.

---

### Track 2: Business Mastery

**The foundational skills track. How to build, run, and grow.**

Practical, step-by-step business education designed specifically for the small business owner who is either starting from nothing or running a business they've never formally learned to manage.

**Core modules:**

| Module | Description | Length |
|---|---|---|
| Business Plan Without Jargon | How to think through your business model in plain language | 4 lessons |
| Legal Foundations | Sole proprietor vs. LLC vs. S-Corp — what you actually need | 3 lessons |
| Banking & Bookkeeping | Opening the right accounts, tracking income and expenses simply | 4 lessons |
| Pricing Your Work | How to price based on value, not fear | 5 lessons |
| Getting Your First 10 Customers | Practical customer acquisition for a business with no marketing budget | 6 lessons |
| Managing Cash Flow | Why profitable businesses run out of money and how to prevent it | 4 lessons |
| Hiring Right | Your first hire, who it should be, and how to structure the relationship | 4 lessons |
| Sales Without Selling | How to convert conversations into customers without feeling manipulative | 5 lessons |
| Payment Processing 101 | How to accept payments, what it costs, and what to watch out for | 3 lessons |
| From Side Hustle to Business | The operational and mental shift from gig to enterprise | 4 lessons |

**The Payment Processing 101 module** is a natural, honest connection to DataOne — not a sales pitch, but a transparent education on how payment processing works, what the costs are, and what to look for in a processor. Merchants who understand payment processing make better decisions. Merchants who make better decisions often choose DataOne because of its values alignment and the certification program.

**Access:** Paid tier, included in Core Membership ($15/month). First module of each section free.

---

### Track 3: Modern Skills

**The tools track. AI, digital commerce, and 21st-century business capabilities.**

This track is the most directly tied to the disruptive technology mandate. The world is changing faster than most small business owners can track. A certified merchant who knows how to use AI tools runs a more efficient business, generates better content, serves customers better, and grows faster. This track is where that knowledge lives.

**Core modules:**

| Module | Description | Length |
|---|---|---|
| AI for Small Business | What AI actually is, what it can do today, and what it can't | 4 lessons |
| AI Writing Tools | How to write better marketing copy, emails, and social posts with AI assistance | 5 lessons |
| AI for Customer Service | Chatbots, automated responses, and when AI should never replace a human | 4 lessons |
| AI for Operations | Scheduling, inventory, bookkeeping automation — practical tools, real setup | 5 lessons |
| Building Your Digital Presence | Website, Google Business Profile, social accounts — the minimum viable digital footprint | 6 lessons |
| Social Media for Local Business | What actually works for a neighborhood business in 2026 — not influencer tactics | 5 lessons |
| E-Commerce Fundamentals | How to sell online, what platforms to use, and how to fulfill orders | 5 lessons |
| Digital Marketing on $0 | Organic strategies that work before you have a marketing budget | 6 lessons |
| Financial Literacy for Business Owners | Reading a P&L, understanding margins, knowing when your business is actually profitable | 5 lessons |
| Protecting Your Business | Insurance, contracts, basic legal protection every small business needs | 3 lessons |
| Blockchain & Payments (Intro) | What's changing in how money moves and what small businesses need to know | 3 lessons |

**Content update cadence:** This track requires quarterly content review minimum. AI tools change faster than any other content area. A module about AI that's 18 months old is dangerously outdated. Build the track with a "Last Updated" date visible on every module and a content refresh process built into operations from day one.

**Access:** Paid tier. Individual modules purchasable à la carte. Full track included in Professional Membership ($35/month).

---

### Track 4: Leadership & Mindset

**The person behind the business. Growth, resilience, and influence.**

Inspired by John Maxwell's leadership frameworks and Tony Robbins-style peak performance content — but grounded in Kingdom values rather than pure secular achievement. The person who builds a lasting, giving business is not just strategically skilled. They are emotionally resilient, relationally intelligent, and spiritually grounded.

**Core modules:**

| Module | Description | Length |
|---|---|---|
| The 5 Levels of Leadership | Adapted from Maxwell's framework for Kingdom entrepreneurs | 5 lessons |
| Influence Without Authority | How to lead people who don't have to follow you | 4 lessons |
| Decision-Making Under Pressure | How great leaders decide when the stakes are high and the information is incomplete | 4 lessons |
| Resilience Through Failure | What to do when the business doesn't go as planned | 5 lessons |
| Peak Performance Foundations | Sleep, energy management, mental clarity for entrepreneurs — Robbins-inspired | 5 lessons |
| Emotional Intelligence in Business | Why EQ matters more than IQ for small business success | 4 lessons |
| The Mentor Relationship | How to find one, how to be one, and why both matter | 3 lessons |
| Building a Team Culture | Creating a workplace where people want to do their best work | 5 lessons |
| Communicating Your Vision | How to cast a compelling story for your business that attracts customers, staff, and partners | 4 lessons |
| Generosity as a Leadership Strategy | Why the most generous leaders attract the most loyal followers | 4 lessons |

**Licensed content consideration:** This track is the strongest candidate for licensed content partnerships. Maxwell Leadership content is licensable. Robbins Research International has licensed content programs. The specific modules above can be original TheGiveback Academy content that is *inspired by* these frameworks without requiring licensing, or they can be co-branded with licensed content from partners. See Section 13.

**Access:** Core Membership tier ($15/month) or individual module purchase.

---

### Track 5: English for Commerce

**The door. Language as the entry point to economic participation.**

This track has a different design philosophy from the other four. It is not a collection of video lessons — it is an adaptive, progressive, practice-heavy learning experience designed specifically for adults who need English for business and commerce contexts, not for academic or general fluency.

Full design specification in Section 6.

---

## 4. Access Model & Pricing Architecture

### The Four Access Tiers

TheGiveback Academy is designed so that nobody is locked out of the most important content by inability to pay. The tiered model creates revenue while ensuring the content that changes lives first is always free.

```
┌─────────────────────────────────────────────────────────────┐
│  TIER 0: FREE FOREVER                                       │
│                                                             │
│  Track 1 complete (Kingdom Entrepreneurship — all 28 lessons│
│  First lesson of every other track                         │
│  English for Commerce: Levels 1-3 (Beginner)               │
│  Community access (read-only)                              │
│  Monthly live Q&A (first Thursday of month)                │
│                                                             │
│  Who this serves: Anyone with curiosity and a phone        │
│  Revenue impact: Zero direct, but creates the pipeline     │
└─────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────┐
│  TIER 1: CORE MEMBERSHIP — $15/month or $120/year           │
│                                                             │
│  Everything in Free tier plus:                              │
│  Track 2 complete (Business Mastery)                       │
│  Track 4 complete (Leadership & Mindset)                   │
│  English for Commerce: All levels                          │
│  Community access (full participation)                     │
│  Certification of completion for each track                │
│  Cohort learning groups (accountability partners)          │
│                                                             │
│  Who this serves: Early-stage entrepreneurs, English       │
│  learners, anyone building toward a first business         │
└─────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────┐
│  TIER 2: PROFESSIONAL MEMBERSHIP — $35/month or $299/year   │
│                                                             │
│  Everything in Core tier plus:                              │
│  Track 3 complete (Modern Skills)                          │
│  Quarterly live skill workshops (virtual)                   │
│  AI tool tutorials (updated quarterly)                     │
│  Access to mentor network (certified merchants + alumni)   │
│  1:1 coaching session (1 per quarter, 30 minutes)          │
│  Shareable Professional Completion Certificate             │
│                                                             │
│  Who this serves: Active business owners, established      │
│  merchants wanting skills updates, team training           │
└─────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────┐
│  TIER 3: BUSINESS SPONSORSHIP — $75/month                   │
│                                                             │
│  Everything in Professional tier plus:                      │
│  Enroll up to 3 employees at no additional cost            │
│  Sponsor a community member (pay for someone's Core tier)  │
│  Listed as an "Academy Sponsor" on TheGiveback merchant    │
│    storefront and community profile                        │
│  Access to hiring network (Academy graduates)              │
│  Featured in monthly Academy graduate spotlight            │
│                                                             │
│  Who this serves: Certified merchants who want to train    │
│  their team and invest in their community's development    │
└─────────────────────────────────────────────────────────────┘
```

### The Giving Integration in Pricing

Learners who cannot afford any paid tier can earn access through giving activity:

- **Giveback Points redemption:** 500 Giveback Points = 1 month of Core Membership access. Points earned by shopping at certified merchants convert directly into education access. Spending in your community funds your own development.
- **Community referral:** Refer 3 new learners to the free tier → receive 1 month Core Membership free.
- **Foundation sponsorship:** Vetted foundations can sponsor unlimited free tier access for their program participants — funded from their TheGiveback disbursements as an approved program use.

### Sponsored Access for Underserved Learners

A dedicated "Access Fund" — funded by a portion of Academy revenue plus optional merchant contributions — provides free Core Membership to:
- People referred by foundations in the TheGiveback network
- Immigrants and refugees in communities served by certified merchants
- Incarcerated or recently released individuals (through partner organizations)
- People living below 200% of the federal poverty line (self-declared, honor system)

The Access Fund is not charity — it is pipeline. Every person who receives sponsored access and builds a business becomes a potential DataOne merchant, a potential TheGiveback consumer, a potential foundation funder. The investment returns at every stage.

---

## 5. Content Strategy — License vs. Create

### The Decision Framework

| Content Type | License or Create | Rationale |
|---|---|---|
| Kingdom Entrepreneurship (Track 1) | **Create — original** | This is TheGiveback's unique voice. No licensed content captures the specific connection between Kingdom values and the certified merchant ecosystem. Must be original. |
| Business Mastery (Track 2) | **Create — original** | Generic business content is everywhere. The value here is practical, SMB-specific, payment-processing-aware content that serves a certified merchant. Must be contextually specific. |
| Modern Skills — AI modules (Track 3) | **License + Create hybrid** | License introductory AI content from established providers (Coursera, LinkedIn Learning, Google Digital Garage). Create original modules for AI applications specific to small business contexts that no licensed provider covers. |
| Leadership & Mindset (Track 4) | **License + Create hybrid** | Pursue licensing conversations with Maxwell Leadership and/or Robbins Research International for foundational frameworks. Create original modules that integrate Kingdom values with those frameworks. |
| English for Commerce (Track 5) | **License core ESL + Create commerce layer** | License a proven ESL curriculum (Rosetta Stone Business, Pimsleur, or similar) for language fundamentals. Create original "English for Commerce" modules on top — negotiating, invoicing, customer service, business communication specifically for small business contexts. |

### Priority for Original Content Creation

The first content to create, in order:
1. Track 1 complete (Kingdom Entrepreneurship) — this is the door; it must exist and be excellent before anything else
2. Business Mastery foundation modules (first 5 modules of Track 2)
3. English for Commerce Levels 1-3 (beginner access — free tier)
4. Leadership modules 1-3 (calling, resilience, decision-making)

This minimum set constitutes a viable Phase 1 launch. Everything else layers in over Phase 2-3.

### Content Creator Network

Original content for TheGiveback Academy is not all created in-house. Build a vetted content creator network — Kingdom entrepreneurs, business educators, licensed coaches, ESL instructors — who create modules under license to the Academy:

- Creator submits module proposal with outline and sample lesson
- Academy editorial team reviews for content quality, mission alignment, and practical application
- Approved creators produce video content, workbooks, and assessments to Academy spec
- Revenue share: creator receives 20% of enrollment revenue attributed to their modules (tracked by engagement analytics)
- Creator retains no ownership of final content — full license transfer to TheGiveback Academy

This creates a content flywheel: graduates who become successful entrepreneurs become the most credible content creators for future cohorts. A certified merchant who built a successful business using Academy principles teaches the next generation of Academy learners. That is Kingdom entrepreneurship expressed in the learning model itself.

---

## 6. The English Access Track — Design Philosophy

### Why This Track Is Different

The other four tracks are primarily video-and-workbook courses. Track 5 is different in structure because language acquisition is different from knowledge acquisition. You cannot watch a video about riding a bike and learn to ride a bike. Similarly, you cannot watch a video about English conversation and learn to have an English conversation.

Effective adult language learning requires:
1. **Comprehensible input** — language slightly above the learner's current level
2. **Repetition with variation** — the same vocabulary in multiple contexts
3. **Production** — the learner must speak and write, not just listen and read
4. **Feedback** — the learner must know when they're correct and when they're not
5. **Relevance** — content that connects directly to the learner's real life

The English for Commerce track is designed around all five. It is not a grammar course. It is not a vocabulary course. It is a practical communication course for adults who need to conduct business in English.

### The Four Levels

```
ENGLISH FOR COMMERCE — FOUR LEVELS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Level 1: FOUNDATIONS (Free)
  Greetings, introductions, numbers, basic transactions
  "How much is this?" · "Let me check for you."
  "My name is ___ and I own ___."

Level 2: COMMERCE BASICS (Free)
  Customer service, taking orders, handling complaints
  "I understand your concern." · "Let me fix that."
  "We accept credit cards and cash."

Level 3: BUSINESS COMMUNICATION (Free)
  Emails, phone calls, scheduling, basic negotiation
  "I'd like to follow up on our conversation."
  "Could we schedule a meeting for Thursday?"

Level 4: PROFESSIONAL FLUENCY (Core Membership)
  Presentations, pitching, contracts, banking conversations
  Job interviews, hiring conversations, community relationships
  Navigating government and regulatory English
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Levels 1-3 Are Free — Without Exception

This is the most important design decision in the entire Academy. Levels 1-3 cover the foundational English a non-English-speaking small business owner needs to serve customers, handle basic transactions, and communicate in everyday commerce situations. Making these free is not a marketing decision. It is a moral one. The economic stakes of English fluency for an immigrant small business owner are too high for this content to sit behind a paywall.

Level 4 — Professional Fluency — is included in Core Membership and covers the more advanced communication skills needed to pitch for contracts, negotiate with suppliers, engage with lenders, and navigate the formal business world. This is appropriately paid because it serves people who have already developed their business beyond the survival stage.

### The AI Conversation Partner

The English for Commerce track includes an AI-powered conversation practice partner. Not a chatbot for support — a dedicated language practice interface where learners can:

- Practice scripted commerce conversations with AI feedback on vocabulary, grammar, and pronunciation
- Role-play specific scenarios: a customer complaint, a supplier negotiation, a job interview, a bank meeting
- Receive instant correction with explanation ("You said 'I no have' — in English this becomes 'I don't have.' Let's practice this together.")
- Track progress across vocabulary breadth and conversation fluency

The AI tutor is available 24/7, infinitely patient, speaks the learner's native language when introducing corrections, and never makes the learner feel embarrassed for making mistakes. This is the thing a human tutor does well but cannot do at scale, at all hours, in every native language.

**Technical implementation:** The AI conversation partner is built using Claude API (Anthropic) with a system prompt specifically designed for adult ESL commerce contexts. It is not a general assistant — it is a focused language coach. Each practice session is in the context of a specific commerce scenario (taking a customer order, explaining a service, writing a business email).

### The Practical Commerce Scenario Library

Every lesson in Levels 1-4 is anchored to a real commerce scenario that a small business owner would encounter. The library of scenarios grows over time and is organized by business category:

| Business Category | Sample Scenarios |
|---|---|
| Food Service | Taking an order, explaining the menu, handling a complaint, managing a reservation |
| Retail | Processing a return, describing a product, managing a price dispute, closing the store |
| Personal Services | Booking an appointment, explaining a service, discussing pricing, handling a rescheduling |
| Construction / Trades | Giving an estimate, explaining a timeline, handling a change order, communicating with a subcontractor |
| Professional Services | Setting up a meeting, explaining a proposal, following up on a quote, handling a referral |

A barbershop owner in the network learns English through scenarios that happen in their barbershop. A restaurant owner learns English through scenarios that happen in their restaurant. The learning is immediately applicable to their actual work.

### Native Language Support

The English for Commerce track provides instructional support in the learner's native language. Vocabulary explanations, grammar notes, and lesson instructions appear in the learner's selected language alongside the English content. Available from launch:

- Spanish (highest priority)
- Portuguese
- Haitian Creole
- Vietnamese
- Korean

The lesson content is in English — that is the product. The support scaffolding is in the learner's native language.

---

## 7. The Virtual & Live Events Layer

### The Academy Event Calendar

The Academy runs two categories of live events: recurring virtual events included in membership tiers, and premium in-person or virtual events available as standalone purchases.

### Recurring Virtual Events (Membership Included)

| Event | Frequency | Access Tier | Description |
|---|---|---|---|
| Monthly Open Q&A | First Thursday, 7pm ET | Free | Live Q&A with Academy team. Any topic. |
| Business Foundations Workshop | Monthly | Core | 90-minute deep dive on one Business Mastery topic |
| Modern Skills Live | Quarterly | Professional | 2-hour workshop on a current AI or digital tool |
| Kingdom Entrepreneur Roundtable | Monthly | Core | Peer group conversation — share wins, struggles, questions |
| English Practice Circle | Weekly | Free (Levels 1-3) | Small group conversation practice with a facilitator |

The English Practice Circle is the single most important recurring event in the Academy. Language acquisition accelerates dramatically with live human conversation practice. A weekly 45-minute small group session (6-8 learners + one facilitator) where participants practice that week's scenarios in real time is more effective than any amount of solo app-based practice. Facilitators are recruited from Academy graduates who have achieved Level 4 fluency and want to give back — they receive Core Membership for free in exchange for facilitating two circles per week.

### Premium Events (Standalone Purchase or Professional Tier)

**Annual TheGiveback Academy Summit**
A 2-day virtual event (with optional in-person hub locations at certified merchant venues) combining keynote sessions, breakout workshops, a Kingdom entrepreneur showcase, a networking marketplace for attendees to find partners and collaborators, and a live pitch competition where Academy graduates pitch their business ideas with judges awarding prizes funded from Academy revenue.

Ticket pricing:
- Virtual access: $97
- In-person hub (at certified merchant location): $147 (includes the hub experience)
- Professional Membership holders: Free virtual access

The Summit serves three purposes simultaneously:
1. It is an Academy event that graduates and prospective learners attend
2. It is a TheGiveback Live event — streamed on the Live platform, generating tips and foundation contributions
3. It is a certified merchant showcase — the in-person hubs are hosted by certified merchants who receive foot traffic, visibility, and the giving story from hosting a summit hub

**Kingdom Business Intensives**
2-day deep-dive workshops on specific topics: launching a food business, building a service business, AI for small business, financial literacy mastery. Pricing $197-$297 per event. Available to any tier with early access for Professional and Business Sponsorship members.

**English for Commerce Immersives**
3-hour virtual intensive practice sessions for specific commerce scenarios. Priced at $29/session or included in a quarterly bundle for Core Membership. Designed for learners preparing for a specific real-world situation (a bank meeting, a contract negotiation, a customer service challenge).

---

## 8. The Robotica AI Connection — Measuring Learning

### OTIS Applied to the Academy

The OTIS video intelligence layer (Layer 1 of the Robotica stack) was designed for foundation program measurement. It applies directly to Academy learning sessions.

When a live Academy event — a workshop, a roundtable, a Practice Circle — is instrumented by OTIS, the Academy receives:
- An engagement curve showing collective attention across the session
- Drop-off analysis identifying exactly which topic or format caused disengagement
- A Session Effectiveness Score (SES — equivalent to the foundation's PES)

This data answers questions no LMS analytics currently answer:
- Which instructor holds attention most effectively?
- Which topics disengage learners fastest — and does that correlate with the topics they struggle with most in assessments?
- At what point in a 90-minute workshop does the room lose momentum — and how do we redesign the format to prevent it?
- Does the English Practice Circle format produce better engagement than solo app-based practice? (Yes, but now you have evidence.)

### Adaptive Learning Paths from Engagement Data

When OTIS engagement data is combined with assessment performance data (quiz scores, practice conversation results, module completion rates), the Academy can identify:
- Which learners are on track for success based on engagement + performance correlation
- Which learners are at risk of dropping out before completing a track (engagement declining, assessment scores plateauing)
- Which content should be flagged for review (high drop-off + low assessment scores = content problem, not learner problem)

This is learning intelligence that the best EdTech companies in the world are building toward. TheGiveback Academy has it built in from the Robotica partnership.

### The Virtuous Measurement Cycle

```
Academy delivers content
        ↓
OTIS measures engagement
        ↓
Academy improves content based on engagement data
        ↓
Improved content produces better learner outcomes
        ↓
Better outcomes produce better graduates
        ↓
Better graduates build stronger businesses
        ↓
Stronger businesses generate more giving
        ↓
More giving funds more foundation programs
        ↓
Foundation programs instrumented by same OTIS stack
        ↓ (loop)
```

The Robotica measurement layer is not just a feature of the Academy — it is the feedback mechanism that makes the Academy systematically better over time in a way that no competitor without the same measurement infrastructure can replicate.

---

## 9. Platform Integration with TheGiveback Ecosystem

### Six Integration Points

#### Integration 1: Giveback Points as Currency for Academy Access
Learners who earn Giveback Points by shopping at certified merchants can redeem them for Academy course access. This directly connects the commerce ecosystem to the learning ecosystem — spending in your community funds your own education.

Conversion rate: 500 Giveback Points = 1 month Core Membership ($15 value)

#### Integration 2: Certified Merchant → Academy Sponsor
Certified merchants in the Business Sponsorship tier ($75/month) can enroll up to 3 employees and sponsor community members for Core Membership. This creates a workforce development channel funded by the businesses that also fund the foundations.

A certified merchant who sponsors their employee's Academy enrollment:
- Gets a more skilled employee
- Earns a "Academy Sponsor" badge on their storefront
- Generates community goodwill that the AI impact story includes
- Has a hiring pipeline from Academy graduates who know the mission

#### Integration 3: Academy Graduates → Certified Merchant Pipeline
Every Academy graduate who builds a business is invited to join DataOne and become a Giveback Certified merchant. The invitation is part of the graduation ceremony — not a sales pitch but a natural next step.

"You've built the skills. Now build the business. And when you do, consider joining the certified merchant network — because the business that gives back is the business that lasts."

#### Integration 4: Foundations → Sponsored Learner Access
Foundations in the TheGiveback network can use a portion of their disbursements to sponsor Academy access for their program participants. A food pantry that runs a financial literacy program can extend that program by sponsoring Core Membership for participants who want to go deeper. The Givehub API integration enables this — a foundation administrator creates sponsored access codes through the Givehub portal.

#### Integration 5: The Community Layer → Academy Activity
Academy milestones surface in the consumer app's My Community feed:
- "A neighbor just completed their Kingdom Entrepreneurship certification"
- "3 new learners joined the English Practice Circle in your neighborhood this week"
- "Miller's Hardware is sponsoring 2 Academy learners this month"

These posts are not marketing. They are community testimony that the platform is doing what it promises — creating more capable, more confident people in the local economy.

#### Integration 6: TheGiveback Live → Academy Content
The Academy's live events (workshops, roundtables, summits) are hosted on TheGiveback Live platform. This means:
- Events generate tips that split 70/20/10 (instructor/foundation/platform)
- Silent auction items from certified merchants appear alongside Academy events
- Attendance at a live Academy event generates an "I was there" badge in the community feed

The instructor becomes the artist in the TheGiveback Live model. The Academy event becomes the show. The foundation is the cause. The format already exists — the Academy just uses it.

---

## 10. Data Architecture

### New Tables

#### `academy_learners`
```
id, consumer_id (nullable — learners may not be consumers yet),
name, email, primary_language, enrollment_tier (free|core|professional|business),
enrollment_date, sponsored_by (merchant_id nullable, foundation_id nullable),
giveback_points_redeemed_cents, created_at, updated_at
```

#### `academy_enrollments`
```
id, learner_id, track_id, enrolled_at, completed_at (nullable),
completion_certificate_url (nullable), created_at
```

#### `academy_module_progress`
*Append-only*
```
id, learner_id, module_id, started_at, completed_at (nullable),
time_spent_seconds, quiz_score (nullable), attempts, created_at
```

#### `academy_tracks`
```
id, name, slug, tier_required (free|core|professional),
description, module_count, estimated_hours, published_at,
language, created_at
```

#### `academy_modules`
```
id, track_id, title, description, lesson_order, estimated_minutes,
content_type (video|audio|text|practice|assessment),
content_url, transcript_url, workbook_url, is_free_preview,
languages_available (JSON array), published_at, last_updated_at,
created_at
```

#### `english_practice_sessions`
```
id, learner_id, session_type (ai_practice|group_circle),
scenario_id, duration_seconds, conversation_log (encrypted),
vocabulary_score, grammar_score, fluency_proxy_score,
facilitator_id (nullable for AI sessions), created_at
```

#### `academy_sponsorships`
```
id, sponsor_type (merchant|foundation),
sponsor_id, learner_id, tier_sponsored (core|professional),
started_at, expires_at, cost_cents, funded_from (giveback_points|
direct_payment|foundation_disbursement), created_at
```

#### `academy_events`
```
id, title, event_type (q_and_a|workshop|roundtable|practice_circle|
intensive|summit), format (virtual|in_person|hybrid),
scheduled_at, duration_minutes, host_id, foundation_beneficiary_id,
min_tier (free|core|professional), ticket_price_cents (nullable),
show_id (nullable — links to TheGiveback Live if streamed),
recording_url (nullable), otis_session_id (nullable), created_at
```

### Privacy Notes

- `conversation_log` in `english_practice_sessions` is encrypted at rest and never surfaces to any third party. It is used only for learning analytics by the learner and the Academy team.
- OTIS engagement data for live sessions follows the same privacy architecture as foundation program instrumentation — aggregate signals only, no individual identification.

---

## 11. Technical Stack

### LMS Platform

**Phase 1-3: Kajabi (white-label)**
- Course delivery, membership tiers, email marketing, community spaces, live sessions
- Custom domain: academy.thegiveback.org
- White-label mobile app: $199/month add-on, launch at Phase 2

**Phase 4-5: Custom migration decision**
Evaluate migration to custom LMS if:
- Enrollment exceeds 5,000 active learners
- Kajabi transaction economics become unfavorable at scale
- The ecosystem integrations (Giveback Points, ledger, OTIS, merchant sponsorship) are mature enough to justify the rebuild cost

Until then: Kajabi is the right choice. Do not build what Kajabi already does.

### AI Conversation Partner

- Claude API (Anthropic) for the English Practice AI tutor
- Dedicated system prompt for ESL commerce contexts
- Speech-to-text: Whisper API (OpenAI) for pronunciation assessment
- Text-to-speech: ElevenLabs or similar for natural instructor voice responses
- Session logs stored encrypted in academy database, not in API provider logs

### Video Hosting

- Wistia or Vimeo Pro for course video hosting (not YouTube — no ads, better analytics)
- Mux for live events (same stack as TheGiveback Live)
- Videos are transcribed automatically for accessibility and multilingual subtitle generation

### Authentication

- Single sign-on with the main TheGiveback consumer account where learner is also a consumer
- Separate email/password auth for learners who are not yet consumers
- Learner → Consumer conversion pathway built into the auth flow: "You're learning how to build a business. Start exploring certified merchants in your community →"

---

## 12. Build Sequence

### Phase 3 — Academy MVP (Months 6–10)

*Content first. Platform second. Community third.*

- [ ] Create Track 1 (Kingdom Entrepreneurship) — all 28 lessons — in-house
- [ ] Create Track 2 first 5 modules (Business Mastery foundation)
- [ ] Create English for Commerce Levels 1-3 (free tier)
- [ ] Set up Kajabi white-label at academy.thegiveback.org
- [ ] Configure four membership tiers and access controls
- [ ] Launch Monthly Open Q&A (free, drives awareness)
- [ ] Launch English Practice Circle (free, weekly virtual)
- [ ] Giveback Points → Core Membership conversion (Kajabi webhook → TheGiveback ledger)
- [ ] Academy milestone posts in consumer app community feed
- [ ] Certified Merchant → Academy Sponsor enrollment flow

### Phase 4 — Academy Full Build (Months 10–16)

*Complete content library. Live events. AI tutor.*

- [ ] Create Track 2 complete (Business Mastery — all 10 modules)
- [ ] Create Track 3 (Modern Skills) — AI modules first, quarterly update process
- [ ] Create Track 4 (Leadership & Mindset) — licensing conversations with Maxwell Leadership
- [ ] Create English for Commerce Level 4 (Professional Fluency)
- [ ] AI Conversation Partner integration (Claude API + Whisper)
- [ ] Spanish language support across all tracks
- [ ] Content Creator Network onboarding (vetted educators)
- [ ] Academy mobile app (Kajabi white-label)
- [ ] First Annual Academy Summit
- [ ] Foundation → Sponsored Learner Access (Givehub portal integration)
- [ ] OTIS instrumentation for live Academy events
- [ ] Graduate → Certified Merchant invitation flow

### Phase 5 — Academy at Scale (Months 18–24+)

*Additional languages. Licensing expansion. Custom LMS evaluation.*

- [ ] Portuguese, Haitian Creole, Vietnamese language support
- [ ] B2B licensing: offer Academy content to corporations for employee training
- [ ] Academic partnerships: community colleges as distribution channel for English track
- [ ] Custom LMS migration evaluation at 5,000+ learners
- [ ] Academy alumni network (graduates who become certified merchants)
- [ ] Business Mastery "Advanced" modules (for established business owners)

---

## 13. Content Partnerships to Pursue

### Licensing Targets

| Partner | What to License | Track | Status |
|---|---|---|---|
| Maxwell Leadership | 5 Levels of Leadership framework, Developing the Leader Within | Track 4 | Pursue Phase 3 |
| Robbins Research International | Peak performance frameworks, peak state content | Track 4 | Pursue Phase 3 |
| Google Digital Garage | AI fundamentals, digital marketing foundations | Track 3 | Free content — integrate directly |
| LinkedIn Learning | Select AI tools courses (license for distribution) | Track 3 | Pursue Phase 3 |
| Rosetta Stone Business | Core ESL curriculum for licensed delivery | Track 5 | Pursue Phase 3 |
| SCORE (SBA) | Small business mentorship content — free licensing available | Track 2 | Phase 3 |
| Khan Academy | Financial literacy foundational content | Track 3 | Free CC license available |

### Content Creation Partners

| Partner Category | What They Create | Revenue Share |
|---|---|---|
| Kingdom entrepreneurs in the merchant network | Track 1 and 2 testimonial modules | 20% of attributed enrollment revenue |
| Certified merchants in relevant industries | Industry-specific Track 2 modules (restaurant, retail, trades) | 20% of attributed enrollment revenue |
| Licensed ESL educators | Track 5 curriculum development | Contract, not revenue share |
| AI practitioners | Track 3 AI modules (updated quarterly) | Contract + 15% of attributed enrollment revenue |

---

## 14. Success Metrics

### Academy Enrollment & Engagement

| Metric | Target | Why |
|---|---|---|
| Free tier enrollments | Growing month-over-month | Top of funnel health |
| Free → Paid conversion rate | 15%+ within 90 days | Content quality signal |
| Track 1 completion rate | 60%+ of enrolled learners | The most important single metric — Track 1 completion predicts everything else |
| English Practice Circle weekly attendees | Growing week-over-week | Language track engagement |
| Monthly active learners (any activity) | 40%+ of enrolled learners | Platform stickiness |
| Core Membership retention (month 3) | 70%+ | Content delivering ongoing value |

### Mission Metrics

| Metric | Why It Matters |
|---|---|
| Academy graduates who become DataOne merchants | The pipeline metric — learning converting to commerce |
| Sponsored learners (via foundations or merchants) | The access metric — are we reaching people who need it most |
| English Practice Circle learners reporting commerce milestone | A learner who gets their first English-only customer, handles their first English complaint — these are the real outcomes |
| Business launches by Academy graduates | The ultimate outcome metric |

### The One Story That Tells You It's Working

Someone who arrived at TheGiveback Academy speaking no English, completed Levels 1-4 of English for Commerce over 8 months, used Track 2 to understand how to structure a business, used the Giveback Points they earned shopping at certified merchants to pay for their Professional Membership, launched a small business, became a DataOne merchant, and now has $47/month flowing to a local foundation — and their 11-year-old child helped them practice English every night.

That story. That is the metric. Build everything in service of that story being possible.

---

## 15. Fixed Decisions for This Feature

| Decision | Rationale |
|---|---|
| English for Commerce Levels 1-3 are free forever, no exceptions | The economic stakes of English fluency for immigrant entrepreneurs are too high for foundational content to be paywalled. |
| Track 1 (Kingdom Entrepreneurship) is free forever | It is both the right thing to do and the most effective marketing. Transformation precedes transaction. |
| Faith integration is contextual, not required | Every person who enters the Academy — regardless of their faith background — should receive the full value of the content. The Kingdom perspective is offered, not imposed. |
| AI Conversation Partner uses Claude API, not a generic chatbot | The conversation partner needs to be reliably patient, contextually intelligent, and culturally sensitive. A purpose-built implementation on a quality model is the right approach. |
| Content is updated quarterly for Track 3 (Modern Skills) minimum | AI content that is 18+ months old is actively harmful to learners who act on it. The update cadence is a commitment, not a goal. |
| Academy events live on TheGiveback Live platform | Every Academy live event is also a community event that generates giving. The format already exists. The Academy uses it. |
| Licensed content does not replace original content — it supplements it | TheGiveback Academy's unique voice — Kingdom entrepreneurship + certified merchant ecosystem + local giving — cannot be outsourced. Original content is the core. Licensed content fills gaps. |
| Kajabi is the Phase 1-3 platform | Do not build LMS infrastructure when Kajabi solves the problem for $378/month. Build the content and the community. Migrate the infrastructure only if scale justifies it. |
| The Access Fund is funded from Academy revenue, not from the giving covenant | The giving covenant funds foundations. The Access Fund funds learning access. These are separate uses of separate revenue streams. Never cross-fund. |
| Graduates are invited, not sold, into the certified merchant network | The graduation-to-merchant pathway is an invitation that the graduate has earned by completing their track. It is never a sales call during the course itself. |

---

*This document is an addendum to TheGiveback Complete Product & Strategy Document (v1.0) and should be read alongside the Feature Gaps & Future Capabilities document. The Academy is one of the highest-mission-impact features on the platform and one of the most complex to execute well. Build the content before you build the platform. Build the free tier before you build the paid tier. And remember: the first learner who builds a business and becomes a certified merchant because of this Academy is worth more to the mission than 10,000 enrolled learners who never finish Track 1.*
