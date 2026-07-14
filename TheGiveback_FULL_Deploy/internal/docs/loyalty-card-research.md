# TheGiveback — Loyalty, Rewards & Card Issuing
### Strategic Research Memo · July 2026 · Not legal or financial advice

---

## Executive Summary

The research confirms this is exactly the right time to be thinking about this layer — and confirms that nobody has built it with the specific architecture that fits TheGiveback's existing structure. The loyalty and card issuing space in 2026 is actively moving toward cause-linked rewards, embedded giving, and card-linked philanthropy. You'd be swimming with the current, not against it. But the path matters enormously: the right architecture makes loyalty a flywheel that amplifies the mission; the wrong one (Bilt's lesson, studied in detail below) makes it a money pit. This memo maps both.

---

## Part 1 — The Loyalty Landscape in 2026

### What's happening in the market right now

Loyalty is entering a new era. What was once a static, rules-based system is becoming a dynamic, data-driven engine that adapts to each customer and every transaction. Programs are expanding to include embedded financial tools — savings, investing, and donations — all triggered by everyday purchases. Roundups, savings boosts, micro-investing, debt paydown, and charitable donations are becoming standard loyalty actions.

The best banking loyalty programs in 2026 step in early. They guide without pressure. They reward without noise. Loyalty is no longer measured in points — it's measured in presence, the sense that each interaction belongs to something bigger.

Three structural things matter for TheGiveback specifically:

**Card-linked loyalty is the winning architecture.** Card linking securely connects a person's debit or credit card to a rewards or loyalty program. Once linked, every time they make a qualifying purchase, the system automatically applies a reward — cashback, roundups, savings, or donations — without any added steps. Every linked transaction is tokenized and encrypted. Card data is never exposed or stored in plain text. This is important: the "no friction" model is precisely what TheGiveback's design philosophy demands. Giving should be automatic, not a conscious act.

**Cause-linked redemption is now a mainstream loyalty feature.** Pledge's platform allows customers to donate points to over 2 million verified nonprofits, or choose from curated cause collections. Studies show that 77% of consumers are more likely to be loyal to brands that offer meaningful giving opportunities. The infrastructure for points-to-charity conversion already exists as a licensable API layer — you don't have to build it from scratch.

**AI is becoming load-bearing in loyalty design.** AI is moving from a supportive tool to the core of program design. A customer showing early signs of churn may receive a targeted incentive within minutes, not days. Card-linked transactions create a single, reliable source of truth for spend behavior and attribution. This aligns directly with the AI cause-matching and impact-story engines already planned for TheGiveback.

---

## Part 2 — The Bilt Case Study: What to Copy and What to Avoid

Bilt Rewards is the most instructive comparable — not because you should replicate it, but because it shows exactly where cause-linked card issuing can go wrong, and why TheGiveback's structure avoids those failure modes.

### What Bilt got right (copy this)

Bilt Rewards is an American financial technology company that operates a loyalty and payments platform centered on rent payments, offering a co-branded credit card program and related financial products.

Bilt operates as a hybrid payment processor and loyalty network that monetizes through transaction fees, merchant commissions, and banking partnership subsidies. The core monetization comes from processing rent payments where Bilt earns 0.6% to 0.9% in transaction fees from landlords and property management companies.

The genius of Bilt's original model: anchor the loyalty currency to a payment that was already happening (rent), generate real transaction volume, and earn interchange on the card spend. The loyalty program didn't cost extra — it was funded by the economics of the underlying payment rail. **That's your model too.** The Giveback loyalty points would be funded by the processing margin already flowing through DataOne, not by a separate loyalty budget.

Bilt has proven rent should be rewarding. The three Bilt Card 2.0 options deliver the richest rewards on rent, mortgage, and everything else — rewarding members across 5.5 million homes with exclusive benefits at tens of thousands of neighborhood locations.

The neighborhood merchant layer is directly analogous to the TheGiveback certified merchant directory. Bilt created a network of local businesses as a loyalty ecosystem. You're doing the same thing, except the certified merchant certification already exists and the giving infrastructure is already running underneath it.

### What Bilt got catastrophically wrong (avoid this)

In July 2025, Wells Fargo announced it would end its partnership with Bilt Rewards ahead of schedule, as it was losing up to $10 million per month through Bilt Rewards.

It looks like Wells Fargo was correct — this variation of the successful credit card co-brand model might scale, but it loses money. The experience of Bilt suggests that innovation alone is not enough. Even innovative products must be supported by sustainable economics, reliable operations, and strong partnerships.

The reason Bilt bled money: they were rewarding a payment category (rent) that generates almost no interchange revenue, while funding rich travel rewards from that same thin margin. The math never worked. A bank loses money every time a Bilt cardholder pays rent with the card because the interchange on ACH rent processing is essentially zero, but the points liability is real.

**TheGiveback's structure doesn't have this problem.** The loyalty points would be earned on card-present merchant transactions — the highest-interchange category — not on rent or mortgage payments. Your interchange economics actually support a loyalty program.

Bilt completely revamped its offerings in early 2026 with three new credit cards — the Bilt Blue ($0 annual fee), Bilt Obsidian ($95 annual fee), and Bilt Palladium ($495 annual fee) — while also adding a new currency called Bilt Cash alongside Bilt Points. Following the rollout, some cardholders reported problems with rent and mortgage payments failing to process on time. The complaints prompted scrutiny from regulators.

The complexity lesson: Bilt launched a dual-currency system (Bilt Points + Bilt Cash) at the same time as a full card product overhaul, and operationally it fell apart. For TheGiveback, keep the currency simple — one unit, one redemption path, one story.

---

## Part 3 — The Card Issuing Infrastructure

### How the stack works

A white-label debit card is a branded payment card issued on top of a licensed sponsor bank, a card network (Visa or Mastercard) and a processor, using your own UX, logo and card art. You design the product, your users see your brand, and a regulated partner carries the license, the compliance and the settlement risk. In 2026, white-label is no longer a novelty. Chime, N26, Revolut, Ramp, Brex, and most modern payroll and gig platforms run on some flavour of this stack.

The key vendors for a US-focused program:

**Processors/issuers:** Marqeta is the card issuer-processor that powers DoorDash, Uber, Klarna and dozens of other at-scale programs. If your product is cards first — spend controls, virtual cards, just-in-time funding — Marqeta is hard to beat on programmatic control. Galileo, owned by SoFi, combines a long-standing processor with access to a national bank charter on SoFi's balance sheet. It is a favorite of card-first fintech launches across North America.

**Sponsor banks (US):** In the US, the leaders are Evolve Bank & Trust, Stride Bank, Celtic Bank, Lead Bank, Patriot Bank, and Piermont Bank, most of them Durbin-exempt.

**Important 2026 context:** Three structural shifts define 2026. First, middleware is going direct — BaaS vendors that used to route through sponsor banks are buying or securing their own licenses, so the brand contracts with one party instead of three. Second, the regulators have caught up — consent orders against Cross River, Evolve, and others in 2023-2024 pushed the industry toward stricter KYC, reconciliation and reserve practices.

The regulatory tightening is worth flagging: sponsor banks are now doing real audits on program managers, not just paperwork. This needs to be built into your compliance budget and timeline from day one.

### The cause-linked point conversion layer

Pledge's platform allows companies to seamlessly integrate charitable giving options directly into their existing loyalty ecosystem. We handle all the technical complexities — from point conversion to donation processing — enabling your brand to offer a powerful, turnkey way for customers to make a difference without leaving your loyalty platform. We handle the backend, including disbursing funds in a safe, trusted and compliant way through our DAF, the Pledgeling Foundation.

This is a direct build-vs-buy decision for TheGiveback. Pledge essentially is the points-to-charity conversion infrastructure as a licensable API, including DAF-compliant disbursement. For Phase 4, this could be the fastest path to launching a cause-linked redemption option without building the entire disbursement layer in-house. Worth a discovery call.

---

## Part 4 — How Loyalty and Cards Fit Into TheGiveback's Architecture

### The model that works

There is a specific model that fits TheGiveback's existing structure and avoids Bilt's failure modes. Here's how it works:

**Step 1 — The Giveback Card (debit, merchant-funded)**
A co-branded Visa or Mastercard debit card issued via a BaaS partner (Marqeta or Galileo + sponsor bank). Cardholders are merchants' customers — consumers who shop at Giveback Certified businesses. The card earns "Giveback Points" on every swipe at certified merchants, funded by merchant interchange on those transactions.

The key economics: debit card interchange on a merchant transaction is 0.05% + $0.22 (Durbin cap) for regulated issuers, or up to ~1.5-2% for unregulated programs. This is very different from Bilt's rent-payment problem. You're earning interchange on exactly the transactions that are already generating the Giveback Pool — the two revenue streams reinforce each other.

**Step 2 — The Giveback Points currency**
Simple, single-currency. One point per dollar spent at certified merchants. Points can be redeemed for three things only:
- **Donate to a foundation** — convert points into direct giving to the merchant's matched cause (via Pledge or similar DAF API). This is the primary redemption path and the mission-aligned one.
- **Statement credit** — standard cash-equivalent value, kept simple.
- **Merchant rewards** — discounts or perks at Giveback Certified businesses (merchant-funded, no cost to TheGiveback).

No travel redemptions. No hotel points. No airline miles. The complexity of a points-transfer ecosystem is what killed Bilt's operational execution and confused its customers. TheGiveback's brand promise is simplicity and local impact — a redemption catalog that includes Delta SkyMiles transfer partners is incoherent with that promise.

**Step 3 — The mission flywheel**
When a consumer uses the Giveback Card at a certified merchant:
- The merchant's Giveback Pool contribution is automatically generated (from DataOne's margin — the existing covenant)
- The consumer earns Giveback Points on their spend
- The consumer can convert those points into additional giving to the same cause
- The foundation receives both the merchant's covenant contribution AND the consumer's point redemption as separate, clearly-labeled pools

