# Meetup workflows

Version 0.1 — 2026-09-20. Confirmed directions and proposed details are separated below.

## Shared foundation

Founder-confirmed: Telegram Mini App first; a person initiates; availability is supplied per meetup; recommendations consider preferences and recent meetups. A bot added to a Telegram group is a tentative companion for initial versions. A standalone web app is intended later; calendar integration is a possible later expansion.

Existing Telegram groups are an inferred starting context. Persistent app groups versus meetup-specific invitations remain undecided. Bot roles and access capabilities have not been verified.

At least two workflows are required. The founder has not said these are the only workflows.

Booking boundary confirmed by the founder: neither workflow books venues in initial versions. Participants arrange reservations themselves. A confirmed group plan does not indicate a venue reservation. Booking is saved as a future feature candidate.

## Flexible decision-making

In response to a choice between group voting and initiator selection, the founder requested flexibility. Preserve both as supported decision approaches rather than imposing one universal rule. Proposed implementation: the initiator selects the decision method for the meetup and participants can see it. This implementation and the default are not yet confirmed.

Decision modes apply where a choice remains: a known-place meetup may only require choosing time, while an assisted meetup may require selecting both time and place. Choosing a plan does not itself confirm every invited person's attendance. Voting thresholds, ties, deadlines, silence, and attendance confirmation remain open.

## Workflow A: the group knows where to go

Confirmed: support people who already know their destination.

Proposed experience:

1. The initiator supplies the chosen place, for example by name or link.
2. Participants mark suitable times for this meetup.
3. The app identifies times that meet the group's attendance rule.
4. Participants respond and the plan is confirmed under a rule still to be defined.

The three-question place-discovery step is not required for this proposed path. Whether the time can also be fixed in advance remains open. Name/link entry and confirmation behavior are design proposals, not verified Telegram functionality.

## Workflow B: the group wants help choosing

Confirmed: AI asks three questions, then helps search the internet, including social media such as Instagram as desired sources. Earlier direction still applies: recommendations use preferences, recent meetups, and per-meetup availability.

Proposed experience:

1. The initiator chooses assistance.
2. AI asks three short questions to understand the occasion and constraints.
3. Availability is collected for this meetup. Its position relative to the questions and whether it is included in the three-question limit remain open.
4. The product searches for relevant places and assesses their fit against the supplied inputs and available history.
5. It presents time/place suggestions for the group to decide on.
6. The plan is confirmed under an agreed participation rule.

### Three-question example — for discussion, not approved

1. What would you like to do: eat, relax and talk, or do an activity?
2. What is the budget per person?
3. Which city or area works for this meetup?

Questions may need to adapt to information already supplied; fixed versus adaptive questions is undecided. Who answers is the immediate interview question. The initiator's answers should not be described as every member's personal preferences without confirmation.

### Proposed search result behavior

Show source links with recommendations and distinguish sourced facts from estimates or unknowns. Search results are candidate places, not confirmed bookings. Verify essential details such as location, opening times, and price when available; do not infer missing facts from promotional content.

Internet search is a confirmed product requirement. Access to Instagram or any particular source has not been validated. Before implementation, research available access methods and test coverage for the chosen city. Design behavior for missing source access, insufficient results, and outdated details.

## Open decisions

- Does “not forget meetups” mean reminders for confirmed plans, prompts to arrange another meetup, or both? The founder confirmed the outcome; exact behavior remains open.
- Does the initiator answer the three questions, does each member answer, or is there a shared response?
- Are questions fixed or adapted to the request and known information?
- Does availability entry count toward the three questions?
- Are preferences stored and reused across meetups?
- What information exists for a group's first meetup, before history has accumulated?
- How many suggestions are presented, and how does a group select one?
- When can planning proceed if some members remain silent?
- Can groups switch from a known place to assisted discovery if the place does not work?

## Remembering meetups

Founder-prioritized outcome: help people not forget meetups, alongside better date and place selection. In the follow-up, the founder said “maybe reminders,” so this is a tentative feature. A proposed optional step for both workflows is to send reminders after confirmation with the current time and place. Inclusion, timing, recipients, delivery, and controls are not yet defined. If implemented, reminders should reflect rescheduling and cancellation; technical delivery feasibility has not been verified.

Whether the product should also prompt a group to arrange its next meetup remains an interview question. This would prompt a person to initiate, not automatically create or confirm a plan.

## Deferred decision: who answers

On 2026-09-20 the founder said they do not know yet. Neither initiator-only nor individual answers is selected.

Proposed validation: prototype both approaches and compare input effort, response delays, and whether suggestions reflect participants' actual needs. Initiator-only answers may be quicker but may miss individual constraints; individual answers may improve fit but require more participation. These are hypotheses to test. Revisit after defining the initial outing types and group profile.
