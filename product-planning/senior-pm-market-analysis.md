# OpenWindow / Avvalo — Senior PM Market Analysis & Product Recommendations

**Author:** Product review (senior PM lens)
**Date:** 2026-09-19
**Status:** External strategic critique. This is an *opinionated* review meant to challenge, not a founder-approved requirement. It does not modify the interview or planning docs; it reacts to them.
**Inputs read:** `thesis.txt`, and the full `product-planning/session-2026-09-19/` set (brief, overview, vision, plan, workflows, interview, decisions, thesis review, strategy-beyond-telegram-polls). Market claims below are backed by external sources checked on this date (see **Sources**).

---

## 0. TL;DR — my verdict in six lines

1. **The market is genuinely attractive.** Uzbekistan may be one of the best consumer markets on earth *right now* for a Telegram-native social utility: 37M people, half under 27, ~89% internet penetration, Telegram as the dominant messenger, near-zero-cost viral distribution via Mini Apps, and a fast-growing eating-out economy.
2. **The current product framing is the weakest expression of that opportunity.** "A coordination layer that matches group availability for any group's meetup" is a category that has repeatedly failed elsewhere, and it competes directly against a "good enough" Telegram poll.
3. **The real, defensible wedge is *discovery*, not *scheduling*.** "Where should we go out in Tashkent for X?" is the part that is (a) painful, (b) hard to fake with a generic AI prompt, and (c) buildable on real local data (2GIS/Yandex both cover Tashkent and expose venue data).
4. **Cut availability-matching from the MVP.** Per-participant free-time collection is the single biggest funnel leak in this category. Replace it with one-tap RSVP on concrete proposals.
5. **"Any group" is a 3-year platform vision, not a launch target.** Pick one sharp beachhead (young urban friend groups, weekend outings) and win it.
6. **There is a clear monetization path — but only through the discovery framing.** Venue lead-gen / promoted placement / off-peak table filling / later booking commissions. The "pure coordination utility" framing closes that door; the discovery framing opens it.

**One-line reframe:** *Stop building "a shared calendar with a brain." Build "the fastest way for young people in Tashkent to decide where to go out — and actually get everyone there."*

---

## 1. Is there market potential? Yes — and the tailwinds are unusually strong

I want to be precise about *why* this market is good, because it changes what you should build.

