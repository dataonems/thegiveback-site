# TheGiveback — Owner Checklist
### Chris Humphrey · Updated July 2026

---

## 🔴 CRITICAL BLOCKERS — Nothing moves without these

- [ ] **Write the covenant today**
  Write and sign a document committing 30% of DataOne's retained margin to Colombian foundations monthly. Board resolution or operating agreement amendment. Signed and dated. This is the legal foundation everything else rests on.

- [ ] **Book the CPA call this week**
  §162 business expense vs §170 charitable deduction. At 30% of margin you will exceed the standard charitable deduction cap. The CPA needs to determine the right tax treatment before the first dollar disbursed. Potentially millions in deductibility difference over the platform's life.

- [ ] **Confirm minimum processing threshold for free hardware**
  The site currently says "TBD." You need a real number before any merchant conversation. Once decided, send it and the site is updated in 5 minutes.

---

## 🟡 LEGAL & FINANCIAL — Complete before first disbursement

- [ ] Retain an attorney (corporate + nonprofit counsel)
- [ ] Have attorney review covenant document once drafted
- [ ] Confirm ASODISVALLE's Colombian legal structure (NIT number needed for site + ledger)
- [ ] Confirm Rescue + Rise's Colombian legal structure (NIT + 501c3 status if applicable)
- [ ] Begin 501(c)(3) application process at Phase 2 launch (not now — use DAF partner for Phase 3 consumer round-up)
- [ ] Select DAF partner for Phase 3 consumer round-up (Fidelity Charitable, Schwab, or specialist)

---

## 🟡 PARTNERSHIPS — Conversations to have this week

- [ ] **Call Jorge → ASODISVALLE intro**
  Message: "Jorge, I'm finally building TheGiveback. I want ASODISVALLE to be one of our first two pilot foundations. Can you set up a call with Jeison?"
  The ask: pilot foundation, monthly disbursements, monthly outcome post, GiveHub access.

- [ ] **Call your pastor → Rescue + Rise intro**
  Message: "Pastor, I want Rescue + Rise to be one of our first two pilot foundations. Can you make the introduction and tell them what you know about me and what I'm building?"

- [ ] **Plan the Cali trip to meet Jeison**
  Before the trip: confirm partnership interest through Jorge.
  On the trip: tour the facility, film a conversation with Jeison, get student photos (with permission), understand their monthly funding needs.
  After the trip: bring back a signed partnership letter of intent.

- [ ] **Call Derek Young at Robotica**
  Schedule the IP review for OTIS integration. This is a 60–90 day process. Every day it doesn't start is a day the verified impact layer is delayed.

---

## 📸 PHOTOS & CONTENT — Needed before site goes live

### Photos you already have — organize and send this week:
- [ ] **Christian entrepreneur group photos (Saturday meetings)**
  Best use: Our Story page (Chris in community in Medellín), Get Started sidebar
  What to look for: candid moments, real conversations, not posed group shots

- [ ] **Foundation work photos — kids programs**
  Best use: Foundations page (replace placeholder boxes)
  Need: which foundation, what city, approximate date, brief description of program
  One strong candid > five posed photos

### Photos you need to get:
- [ ] **Founder photo — Chris in Medellín**
  Where: outdoors in the city, somewhere recognizable as Colombia
  Style: candid/working, not a headshot
  Optional but powerful: with Mia
  Send to: add to site immediately

- [ ] **ASODISVALLE photos** (from Cali trip or via Jorge)
  Needed: facility, students, Jeison, the university
  Permission: confirm photo rights with foundation before using publicly

- [ ] **Rescue + Rise photos** (via pastor)
  Needed: mothers program, babies, community setting
  Permission: confirm photo rights before using

### Video (high priority, low cost):
- [ ] **90-second founder video**
  Film on phone, outdoors in Medellín, in your own words
  Script: who you are, why Colombia, why now, what TheGiveback does, one CTA
  English AND Spanish versions (same content, different language)
  No production needed. Authentic > polished.

- [ ] **Jeison conversation video** (from Cali trip)
  5–10 minutes, informal, in Spanish
  Key questions: What does predictable monthly funding mean for ASODISVALLE? What do you wish the Colombian diaspora in the US understood about the work here?

---

## 📱 SITE — Tasks only Chris can complete

- [ ] **Add real phone number + WhatsApp link**
  Goes in: Get Started page contact box, footer, nav (mobile)
  Format: WhatsApp link = https://wa.me/[number]
  This is the highest-converting single addition to the site right now.

