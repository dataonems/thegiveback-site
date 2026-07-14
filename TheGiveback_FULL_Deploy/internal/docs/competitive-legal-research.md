# TheGiveback — Competitive Landscape & Legal Landscape Research
### v1.0 · July 2026 · Research memo, not legal or tax advice

---

## PART 1 — WHO ELSE IS DOING THIS

Nobody is building exactly your three-sided system (payment infrastructure + merchant marketplace + vetted foundation network, funded from the processor's own margin). But four adjacent categories already exist, each proving out one piece of your model. Worth knowing all four before you build, because each one solved a problem you'll hit.

### Category A — Payment processors that already tithe their own margin
**This is your closest direct competitor category, and it's smaller than you'd think.**

- **Pro-Life Payments** (Mt. Pleasant, SC) — a full merchant services/POS processor that donates 15% of its *revenue* (not just profit) to pro-life ministries, marketed explicitly as a values-aligned alternative to Stripe/Square/PayPal. Single-cause focus, faith-branded, openly political positioning.
- **EPS (Electronic Payment Processing)** — donates a percentage of profits from transaction fees to a church or religious organization the merchant designates. Merchant-directed, single beneficiary per merchant.
- **AdelFi (formerly Christian Community Credit Union)** — not a processor but a faith-based bank/credit union that donates a portion of cardholder spend to Christian ministries and missions, member-owned.
- **My Well Ministry** — a nonprofit that runs a for-profit processing arm and gives services away at-cost to churches, using processing *savings* rather than a giveback pool.

**What this tells you:** the "payment processor with a giving covenant" model is proven and has real, sustained businesses in it — you're not inventing an unworkable category. But every one of them is single-cause, single-beneficiary, and processor-to-nonprofit direct. None of them run a multi-cause vetted marketplace, a merchant certification/dashboard layer, or a consumer-facing directory. **That three-sided system is your actual differentiation** — the giving-processor idea alone isn't new, but nobody has built the marketplace and transparency layer on top of it.

### Category B — Checkout micro-donation infrastructure (the "Round-Up" layer)
This is the closest analog to your consumer-facing "Round-Up for Good" feature, and it's a mature space with a specific, repeated structural pattern worth copying.

- **Pennies (UK)** — the category leader. Registered *as a charity itself*, partners with retailers and payment providers to add a round-up/top-up prompt at the terminal or checkout. 100+ merchants, 190M+ donations, £45M+ raised since 2010. Structurally: Pennies is the charity, keeps 10% for its own operating mission, grants 90% to the merchant's nominated charity. No consumer PII collected, no GDPR/PCI implications because the donation sits outside the secure payment flow.
- **RoundUp.org / RoundUp App** — US equivalent. Consumer links a card, purchases round up monthly, funds go first to **Our Change Foundation**, a registered 501(c)(3) donor-advised fund, which then grants to the consumer's chosen nonprofit. Acquired by Flourish Change in 2020.
- **DailyKarma / Shop for Good (Shopify)** — checkout-embedded round-up and % of sales, explicitly markets **"commercial co-venturing compliance and charity donation distribution services"** as part of its product — i.e., a checkout-donation vendor whose actual product includes solving the legal problem below, not just the UX.
- **Mastercard's Donate API** — card-network-level infrastructure for round-up donations, meaning the rails for this exact feature already exist as licensable infrastructure rather than something you'd need to build from scratch.

**The pattern that matters:** every single one of these routes consumer funds through either (a) being a registered charity itself, or (b) a donor-advised-fund intermediary. None of them hold consumer donation funds directly as a for-profit entity. That's not a coincidence — see Part 2.

### Category C — "Give away the whole company" corporate structures
Useful less as a direct competitor and more as *precedent that what you're proposing is legally normal, not a novel legal question*.

- **Newman's Own** — 100% of profits to charity since 1982, ~$600M+ given away, now structured with the company wholly owned by Newman's Own Foundation (enabled by the 2018 **Philanthropic Enterprise Act**, which changed IRS rules that previously capped foundation ownership of a business at 20%).
- **Patagonia** — reorganized in 2022; voting stock to a purpose trust, 98% of non-voting stock to the Holdfast Collective (a 501(c)(4)), routing ~$100M/year to environmental causes. "Earth is now our only shareholder."
- **Humanitix** (Australia) — 100% of ticketing profits to charity; second member of Newman's Own's new "100% for Purpose Club," which is actively recruiting other founders into similar structures.
- Smaller-scale precedent directly on point: an IRS letter ruling (LTR 9309006) addressed **a supermarket chain that set aside 1% of sales annually for donation to public interests in the cities where sales occurred** — structurally almost identical to your model, decades old, already blessed by IRS analysis.

### Category D — Cause-marketing / checkout-donation SaaS vendors
Companies that exist specifically to let *any* retailer bolt on a giving layer: **Change** (getchange.io, powers round-up donations for apps like DoorDash and Uber), **iGive**, **B1G1** (Buy1Give1). These are worth knowing not as competitors but as **potential compliance/infrastructure vendors** — several explicitly sell the commercial-co-venturer compliance work as a service, which is a build-vs-buy question for your Phase 3 round-up layer rather than something you necessarily build in-house.

---

## PART 2 — LEGAL LANDSCAPE: CAN YOU GIVE AWAY 20–30% OF YOUR OWN PROFITS?

**Short answer: yes, unambiguously.** There is no law that prevents a company from donating a large share — even all — of its profits to charity. Newman's Own, Patagonia, Pro-Life Payments, and the IRS-blessed supermarket example above all confirm this is legally normal territory, not a gray area. Nobody needs anyone's permission to be generous with money they own.

*(Everything below is landscape, not advice — a fintech/tax attorney and a CPA need to sign off on the actual structure before real money moves. But the shape of the questions is now mapped, so those conversations will be efficient rather than open-ended.)*

### 2.1 The genuinely important finding: tax deductibility at your scale is capped — and that changes the shape of the decision

This is the one piece of news in this research that should actually change how you think about the model, so I'm putting it first.

As of tax years beginning after **December 31, 2025** (the One Big Beautiful Bill Act, signed July 2025), C-corporation charitable contribution deductions are:
- **Floored at 1%** of taxable income — the first 1% of taxable income's worth of giving is *not deductible at all*, permanently, if total giving that year doesn't exceed the 10% ceiling.
- **Capped at 10%** of taxable income — anything above that carries forward up to 5 years.

**Why this matters for you specifically:** you're planning to give away 20–30% of *company retained margin*, which (depending on how your other expenses net out) is very likely to blow well past the 10% *taxable income* ceiling most years — meaning a large share of your giveback may not be currently deductible as a straight §170 charitable contribution. It carries forward, but if you're giving at this rate every year, the carryforward balloons rather than clears, and unused carryforwards expire worthless after 5 years.

**The alternative worth raising with your tax advisor:** the IRS has a separate line of authority (cited in current tax literature, including that 1993 supermarket letter ruling and a 1954 revenue ruling on a newspaper donating a percentage of subscription receipts) treating a *bona fide, advertised, ongoing percentage-of-sales giving program tied to a genuine business purpose* (customer acquisition, brand differentiation, marketing) as an ordinary and necessary **business expense under §162**, rather than a charitable contribution under §170 — which would not be subject to the 1%/10% caps at all. This is a real, live structuring question, not a loophole you're inventing: the entire "cause marketing" industry (Category D above) exists partly because this distinction has dollar consequences. Whether TheGiveback's dollars are booked as marketing spend vs. charitable contribution is a conversation for your CPA and tax counsel *before* you finalize disbursement mechanics — it plausibly affects millions of dollars of deductibility at your volume.

### 2.2 Commercial co-venturer / cause-marketing law — this is the part that touches your actual product

The moment you advertise "your purchase/transaction generates a donation" — which is the entire point of the "Giveback Certified" badge and merchant dashboard — you're doing what roughly **21–40 states** (depending on definition) regulate as a **"commercial co-venture"** or **"charitable sales promotion."**

Typical requirements where triggered:
- A **written contract** with each specific charity naming the campaign terms, dates, and geography
- **Registration** with the state AG or Secretary of State in ~6 states (California, others) — filing fees generally $100–$500
- **Point-of-advertising disclosures** stating the actual dollar amount or percentage donated (about 11 states require this explicitly)
- **Post-campaign financial reporting**, sometimes jointly signed by you and the charity
- **Surety bonds** ($10,000–$25,000) required in Massachusetts and Alabama specifically before you can run the promotion at all
- The **FTC Act and state "mini-FTC" statutes** independently prohibit deceptive claims regardless of whether a specific co-venture statute applies

This is a real, mapped compliance domain (there's a whole cottage industry — CogencyGlobal, Harbor Compliance, Labyrinth — that exists just to file this paperwork across states), which is good news: it means it's a solvable, budgetable line item, not a novel unknown. But it needs to be built into your Phase 2/3 timeline and legal budget now, not discovered later. Every merchant certification and every piece of "$412 given this month" marketing copy is technically a charitable sales promotion the moment it names a specific cause and a specific dollar/percentage.

### 2.3 Money transmission — the sharp legal line in your whole model sits exactly where you'd hope: between the two pools

This is the most useful thing this research surfaces, because it validates a distinction you already built into the product.

- **Your company's own 20–30% tithe is not money transmission.** You're not moving someone else's money through your business — you're donating money that is legally already yours (retained margin) to a charity of your choosing. This is ordinary corporate philanthropy/grantmaking. No money transmitter license, no FinCEN MSB registration implicated by this piece alone.
- **Consumer round-up funds are a different animal.** The instant you collect money *from a customer* and hold it, even briefly, before forwarding it to a third-party nonprofit, you're much closer to activity that state money transmission laws were written to cover — unless you fit a recognized exemption (the "payment processor" exemption FinCEN has issued rulings on, or the narrower "agent of payee" exemption).

**This is exactly why every single Category B company above is structured the same way**: Pennies *is* the registered charity itself; RoundUp.org routes every dollar through **Our Change Foundation**, a 501(c)(3) donor-advised fund, before it ever reaches the designated nonprofit. This isn't incidental — it's the standard, market-tested way this specific legal problem gets solved, and it matches almost exactly what your own ledger spec already recommends (a DAF-partner route for Phase 3, or registering your own 501(c)(3) for the pool). Worth treating that DAF-or-own-charity decision as load-bearing rather than optional before Round-Up ships publicly.

### 2.4 Corporate structure options, mapped against precedent

| Structure | Precedent | Fit for you |
|---|---|---|
| Ordinary corporate donor — DataOne gives directly to vetted public charities / a DAF, no new entity | Pro-Life Payments, EPS | Simplest, fastest, matches Phase 1–2 needs |
| Own 501(c)(3) private foundation | — | Adds 5%-minimum-annual-distribution rules, excise taxes, self-dealing restrictions — heavier than you need right now |
| Foundation owns the for-profit entity (Newman's Own model) | Newman's Own, Humanitix | Powerful for succession/legacy planning, enabled by the 2018 Philanthropic Enterprise Act, but structurally a much bigger decision than "start giving 25% this year" — a later-stage conversation, not a Phase 1 one |
| Purpose trust / non-voting stock to a nonprofit (Patagonia model) | Patagonia | Same — an ownership-transfer decision, not a giving-program decision; keep this in your back pocket for a future "what happens to DataOne long-term" conversation, not this build |

For where you are right now — proving the plumbing on 5–10 pilot merchants — the first row is almost certainly the right answer, and it's the one every close comparable in Category A actually uses.

### 2.5 Two smaller things worth a line each

- **Fiduciary/authorization:** if DataOne has any outside shareholders, investors, or a board beyond you, committing a recurring 20–30% of margin to charity is a material use of corporate assets that should be formally authorized (which is exactly why the master vision doc already recommends a board resolution — that recommendation gets stronger, not weaker, in light of this research). If you're the sole owner, it's entirely your call, but documenting it in writing still protects the covenant from a future bad quarter.
- **Charity-side due diligence:** any deduction you do take depends on the recipient being a verified 501(c)(3) public charity in good standing — a five-minute IRS Tax Exempt Organization Search check per foundation before the first disbursement, and periodically after, which your ledger spec's "vetting_expires_at" field already anticipates.

---

## Bottom line

You're legally clear to build this. Nothing here is a stop sign. The two things worth putting in front of an actual attorney and CPA before real dollars move, in priority order:

1. **The §162 marketing-expense vs. §170 charitable-contribution characterization question** — at 20–30% of margin, this is likely a real dollar decision, not a technicality.
2. **Whether the consumer round-up layer routes through your own registered charity or a DAF partner** — every working competitor in that space made this same choice, and for the same legal reason.

Everything else (commercial co-venture filings, charity vetting, authorization) is process and paperwork rather than open legal risk.