Three separate giving streams from one swipe: company margin, consumer points, optional consumer round-up. All traceable. All on the public ledger. Each with its own story.

**Step 4 — The certification loyalty tier**
Merchants who process above a threshold volume through DataOne get "Platinum Certified" status — their customers earn bonus points at their business. This creates a merchant retention incentive beyond the giveback badge alone: their customers accumulate more points by shopping at their location than at a non-certified competitor. The certified merchant network becomes a loyalty coalition, not just a directory.

---

## Part 5 — What Makes This Structurally Different From Every Other Cause-Linked Card

| Program | Who funds the giving | Card economics | Mission alignment |
|---|---|---|---|
| Chase Pay Yourself Back | Cardholder's own points | Standard interchange | Incidental feature |
| Bilt Rewards | Bank subsidy (unsustainable) | Rent = near-zero interchange | Loyalty first, giving secondary |
| Airline miles to charity | Cardholder's expiring miles | Standard interchange | Expiry management tool |
| Pledge (white-label) | Cardholder's points | Depends on host program | API layer, no covenant |
| **TheGiveback Card** | **Company covenant (20-30% of margin) + cardholder points + round-up** | **Merchant-present card = highest interchange category** | **Giving is the product, card is the instrument** |

The differentiation is structural, not cosmetic. Every other cause-linked card treats giving as a feature of a payments product. TheGiveback's card would be a payments feature of a giving product. That inversion matters enormously for how customers experience it, how merchants talk about it, and how foundations trust it.

