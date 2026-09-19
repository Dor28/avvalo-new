# Product plan

Version 0.8 — updated 2026-09-20. Dates, staffing, budget, and numeric targets await founder input.

Confirmed direction: Uzbekistan; groups struggling to choose when and where to meet during holidays; AI helping select suitable times and places; ambition for a larger product helping people meet and decide faster.

Confirmed planning flow: a person initiates with a known place or requests AI assistance; members supply availability for that meetup. In the assisted path, AI asks three questions and searches online, with social media including Instagram among desired sources. Recommendations consider preferences, recent meetups, and availability. Input order and who answers are undecided. Autonomous initiation is superseded for the initial experience. Calendar integration is a possible later expansion.

Initial platform direction: Telegram Mini App, with a group bot as a possible companion. A standalone web app is intended later. Design the member journey around Telegram first, then verify current platform capabilities before specifying integrations or implementation. Define group entry, invitations, private inputs, proposals, responses, and notification behavior. No platform implementation is underway in this discovery session.

## Platform sequence

1. **Initial versions — Telegram Mini App:** confirmed direction. Define and validate the known-place and assisted workflows here.
2. **Possible group bot in initial versions:** tentative founder idea, not a required integration yet. A proposed role is to provide entry to the Mini App and share planning updates; exact responsibilities and feasibility remain open.
3. **Later — standalone web app:** founder's intended expansion. Timing, feature scope, account continuity, and how it works alongside Telegram remain undecided.

The group bot suggests existing Telegram groups as a starting context, but membership and invitation rules still need definition. Do not treat bot participation as access to historical chat messages or meetup history.

## Phase 1: validate the problem across group types

Interview the founder, then prospective members and organizers from the intended audience. Collect recent planning stories, existing workarounds, failed plans, meeting frequency, and recruitment access.

Founder direction, 2026-09-20: serve any group arranging a meetup in Uzbekistan, including friends, families, colleagues, and communities. Discovery must extend beyond the founder's own group. Recruit across different group types and compare shared coordination problems and segment-specific needs. Pilot composition is a validation choice, not a restriction of the agreed audience.

Next discovery priorities: preference setup; source and intended use of recent meetup history; details of per-meetup availability entry; first city and group profile; meaning and frequency of holiday occasions; why members remain passive; and whether the group prefers accepting one proposal or voting on several. Include passive members in interviews, not only organizers.

Define both workflows in [workflows.md](workflows.md). The founder has deferred who answers the three AI questions. Clarify initial outing types and group profile next, then compare initiator-only and individual-answer prototypes for effort, response delays, and recommendation fit. Question content, relationship to availability entry, and saved preferences remain unconfirmed.

Outputs: shared and group-specific needs, concrete problem statement, pilot recruitment approach, revised overview and vision, and an assumption register.

Decision gate: establish that the audience wants more meetups and that coordination is a material obstacle. If willingness or competing priorities dominate, revise the promise before building.

## Phase 2: test the behavior with a small pilot

Recruit a small number of existing groups; determine group count and pilot duration after learning access and typical meeting cadence. Explain any manual assistance. When a member initiates planning, collect availability specifically for that meetup, minimal preferences, and recent meetup history where available; identify suitable time/place options and deliver concrete proposals through the group's existing channel. Test the first-meetup experience with no stored history as well as repeated use. Measure how many invited members supply availability and how much effort this takes.

Record participation effort, response times, confirmed plans, completed meetups, declines, stale availability, cancellations, and organizer interventions. Establish a baseline before making proposals. Ask whether a meetup was already planned; treat self-reported additional meetups as an estimate.

Pilot both known-place coordination and assisted discovery. For discovery, test whether three questions produce enough information for useful results. Once the city is chosen, research and test internet/social source access, local coverage, freshness, and accuracy of essential venue details. Record search failures and manual work. Instagram access is an unvalidated dependency, not a guaranteed integration.

