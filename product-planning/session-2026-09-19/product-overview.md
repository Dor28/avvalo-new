# Product overview

Version 0.8 — updated from founder interview, 2026-09-20. Experience details remain proposals.

## Working definition

Core value confirmed by the founder: help groups choose a better date, choose a better place, and not forget meetups. Reminders are a tentative feature, not a committed initial requirement; their scope remains open.

OpenWindow is a Telegram Mini App helping groups in Uzbekistan agree on when and where to meet. Someone initiates planning with either a known destination or a request for AI assistance. In the assisted workflow, AI asks three questions and searches the internet for suitable places, informed by preferences, recent meetups, and availability supplied for that meetup.

## Intended audience

Founder-confirmed audience: any group arranging a meetup in Uzbekistan, including friends, families, colleagues, and communities. The product is not restricted to friend groups or the founder's own group. Pilot recruitment and outing categories remain open; demand across these audiences still needs validation.

Launch geography: Tashkent, confirmed by the founder. Uzbekistan remains the broader intended market. Place discovery and initial validation should focus on Tashkent; expansion timing remains open.

Launch languages: Uzbek and Russian for the interface and AI conversation. Language selection and Uzbek script support remain design details to resolve; search-source languages are a separate question.

The initial problem described by the founder is holiday meetup planning: some people actively want a meetup while others remain passive; sometimes the whole group struggles to choose a destination. Holidays are a motivating use case, not a confirmed restriction on the product. Group sizes, meeting frequency, and current communication channels are unconfirmed. The meaning of “holidays” remains open.

Distinguish the person who introduces the product from the other members who must participate. The first adopter may be the habitual organizer, even if the long-term promise is to reduce dependence on that person.

## Problem hypothesis

Founder-reported problem: groups want to meet but stall over time and place, compounded by passive members. This supports investigating group decision-making alongside availability matching. A specific recent incident and evidence from prospective users are still needed.

Assistant interpretation: a passive member may be happy to join a good proposal, unavailable, uninterested, or simply not responding. These states must not be treated as equivalent. The thesis's private-budget and constraint hypotheses remain unvalidated.

## Job to be done

“When we want to see each other but nobody wants to coordinate everything, help us agree on a realistic plan with little effort and without awkward negotiations.”

## Proposed core experience

1. A member initiates a meetup for the group. This trigger is founder-confirmed.
2. Planning follows a known-place or AI-assisted workflow. In both cases, members mark availability for this meetup; the order of input collection remains open.
3. For a known place, the proposed flow preserves that choice and helps coordinate time and attendance. For assistance, AI asks three questions, searches online, and proposes suitable time/place options using available preferences and recent meetup history. Who answers, the questions, number of suggestions, and whose constraints must be satisfied remain open.
4. Decision-making is flexible: support group voting and initiator selection after participant responses. The default and how a meetup selects its decision method remain open. Choosing a plan and confirming individual attendance are separate; attendance rules remain undecided.
5. Potential supporting step: remind participants about the meetup. The founder is tentative about reminders; inclusion, scope, timing, and delivery remain open.
6. After the planned time, members report whether the meetup happened and whether it worked for them.

The founder's initial platform direction is a Telegram Mini App, possibly accompanied by a bot added to a Telegram group. A standalone web app is intended later, with no committed date or scope. The proposed role of the Mini App is to collect inputs, show suggested times and places, and let members respond. Entry from group chats, exact bot responsibilities, invitations, and notifications still need definition; these are experience proposals, not verified platform capabilities. One proposal versus several options and attendance rules remain open. Participants handle reservations in the initial versions; venue booking is saved for future consideration. The founder wants AI to assist with time and place selection; model choice and the division between AI and structured matching are undecided.

Existing Telegram groups are a likely initial context, inferred from the proposed group bot. This does not yet settle whether the product requires persistent app groups, supports meetup-specific invitations, or offers both. A group bot does not imply permission or capability to read past conversations.

## Recommendation inputs

- **Preferences:** founder-confirmed input. The assisted workflow includes three AI questions. Who answers, the question content, and whether answers become reusable preferences remain open. Possible fields include activity interests, budget, and travel tolerance; these particular fields are proposals.
- **Recent meetups:** founder-confirmed input. How history is captured and whether it should favor familiar places, variety, or both remain open. No automatic access to prior Telegram conversations is assumed.
- **Timetable:** members supply availability separately for each meetup in the initial product. Date-range selection, time-slot format, response deadlines, and edits remain to be designed. Calendar integration is a possible later expansion, not an initial requirement or a committed release.
- **Internet discovery:** founder-confirmed direction for AI assistance, including social media and Instagram as desired sources. Source access, coverage, freshness, and search implementation have not been researched or validated. These are desired product capabilities, not claims of a working integration.

See [workflow drafts](workflows.md) for the two paths and a proposed three-question example.

The initial experience begins with a person's request. Autonomous initiation from detected availability is superseded as the initial direction. Proposed handling for missing history: first-time groups can receive suggestions from available preferences and timetable inputs; validate this during design.

## Proposed value

- Choose dates and times that suit participants' supplied availability.
- Find places that fit the meetup and participants' preferences.
- Help people remember meetups; distinguish reminders for existing plans from prompts to arrange a future meetup.
- Members spend less effort reaching a decision.
- Active members can move a plan forward while passive members have an easy way to respond; the exact behavior requires agreement.
- Sensitive constraints can shape suggestions without being posted to the group.
- Groups get plans they can act on, with suggestions improving from repeated use.

## Scope boundary

Founder-confirmed: no venue booking in the first versions. The product helps groups choose and agree on a plan; participants arrange any necessary reservations. Venue booking is retained as a future expansion candidate, with no committed release date. A confirmed meetup plan must not imply a confirmed venue reservation.

Focus on arranging meetups for any group. The thesis's friend-group-only starting scope is superseded by founder direction. A full calendar, social feed, expert marketplace, professional capacity marketplace, and general-purpose AI assistant remain outside the proposed initial scope. “Any group” does not by itself establish public group discovery, stranger matching, or event ticketing as requirements.

Founder-confirmed availability scope: per-meetup input first. Recurring weekly schedules are not selected for the initial version. Connected calendars may be explored later.

## Success and business model

Founder-prioritized outcomes: better date selection, better place selection, and remembering meetups. Supporting outcome hypotheses: faster agreement, less coordination effort, and more completed meetups. Assess perceived fit of time/place suggestions and reasons for missed meetups alongside decision speed and attendance.

Launch free to users. The founder explicitly deferred monetization and AI spending decisions until later. No paid tier, revenue model, AI budget, provider, or usage allowance has been selected. Proposed pilot measurement: track AI/search usage and cost alongside product outcomes so later decisions have evidence; tracking is not a committed spending policy.