---

## Part 6 — The Sequencing Question

**Do not build the card in Phase 1, 2, or 3.**

The card issuing infrastructure requires: BaaS partner selection and contract negotiation, sponsor bank relationship, program manager designation, KYC/AML build, Visa/Mastercard network registration, PCI DSS compliance, and a compliance audit from the sponsor bank. That's 12-18 months of parallel-track work minimum, and it cannot start productively until you have a proven merchant network and a real giving track record to show the BaaS partners.

The right sequencing:

- **Phases 1-3 (now → month 8):** Build the giving infrastructure, prove the plumbing, launch the merchant dashboard and public site. This creates the evidence that makes the card program credible.
- **Phase 3-4 (month 6-12):** Begin BaaS partner discovery. The pitch to Marqeta or Galileo is "we have X certified merchants doing $Y in monthly volume, with a covenant giving program that creates a loyalty story no other card issuer has." You need real numbers to make that pitch.
- **Phase 4-5 (month 12-24):** Card program launch. Start with a waitlist of consumers who've already engaged with the platform — you're not launching cold.

The loyalty program itself (points on purchases, cause-linked redemption) can be built in Phase 3 as a card-linked feature on existing payment cards before the TheGiveback branded card exists. Use Pledge or a similar API to enable points-to-charity conversion from any payment card, tied to Giveback Certified merchant transactions. That's a lighter lift and generates the behavioral data you need before committing to a full card program.

---

## Part 7 — Open Risks and Questions for Counsel

*(Landscape only — not legal or financial advice)*

- **Program manager registration:** Depending on the BaaS structure, you may need to register as a payment facilitator or program manager with Visa/Mastercard before issuing cards under your brand.
- **Durbin Amendment:** If DataOne or a subsidiary issues the card, regulated issuer interchange caps apply (Durbin). Most fintech card programs work with Durbin-exempt banks (under $10B in assets) specifically to preserve higher interchange. Your sponsor bank selection matters enormously for unit economics.
- **Points liability on the balance sheet:** Unredeemed loyalty points are a liability. The accounting treatment and how they're reserved needs a CPA conversation before you launch a points program.
- **Consumer data:** Card-linked loyalty requires access to transaction data at the consumer level. The data-sharing agreement between the BaaS layer, DataOne, and TheGiveback needs to be clearly structured — consumers need to consent to the giving attribution.
- **Cause-linked redemption as charitable solicitation:** Converting points to donations on behalf of consumers may trigger commercial co-venture regulations in some states (the same landscape mapped in the competitive/legal research). Using a DAF intermediary (Pledge's model) largely resolves this, but needs confirmation.

---

## Bottom Line

The loyalty and card issuing layer is the right long-term vision. It turns TheGiveback from a giving program with a payment engine underneath it into a full financial platform where every swipe creates three simultaneous value streams: merchant goodwill, consumer engagement, and foundation funding. No competitor has built this combination.

The Bilt case study is the clearest cautionary tale in the space: you can build a brilliant loyalty architecture on top of a broken economics model. TheGiveback's model has the opposite problem — strong economics (merchant-present interchange on certified merchant transactions) underneath a loyalty structure that hasn't been built yet. That's a much better starting position.

The two things that determine whether this works: keeping the currency simple (one unit, three redemption paths, no travel transfer partners) and sequencing the card program correctly (prove the giving infrastructure first, use the track record to pitch the BaaS partner, launch the card with a warm audience). Build the points layer in Phase 3. Launch the branded card in Phase 4-5 when the merchant network and giving history give you something real to show.