For the founder's decision-speed goal, record elapsed time from planning start to an explicitly agreed time and place. Record unresolved or abandoned attempts too. Compare similar occasions; faster agreement alone does not establish a useful meetup.

Decision gate: groups repeatedly act on proposals and are willing to keep providing the required inputs. Set explicit pass/revise/stop thresholds before the pilot starts, after baseline and feasibility are known.

## Phase 3: define the smallest automated product

Candidate scope, pending pilot evidence:

- Group invitation and member participation.
- Member-initiated meetup request.
- Known-place path and AI-assisted discovery path.
- Three-question AI interaction in the assisted path; question content and respondent rules to be defined.
- Internet place search, with social media among desired sources; source integrations require feasibility validation.
- Per-meetup availability entry. Private visibility, expiry, and easy updates are proposed details to validate.
- Essential activity preferences and constraints.
- Recent meetup history used in time/place suggestions, with collection and ranking behavior to be defined.
- Overlap detection and simple proposal ranking.
- A concrete proposal with acceptance and a response deadline.
- Flexible decision methods: group voting or initiator selection after responses. Define a simple, visible rule per meetup; the selector and default remain open.
- Transparent attendance threshold and confirmation state.
- Cancellation or changed-availability handling.
- Help members remember meetups. Proposed initial behavior: reminders tied to a confirmed plan; founder clarification on scope is pending. Define recipients, timing, controls, and handling of changed/cancelled plans before implementation. Delivery capability remains to be verified.
- Meetup occurrence check and lightweight feedback.
- Basic visibility controls, leaving a group, and deleting supplied data.

Resolve before implementation: Telegram entry and notification flow; per-meetup date range, time-slot format, and availability updates; preference setup; meetup history capture and missing-data behavior; required versus optional members; hard versus soft constraints; handling silence; number of options; reminder frequency; who arranges bookings; data visibility; and what invalidates a confirmed plan.

AI assistance with three questions and internet discovery is part of the founder's direction, alongside a known-place workflow. Validate whether assistance helps the group reach agreement; the technical approach is still open. The founder selected per-meetup availability first, with calendar integration as a possible later expansion. Calendar integration is outside initial scope and has no committed date. Automated bookings and sophisticated fairness scoring should earn inclusion through evidence that they are necessary for the core experience.

## Phase 4: evaluate repeated value and economics

Founder-prioritized value: choosing a better date, choosing a better place, and remembering meetups. Clarify whether reminders concern confirmed plans, arranging the next meetup, or both. Prompts to arrange another meetup would not change the confirmed person-initiated planning rule. Validate the simplest usable form of each agreed workflow.

Measure repeat use across multiple opportunities, completed meetups per active group, member effort, recurring exclusion, proposal muting, and continued availability updates. Interview both active groups and groups that stop.

Investigate who would pay, what they value, and the cost of serving a group, including activity data and manual support. Select monetization experiments only after identifying a plausible buyer and value exchange.

## Measurement notes

Primary outcome: estimated additional completed meetups attributable to the product. Distinguish an opportunity, proposal, confirmation, and completed meetup as separate events.

Supporting measures: member activation within a group; availability freshness; proposal response and acceptance; participant-rated date/place fit; confirmation-to-attendance conversion; reasons for missed meetups, including forgetting; repeat group participation; and coordination effort. Treat reminder effectiveness as a hypothesis to evaluate, not an assumed cause of attendance improvements.

Guardrails: unwanted notifications, privacy complaints, repeated exclusion, cancellations, and false or outdated venue details.

Attribution: compare against baseline and ask whether plans were already underway. If recruitment permits, use staggered starts or a comparison group. Do not describe all product-assisted meetups as incremental.

## Planning inputs still needed

Founder availability, team capabilities, development budget, target launch horizon, access to initial groups, first city within Uzbekistan, and concrete growth and business objectives. No delivery schedule is committed yet.