### 1.1 A young, mobile, Telegram-native population
- **Population 37.2M, half under age 27** — a genuinely young market entering peak "go out with friends" life stage. Urbanisation ~50%. ([DataReportal / Kursiv](https://uz.kursiv.media/en/2025-11-09/how-internet-is-changing-uzbekistan-key-figures-for-2025/))
- **~89% internet penetration (32.7M users), ~77% smartphone penetration, ~92% mobile connections.** This is not an early-adopter market; it's mainstream-connected. ([DataReportal Uzbekistan 2025](https://datareportal.com/reports/digital-2025-uzbekistan))
- **Telegram is the #1 messenger**, especially among the young and urban; WhatsApp is a distant second (~18% primary use). Uzbekistan is a *top-three* country globally by Telegram channel/chat subscriptions. ([Similarweb](https://www.similarweb.com/blog/research/apps/worldwide-messaging-apps/), [CA Barometer](https://ca-barometer.org/en/publications/which-messaging-apps-are-popular-in-uzbekistan-kyrgyzstan-and-kazakhstan)) Telling detail: **social-media identities (~14.1M, 37.9%) are far fewer than internet users (89%)** — meaning the social graph that matters here lives in Telegram chats, *not* Instagram/Facebook feeds. That is a gift for a Telegram-first product and a warning against over-indexing on Instagram as a discovery source.

**Implication:** Being Telegram-first is not a limitation here — it is the single best distribution decision available. This is the strongest founder call in the docs.

### 1.2 Distribution is nearly free — if you design for it
- Telegram passed **1B MAU / 500M DAU (2025)**; Mini Apps settled to a steady **~150–190M monthly reach** after the 2024 hype and did **$1B+ in transaction volume in 2025**. The **Bot API is free** (no per-message fees). ([Game World Observer](https://gameworldobserver.com/2025/04/04/telegram-mini-apps-monetization-top-games-features), [VoxBooster](https://voxbooster.com/blog/telegram-statistics-2026/))
- In-chat viral loops are real: **Notcoin reached 35M users in ~3 months, ~80% via invites**; Mini-App **user-acquisition costs run ~$0.1–0.5** vs ~$5–20 for comparable web/web3 acquisition. ([ChainPeak](https://medium.com/@chainpeak/2026-telegram-mini-app-marketing-complete-guide-how-ton-ecosystem-projects-go-from-0-to-1m-users-61eb4f752b8d))
- Local truth that validates the whole approach: in Uzbekistan/CIS, **Telegram bots consistently out-perform newly launched standalone mobile apps**, because they plug into an existing habit instead of asking people to install and adopt something new. ([wnexus](https://wnexus.io/the-complete-guide-to-telegram-bot-development-in-2025/))

**Implication:** The growth engine should be *sharing a useful artifact into a group chat*, not app-store installs. This must be designed in from day one (see §6).

### 1.3 The "going out" economy is growing and under-digitised
- Foodservice sales were ~**$1.2B (2023)**; catering-sector revenue is still growing double-digit-ish (**+8.2% YoY reported for Q1 2026**), with **27,312 registered catering enterprises** and a stated national push on hospitality/gastronomy. GDP growth ~6.5% (2024). ([USDA GAIN 2025](https://www.fas.usda.gov/data/gain-report/2025/06/Uzbekistan%20Exporter%20Guide_Tashkent_Uzbekistan%20-%20Republic%20of_UZ2025-0002.pdf), [Zamin](https://zamin.uz/en/uzbekistan/201549-ozbekistonda-kafe-va-restoranlar-daromadi-oshdi.html), [Euronews](https://www.euronews.com/travel/2025/11/07/from-plov-to-fine-dining-uzbekistans-push-for-global-culinary-recognition))
- Discovery today is fragmented: **Afisha.uz** (100k+ users) for events, **iTicket.uz** for tickets, **Yandex Maps / 2GIS** for places. Nobody owns "help my group decide where to go." ([Afisha.uz](https://play.google.com/store/apps/details?id=uz.AfishaMedia.afisha))

**Implication:** There is a growing pool of venues that want customers and a growing pool of young spenders — i.e., a two-sided market with a real money flow to tap later.

### 1.4 A credible local tech ecosystem and capital
- **Uzum** is the country's first unicorn (**$1.5B valuation, Tencent-backed**), running a super-app (marketplace, bank, BNPL, delivery). **Click** and **Payme** are near-ubiquitous payment rails. **IT Park** runs a venture fund. Uzbekistan was the **largest single-year climber in the StartupBlink 2026 index (+19 to #79)**. ([emerging-europe](https://emerging-europe.com/with-superapp-uzum-uzbekistan-gets-its-first-tech-unicorn/), [PR Newswire](https://tools.prnewswire.com/en-us/live/20823/release/20250805EN44452), [Startup Genome](https://startupgenome.com/report/gser2025/uzbekistan-central-asias-fastest-rising-startup-ecosystem))

**Implication:** Payments infrastructure for future monetisation already exists and is trusted. There is local capital and a precedent (Uzum) for consumer-tech scale.

> **Net:** the *market and distribution* thesis is strong — arguably strong enough to justify building. The risk is almost entirely in the *product framing*, which is what the rest of this doc attacks.

---

## 2. The hard truths — where the current direction is fragile

The planning docs are unusually honest (the strategy note already admits "a Telegram poll can be enough"). I'm going to push that honesty further, because these are the things that kill products like this.

### 2.1 You're building in a category with a graveyard
Availability-matching / "who's free" apps (HangTime, Free to Hang, DayGap, and many others in your own analog list) have overwhelmingly failed to retain. The consumer social-planning products that actually *broke out* did the opposite thing:
- **Partiful** — the current category winner — raised **$27.4M (a16z, ~$140M valuation)** and hit **~500k MAU, +400% YoY, ~5M new users in H1 2025, Google "Best App 2024."** It is a **host-driven invitation / RSVP / delight** product. It does **not** ask everyone for their free time. ([Sacra](https://sacra.com/c/partiful/), [CNBC](https://www.cnbc.com/2025/04/19/meet-partiful-the-gen-z-party-planning-staple-thats-taking-on-apple.html))

**Lesson:** the winning primitive is *"someone proposes something concrete and others say yes,"* not *"everyone declares availability and the system computes an intersection."* Your MVP still leans on per-meetup availability collection (D10). That is the exact mechanic the graveyard is full of.

### 2.2 Coordination may not be the real blocker — willingness is
The founding problem is "groups want to meet but stall on when/where, made worse by passive members." I'd challenge the causal story: **for most casual outings, the blocker isn't computing an overlap — it's that nobody has the energy to champion a concrete plan, and "passive" often means "mildly indifferent," not "available but un-coordinated."** Your own thesis review flags this ("free time ≠ willingness"). A tool that removes coordination friction does nothing for indifference. This is the difference between a *painkiller* and a *vitamin*, and it's the #1 thing to validate before building (see §8).

### 2.3 Two workflows × "any group" × two decision modes = an unfocused MVP
Right now the launch scope is: *any group* (friends/family/colleagues/communities) × *any occasion* × *known-place OR AI-assisted* × *voting OR initiator-choice* × *Uzbek OR Russian*. That's a lot of forks for a v1 that hasn't proven a single loop. Families coordinating a holiday, colleagues booking a team lunch, and 22-year-olds picking a Friday café are **three different jobs with different willingness, cadence, and data**. "Any group" is a platform aspiration; as a launch target it guarantees a blurry product that's excellent for no one.

> I'm explicitly disagreeing with a recorded founder decision here (D16, "any group"). That's the founder's call — but my strong recommendation is to keep the *platform* generic underneath while pointing the *launch* at one beachhead. See §4.

### 2.4 The AI-discovery promise is simultaneously the best idea and the biggest execution risk
"AI asks 3 questions and searches the internet (Instagram, etc.)" is where the differentiation lives — *and* where you can most easily ship something worse than a ChatGPT prompt. Failure modes:
- **Hallucinated or stale venues** (a closed/wrong-priced place recommended once = trust gone forever). In a small city where word travels, one bad rec is expensive.
- **Instagram as the primary source is the wrong bet** — access is unreliable, and (per §1.1) it's not even where most Uzbeks are. The docs already mark this "unvalidated"; I'd go further and say *don't build on it.*
- **A generic "5 restaurants near you" list is not a product.** If a single general-AI prompt matches your output, you have no wedge.

The good news, which the docs under-weight: **the structured data to do this well already exists locally.** 2GIS launched in Uzbekistan in 2019, covers Tashkent, and exposes a catalog API (name, address, hours, phone, rating, reviews, categories); Yandex Maps has comparable coverage. ([2gis.uz](https://2gis.uz/), [spot.uz](https://www.spot.uz/ru/2019/08/30/2gis/), [2GIS catalog API via Apify](https://apify.com/haketa/2gis-scraper/api)) This turns "venue data" from an *unvalidated dependency* into a *buildable moat*.

### 2.5 Frequency & retention: planning is episodic
People plan outings weekly-to-monthly, not daily. Low CAC (§1.2) helps, but a product with no reason to open between plans churns. You need a lightweight *always-on surface* (see §5.4) or you'll re-acquire the same users repeatedly.

### 2.6 Platform concentration risk
Betting everything on Telegram means betting on Telegram's policy, API terms, and Mini-App discovery mechanics. Acceptable — even correct — at this stage, but keep the domain model portable so a standalone/web path (already in the roadmap) is a genuine option, not a rewrite.

### 2.7 Monetization is deferred *and* the chosen category is hard to monetize
Deferring pricing is fine. But "free group-coordination utility" is *structurally* one of the hardest things to monetize (utility, episodic, no inventory). If you never reframe, you back yourself into ads or nothing. The discovery reframe (§5) is what gives you a supply side that will actually pay.

---

## 3. The reframe (the single most important section)

> **Move the center of gravity from "coordinating people's time" to "deciding where to go — and pulling the group along."**

Your original thesis had a great primitive — *"temporary availability as expiring inventory."* You aimed it at the **demand side** (people's free time), which is low-value and hard to fill. **Point the same primitive at the supply side: venues' empty tables and quiet nights.** Restaurants and activity venues in Tashkent have expiring inventory *every single evening*, they want to fill it, and (unlike your users' free evenings) **they will pay to fill it.** That is where the "inventory" idea becomes a business.

So the product stack becomes:

1. **Discovery (the wedge & the value):** "Tell me what kind of night you want → get a small, trustworthy, source-linked shortlist of real Tashkent places." Buildable on 2GIS/Yandex + a curated catalog. This delivers value to *one person, before any group exists* — which is exactly the "get value solo first" requirement the strategy note calls for.
2. **Coordination (the sharing loop):** share that shortlist into the Telegram group; members react/RSVP to concrete options with one tap. This is the viral mechanic and the "get everyone there" payoff — *without* upfront availability forms.
3. **Memory (the retention layer):** remember what this group liked, what's new, what's on this weekend — the reason to come back.
4. **Supply/monetization (the business, later):** promoted placements, off-peak deals, and eventually booking — filling venues' expiring inventory.

Positioning line to test (plain language, per the strategy note's own advice): **"Qayerga boramiz?" / "Куда пойдём?"** — *"Where should we go?"* Not "AI coordination layer," not "availability graph."

---

## 4. Pick a beachhead (my recommended launch ICP)

**Launch target:** friend groups, ~18–27, in Tashkent, planning **weekend eat / hang / light-activity outings** (café, restaurant, bowling/billiards, kino, chaykhana, weekend spot). Uzbek + Russian.

Why this and not "any group":
- It's the segment with the **highest frequency**, the **most Telegram-native behavior**, the **lowest willingness-to-organise** (your actual pain), and the **tightest fit with the growing café economy**.
- It's a **coherent catalog** to curate (you can't credibly curate "any occasion for any group" at launch).
- Families/holiday-trips/colleagues are all reachable *later* on the same platform — but they need different data, cadence, and trust, and would blur v1.

Keep the data model group-type-agnostic; just **point acquisition, catalog, and copy at this one segment** until the loop works. The founder's "big product for everyone" ambition is served *better* by nailing a beachhead than by launching broad.

---

## 5. Prioritized product recommendations

Framed as P0 (do for MVP), P1 (fast-follow), P2 (later), with the reasoning, so you can disagree with specifics.

### P0 — the MVP that proves the wedge
- **P0.1 — Hero flow = discovery, 2–3 taps, not a chat.** Occasion/vibe → budget band → area. Return **3–5 concrete places**, each with: what it is, area, a *sourced* price signal (or clearly-labelled estimate), hours, rating/really-short review snippet, and a **source link**. Never invent. Mark anything unverified. *(This is Workflow B, sharpened; it should be the default, and it should work for a single user with no group.)*
- **P0.2 — Cut per-participant availability from MVP.** Replace with **one-tap RSVP on concrete proposals** ("Fri 20:00 @ X — I'm in / can't / suggest another"). Show honest state ("4 in, 2 haven't answered") — never count silence as yes. *(Directly contradicts D10; that's deliberate — validate availability-collection separately before committing to it.)*
- **P0.3 — Keep the known-place path as a 10-second utility.** "We already know where — just get everyone to pick a time and confirm." No AI questions. This is the fast lane and a good low-friction on-ramp. *(Workflow A — good, keep it.)*
- **P0.4 — Build the Tashkent venue spine.** Ingest 2GIS/Yandex catalog data + a hand-curated seed set (a few hundred quality places across the launch occasions). Store source + last-checked timestamp on every fact. **This is the asset competitors and a raw LLM prompt can't cheaply replicate.**
- **P0.5 — Shareable-by-design.** Every shortlist and plan is a Mini-App deep link that renders as a rich card in the group chat, with one-tap "open / I'm in / join." The share *is* the growth loop (§6).
- **P0.6 — Trust UI.** Source links, "verified vs estimated" labels, and a one-tap "this is wrong" that improves the catalog. In a small city, trust is the moat.

### P1 — fast-follow once the loop shows life
- **P1.1 — Group memory / taste profile** (liked places, "you haven't done X in a while," novelty vs favourite). The retention layer.
- **P1.2 — Lightweight reminders** for *confirmed* plans only (founder's "maybe reminders," scoped tightly). Do **not** make reminders the differentiator.
- **P1.3 — "What's on this weekend in Tashkent"** always-on surface (ties into Afisha/iTicket-type content) so the app has a reason to be opened between plans.
- **P1.4 — Availability collection as an *optional* power feature**, *if and only if* pilots show groups will actually do it. Prove it earns its friction.

### P2 — platform expansion (the founder's big vision, sequenced)
- Other cities → other group types (families/holidays, teams) → standalone web app → calendar integration → **booking** (which unlocks the strongest monetization). Each is a deliberate step *after* the core loop retains.

**What I'd explicitly NOT build for a while:** a full calendar, a social feed, stranger/public discovery, an expert/creator marketplace, a bench-capacity marketplace (all in the original thesis). They're distractions from the one loop that has to work first.

---

## 6. Go-to-market & the viral loop (design it, don't hope for it)

The only cheap growth here is in-chat virality. Engineer it:

1. **Solo value first:** the initiator gets a genuinely useful shortlist *before* recruiting anyone. (Removes the cold-start "empty group" problem.)
2. **The share is the ad:** shortlist/plan cards posted to the group carry a "planned with @AvvaloBot — open" footer and a one-tap join. No install wall.
3. **Cross-group spread:** a participant in Group A later *initiates* in Group B. Track this explicitly as your K-factor; it's the real engine, not raw shares.
4. **Seed deliberately:** launch inside 10–30 real Tashkent friend groups you can reach directly; over-serve them (concierge, §8) so the first experience is excellent.
5. **Instrument the loop:** shortlist→share→RSVP→confirmed→completed→*next initiator*. If step "next initiator" doesn't fire, you have distribution but no engine — fix that before spending on anything else.

Given Mini-App UA can be ~$0.1–0.5, if the loop works at all the economics are extraordinary. If it doesn't, no ad budget will save it — so prove the loop before spending.

---

## 7. Monetization thesis (sketch it now, charge later)

Keep launch free (agreed). But *design toward* a business, via the supply side:

| Stage | Mechanism | Why it works here |
| --- | --- | --- |
| Now | Free; instrument everything | Build demand + data; no willingness-to-pay risk yet |
| Early | **Promoted / featured venues** in shortlists (clearly labelled) | Venues already advertise on Yandex/2GIS/Afisha; you offer *intent-qualified groups* |
| Early–mid | **Off-peak deals / "fill tonight"** — venues surface discounts for quiet slots | Directly monetises *venues' expiring inventory* — the thesis primitive, aimed where the money is |
| Mid | **Booking / reservations take-rate** | The deferred "booking" feature becomes the revenue event; rails (Click/Payme/Uzum) already trusted |
| Later | **B2B / community tiers, data insights** | Once you own local "going-out intent," aggregate demand signals have value |

The point: **the discovery reframe gives you paying customers (venues). The pure-coordination framing does not.** Deferring the *decision* is fine; foreclosing the *option* by framing is not.

---

## 8. Validation plan — spend 4–6 weeks before writing recommendation code

The strategy note already proposes a concierge pilot; I'm sharpening it into a kill/continue test.

**Concierge (Wizard-of-Oz) bot, 10–15 Tashkent friend groups:**
- A human curates the shortlist behind a plain Telegram bot. **No recommendation engine yet.** You're testing demand and the loop, not your code.
- For each real (already-wanted) outing, measure the funnel: request → shortlist delivered → **shared to group** → RSVPs → **confirmed plan** → **completed meetup** → **someone initiates again**.

**The three questions that decide everything:**
1. **Painkiller or vitamin?** Do groups reach a *confirmed, completed* plan they say wouldn't have happened otherwise? (Attacks §2.2.)
2. **Is the shortlist share-worthy?** Do initiators actually forward it *without prompting*? (Attacks §2.4 — this is your real differentiator test.)
3. **Does the loop close?** Does a participant later become an initiator in another group? (Attacks §6 — the growth engine.)

**Provisional kill/continue criteria (set real numbers with the founder before starting):**
- **Continue** if a clear majority of pilot groups complete a plan *and* initiators share shortlists unprompted *and* at least a few cross-group initiations occur.
- **Pivot** if they like the shortlist but ignore coordination → make discovery-and-share the whole product.
- **Kill/rethink** if plans complete at baseline rates with or without you → the problem was willingness, not coordination, and this product doesn't fix that.

Record every bit of manual effort — if a human had to chase every RSVP and verify every venue, that cost is part of the real product.

---

## 9. Metrics that matter

**North star:** *completed meetups the product plausibly caused* (vs a baseline / self-reported "would this have happened anyway?"). Everything else is a supporting funnel metric.

- **Activation (solo):** % of initiators who get a shortlist they rate useful (target: value in <1 shortlist, before any group step).
- **Share rate:** % of shortlists forwarded to a group unprompted. *(Your differentiation signal.)*
- **Coordination conversion:** shortlist → concrete proposal → confirmed plan.
- **Completion:** confirmed → actually happened (one-tap post-hoc check).
- **K-factor / next-initiator rate:** participants who later initiate. *(Your growth engine.)*
- **Repeat rate:** groups that plan again within N weeks.
- **Trust guardrails:** wrong/stale venue reports per 100 recs; unwanted-notification complaints.

Avoid vanity metrics (installs, "AI chats," poll responses). The strategy note is right that daily use is the wrong bar — measure *return at the next occasion*, not DAU.

---

## 10. Risk register & explicit kill criteria

| Risk | Severity | Mitigation |
| --- | --- | --- |
| Coordination isn't the real blocker (willingness is) | **High** | §8 concierge test *before* building; kill criteria defined |
| Availability-collection friction kills the funnel | High | Cut it from MVP (P0.2); RSVP on concrete options instead |
| Bad/stale venue recs destroy trust | High | Structured 2GIS/Yandex spine + curation + source labels + "report wrong" |
| "Any group / any occasion" dilutes v1 | High | Beachhead ICP (§4); keep platform generic underneath |
| Weak differentiation vs Telegram poll + ChatGPT | High | Local data moat + share loop; if a raw LLM prompt matches you, you have no wedge |
| No monetisation path | Medium | Discovery reframe → venue supply side (§7) |
| Episodic use → churn | Medium | Always-on "what's on this weekend" surface (P1.3) |
| Telegram platform dependency | Medium | Portable domain model; web path already roadmapped |
| Notification fatigue | Medium | Only act when there's a concrete, useful action; confirmed-plan reminders only |

**When to walk away:** if the concierge pilot shows groups don't complete more plans *and* don't share shortlists, this is a vitamin. Don't paper over it with more AI, prettier cards, or booking — those are the exact "don't add features to compensate for a weak core" traps your own strategy note warns about.

---

## 11. Competitive snapshot (for orientation, not exhaustive)

| Player | What it really is | Read-across for you |
| --- | --- | --- |
| **Telegram polls** (native, incl. 2026 media/location/suggestions) | Free, zero-friction, already in the chat | Your true baseline. You must remove *real work*, not add gloss |
| **Partiful** (~500k MAU, +400% YoY, a16z) | Host-driven invitations/RSVP + delight | Proof the winning primitive is *propose→RSVP*, not availability-matching |
| **Doodle / when2meet / Howbout** | Time-poll / shared-availability utilities | The graveyard pattern — utility, low retention, no local discovery |
| **Yandex Maps / 2GIS (Tashkent)** | Place data + reviews | Your *data source*, not a competitor. The moat is turning it into group decisions |
| **Afisha.uz / iTicket.uz** | Event listings / ticketing | Adjacent; potential content + partnership, not head-to-head |
| **Uzum / Click / Payme** | Super-app / payments | Future rails (and potential acquirers) for booking/monetisation |
| ChatGPT / generic AI | On-demand recs | The bar for your discovery output. Beat it with *fresh, local, verified, shareable* |

---

## 12. Direct answers to the founder's two questions

**"Does it have potential in the market?"**
Yes — the *market* has strong, well-evidenced potential (young, connected, Telegram-native, growing going-out economy, near-free distribution, trusted payment rails). But potential is in the *opportunity*, not yet in the *current product framing*. The framing most likely to realise the potential is a **Tashkent-first, Telegram-native "where should we go out" discovery product for young friend groups, with light one-tap coordination and a venue-supply monetization path** — not an availability-matching coordinator for "any group."

**"How can we improve / what should we change?"** (ranked)
1. **Reframe the hero from scheduling to discovery.** Lead with "where should we go," deliver value to one person before the group exists. (§3, P0.1)
2. **Cut per-participant availability collection; use one-tap RSVP on concrete options.** (P0.2)
3. **Narrow the launch to one ICP** (young Tashkent friend groups, weekend outings); keep the platform generic underneath. (§4)
4. **Treat local venue data (2GIS/Yandex + curation) as the core asset/moat**, not an unvalidated dependency; stop centring Instagram. (P0.4, §2.4)
5. **Engineer the in-chat viral loop explicitly** and measure next-initiator K-factor. (§6)
6. **Sketch the venue-side monetization now** even while free. (§7)
7. **Run the 4–6 week concierge pilot with real kill/continue criteria before building the recommendation engine.** (§8)
8. **Use plain local-language positioning** ("Qayerga boramiz? / Куда пойдём?"), and align the brand (repo is *Avvalo*; docs say *OpenWindow* — pick one, ideally the local one). (§3)

---

## Sources
- [DataReportal — Digital 2025: Uzbekistan](https://datareportal.com/reports/digital-2025-uzbekistan)
- [Kursiv Media — How the Internet is changing Uzbekistan: key figures for 2025](https://uz.kursiv.media/en/2025-11-09/how-internet-is-changing-uzbekistan-key-figures-for-2025/)
- [Similarweb — Most popular messaging apps 2025](https://www.similarweb.com/blog/research/apps/worldwide-messaging-apps/)
- [CA Barometer — Messaging apps in Uzbekistan, Kyrgyzstan, Kazakhstan](https://ca-barometer.org/en/publications/which-messaging-apps-are-popular-in-uzbekistan-kyrgyzstan-and-kazakhstan)
- [Game World Observer — Telegram Mini Apps: features, monetization](https://gameworldobserver.com/2025/04/04/telegram-mini-apps-monetization-top-games-features)
- [VoxBooster — Telegram statistics 2026](https://voxbooster.com/blog/telegram-statistics-2026/)
- [ChainPeak — Telegram Mini-App marketing guide (0→1M users)](https://medium.com/@chainpeak/2026-telegram-mini-app-marketing-complete-guide-how-ton-ecosystem-projects-go-from-0-to-1m-users-61eb4f752b8d)
- [wnexus — Telegram bot development guide 2025 (CIS/Uzbekistan)](https://wnexus.io/the-complete-guide-to-telegram-bot-development-in-2025/)
- [emerging-europe — Uzum, Uzbekistan's first tech unicorn](https://emerging-europe.com/with-superapp-uzum-uzbekistan-gets-its-first-tech-unicorn/)
- [PR Newswire — Uzum $70M raise, $1.5B valuation (Tencent)](https://tools.prnewswire.com/en-us/live/20823/release/20250805EN44452)
- [Startup Genome — Uzbekistan: Central Asia's fastest-rising ecosystem](https://startupgenome.com/report/gser2025/uzbekistan-central-asias-fastest-rising-startup-ecosystem)
- [Sacra — Partiful valuation & funding](https://sacra.com/c/partiful/)
- [CNBC — Partiful, the Gen Z party-planning staple](https://www.cnbc.com/2025/04/19/meet-partiful-the-gen-z-party-planning-staple-thats-taking-on-apple.html)
- [2GIS Uzbekistan](https://2gis.uz/) · [Spot.uz — 2GIS launched in Uzbekistan (2019)](https://www.spot.uz/ru/2019/08/30/2gis/) · [2GIS catalog API (Apify)](https://apify.com/haketa/2gis-scraper/api)
- [USDA GAIN — Uzbekistan Exporter Guide 2025 (foodservice)](https://www.fas.usda.gov/data/gain-report/2025/06/Uzbekistan%20Exporter%20Guide_Tashkent_Uzbekistan%20-%20Republic%20of_UZ2025-0002.pdf)
- [Zamin — Uzbekistan cafe/restaurant revenue growth](https://zamin.uz/en/uzbekistan/201549-ozbekistonda-kafe-va-restoranlar-daromadi-oshdi.html)
- [Euronews — Uzbekistan's culinary push / Gastro Forum Tashkent 2025](https://www.euronews.com/travel/2025/11/07/from-plov-to-fine-dining-uzbekistans-push-for-global-culinary-recognition)
- [Afisha.uz (Google Play)](https://play.google.com/store/apps/details?id=uz.AfishaMedia.afisha) · [iTicket.UZ](https://iticket.uz/en/events)

*This document is analysis and opinion for discussion. It intentionally challenges several recorded founder decisions (notably "any group" and per-meetup availability collection); those remain the founder's to decide. Market figures are third-party estimates cited as directional evidence, not audited data.*