- [ ] **Decide on the live counter display**
  Option A: Hide counter entirely until first disbursement, then reveal
  Option B: Show "First disbursement: [Month] 2026" as a countdown
  Option C: Show $0 with honest "Coming soon" note (current — weakest option)
  Recommendation: Option B

- [ ] **Confirm both foundation partnerships before publishing foundation cards publicly**
  Right now both cards are placeholder. Do not publish real foundation names publicly until partnership is confirmed with each foundation.

- [ ] **Confirm the covenant document is in place**
  Send signed covenant scan to file, then update site copy from "written into our operating agreement" to accurate legal description.

---

## 🌐 TECHNICAL — For your developer (or Ivan)

- [ ] **Wire the Get Started form to Netlify Forms**
  In the HTML form tag, add: `name="contact" netlify`
  That's it. Submissions route to your Netlify email immediately.
  Time: 20 minutes. Highest ROI of any technical task.

- [ ] **Deploy to Netlify**
  Upload TheGiveback_Site_V4.html as index.html
  Connect custom domain: thegiveback.org
  Enable HTTPS (automatic with Netlify)

- [ ] **Set up a simple email auto-responder**
  When form submits → Mailchimp or ConvertKit free tier sends:
  Email 1 (immediate): Confirmation + story page link + foundation overview
  Email 2 (Day 3): How It Works deep dive + math
  Email 3 (Day 7): Follow-up + WhatsApp CTA

- [ ] **Add Google Analytics or Plausible**
  Need to know: which pages get traffic, where people drop off, which CTA converts
  Plausible is privacy-first, GDPR compliant, better for Colombian/diaspora audience

- [ ] **Create public ledger placeholder page**
  URL: thegiveback.org/ledger
  Content: "The public ledger launches with the first disbursement. Here is the signed covenant document." + link to covenant PDF
  This makes the promise feel real before the first dollar moves.

- [ ] **Create the covenant page**
  URL: thegiveback.org/covenant
  Content: Scan or PDF of signed covenant document + plain English explanation
  This is what you show Jeison and your pastor when they ask "how do we know this is permanent?"

- [ ] **Set up WhatsApp Business account**
  Link to site, enable auto-reply, set business hours
  This is where most Colombian diaspora merchants will actually reach you first

---

## 🗓 WEEKLY MEETING — Ivan facilitates every Monday 9am

**Who needs to be in the room:**
- Chris (final decisions, partnership calls, covenant)
- Ivan (project management, task board, Academy track)
- Lead engineer (when hired — ledger, form backend, tech decisions)
- Attorney (as needed for covenant and legal structure)
- CPA (as needed before first disbursement)

**Agenda every week:**
1. Task board review (5 min) — status on every item above
2. Blocker review (10 min) — covenant, CPA, attorney
3. Pilot cohort progress (15 min) — merchant and foundation list
4. Engineering update (15 min) — ledger, form, Netlify
5. Ivan update (10 min) — Academy, content, English school
6. Owners named for every open item (5 min)

---

## ✅ PHASE 1 DEFINITION OF DONE

The platform is live when:
1. Covenant is written, signed, and publicly linked
2. 5 pilot merchants are processing through DataOne on dual pricing
3. 2–3 pilot foundations have signed partnership letters
4. Internal ledger is tracking every transaction
5. First real disbursement has been made — specific dollar amount, specific foundation, receipt in hand
6. Public ledger page shows that first entry
7. First merchant impact report has been sent
8. Get Started form is wired and responding within 24 hours

**Do not announce. Do not launch publicly. Make the first disbursement first.**
Then the site becomes a document of something real, not a promise of something future.

---

## 📋 CONTENT NEEDED FROM BOTH FOUNDATIONS (before publishing)

For each foundation:
- [ ] Official name (exact legal name as registered)
- [ ] NIT number (Colombian tax ID)
- [ ] Legal representative name and title
- [ ] Mission statement (their own words, in Spanish)
- [ ] 3 program outcome statistics (specific, verified)
- [ ] 2–3 high-resolution photos (with usage permission)
- [ ] Monthly reporting agreement (they agree to publish one outcome post per disbursement)
- [ ] WhatsApp contact for DataOne's disbursement team

---

*Last updated: July 2026 · Owner: Chris Humphrey · PM: Ivan*
*Next review: Monday weekly meeting*
