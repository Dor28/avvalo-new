# Product interview

Status: founder requested a separate analysis of differentiation from Telegram polls and broad appeal, then continuation tomorrow. Analysis saved in `strategy-beyond-telegram-polls.md`. Round 15 and earlier unanswered questions remain open; no immediate answer requested.

## Interview approach

Use short rounds and concrete examples. The founder can answer informally, ask questions, or challenge the drafts. After each round, record answers and update the overview, vision, plan, and decision register. Separate explicit answers from assistant interpretation.

## Round 1 — people, problem, and direction

1. Who are the first people you want to build this for? Describe one real group: where they live, their life stage, roughly how many people are in it, and how they currently arrange meetups.
2. Tell me about the last time that group wanted to meet but the plan failed or became frustrating. What happened, who tried to organize it, and what actually stopped it?
3. The thesis favors friend-group autopilot. Is that the product you most want to build, or is your stronger interest in another part of the idea? What makes this worth building for you personally?

Founder answer, 2026-09-20 (verbatim):

> we are building for uzbekistan, group of people want to meet in holidays but cant decide where and when, usually part of the group want to meet but other part is passive or everyone cant decide where to go,  i want to build big product, which will help people to meet and decide things faster, ai will help to choose correct time and place

Explicitly established: Uzbekistan; holiday meetups; difficulty choosing time and place; uneven member participation; ambition for a large product; AI assistance with time and place selection.

Assistant interpretation: helping a group reach agreement may be as central as finding shared availability. Passive participation needs investigation before selecting reminders or attendance rules. This answer does not establish that passive members lack interest.

Still open from round 1: a specific group profile and recent incident, initial city, group size, current channel, and whether holiday means public holiday, weekend, or vacation.

Founder follow-up, 2026-09-20 (verbatim):

> my initial thought that we will start from mini-app in telegram

Initial product platform direction: Telegram Mini App. The group's current planning channel has not separately been confirmed. Bot behavior, sharing, notifications, and the Mini App interaction flow remain to be designed.

## Round 2 — how the group reaches a decision

1. How should planning start: someone says “let’s meet this holiday” and asks the product to help, or the product independently notices an opportunity and prompts the group?
2. Imagine a group of eight: four want to meet and four do not reply. Should the product help the four proceed, wait for everyone, or let the person starting the plan choose who must respond?
3. What should AI deliver first: one recommended time and place to accept or decline, or two or three options for the group to vote on?

Founder answer, 2026-09-20 (verbatim):

> of course someone should initiate, ai should propose time and place according to users preferenceses, latest meets, timetable

Confirmed: a person initiates planning; AI proposes time and place using user preferences, recent meetups, and timetable information.

Still unanswered: handling silent members; one proposal versus several; confirmation authority. The eight-person example above is an interview scenario, not a confirmed group size.

Interpretation boundary: “timetable” does not yet imply calendar integration; “latest meets” does not imply access to chat history or a preference for novelty. Collection methods remain open.

## Round 3 — how the app learns availability

How should the app know when people are free: members mark available times for each proposed meetup, set a reusable weekly schedule, or connect a calendar? A combination is also possible.

Founder answer, 2026-09-20 (verbatim):

> lets start from the per meetup, than probably we will expand to the calendars

Confirmed: members mark availability for each meetup in the initial product. Calendar integration is a possible later expansion, not a committed feature or date. Recurring weekly schedules were not selected.

## Round 4 — preferences for choosing a place

Should members save preferences, such as activities they enjoy, usual budget, and preferred areas, then adjust them for each meetup—or choose everything afresh each time?

Assistant proposal for discussion: save reusable preferences and allow meetup-specific changes, such as a lower budget or wanting a quiet place today. The fields and this reuse behavior are not yet founder-confirmed.

Founder answer, 2026-09-20 (verbatim):

> we can have several workflows, where users are sure where to go and where they want ai assistence, in case of assitence ai will ask 3 questions and try to help with search from the internet (social media, instagram and etc)

Confirmed: support at least a known-place workflow and an AI-assisted workflow. Assistance asks three questions and searches online, with social media including Instagram among desired sources.

Still open: saved versus per-meetup preferences. This answer defines alternative workflows rather than approving the suggested preference profile. Question content, respondent, and whether availability entry is included in the three questions remain open. No source access has been verified.

## Round 5 — who supplies the discovery inputs

Should AI ask its three questions only to the person organizing the meetup, or should each participant answer so suggestions reflect individual preferences?

Founder answer, 2026-09-20 (verbatim):

> i dont know for now

Decision deferred: who answers the three questions remains open. Do not treat uncertainty as acceptance of either approach. Assistant proposes comparing initiator-only and individual-answer flows in a prototype; a hybrid remains possible.

Assistant draft for later discussion: activity/vibe, budget per person, and city/area are possible question topics. These are examples, not confirmed requirements; see `workflows.md`.

## Round 6 — what outings to support first

Thinking of your own group, what would you most often use this to arrange: restaurants/cafes, activities such as bowling or cinema, or trips outside the city? A recent example is enough.

Founder response, 2026-09-20 (verbatim):

> lets do not focus only on my group

Correction accepted: do not frame discovery or product scope primarily around the founder's own group. The outing-category question was not answered; no categories were selected or excluded.

Reframed interview question: who should the product serve—friend groups, families, colleagues, communities, or any group arranging a meetup?

Founder answer, 2026-09-20 (verbatim):

> any group

Confirmed: the intended audience includes any group arranging a meetup, such as friends, families, colleagues, and communities. Uzbekistan remains the initial market. This supersedes the thesis's friend-group-only starting scope. It does not establish public discovery or stranger matching as requirements. Initial outing categories remain undecided.

## Round 7 — lasting groups or meetup-specific invitations

Should people create a lasting group in the app for repeated meetups, or create a meetup and share an invitation link with whoever should join? Supporting both is also an option.

Founder answer, 2026-09-20 (verbatim):

> in first versions lets use telegram mini-apps, maybe bot that will join group, later we will have web-app

Confirmed: Telegram Mini App for initial versions; standalone web app later. Tentative: a bot added to a Telegram group. This clarifies platform progression, but does not explicitly choose persistent app groups, meetup-specific invitations, or both.

Assistant interpretation: existing Telegram groups are a likely initial context. Exact bot responsibilities, invitation behavior, and membership/history association remain open. No current Telegram capabilities were verified in this discussion.

## Round 8 — reaching a final decision

Once suggestions are ready, should participants vote and the winning option become the plan, or should the person who initiated the meetup choose after seeing everyone's responses?

Founder answer, 2026-09-20 (verbatim):

> lets be flexible

Recorded direction: support flexibility between group voting and initiator selection rather than imposing one universal decision method. The founder did not select a default or specify who configures the mode. Proposed implementation: the initiator chooses a visible rule for each meetup; this is not yet approved. Attendance confirmation and rules for silence or ties remain open.

## Round 9 — primary value and repeat use

What should make groups come back: reaching agreement faster, discovering better places, getting more people to participate, or something else? These can coexist; which should be the main promise?

Founder answer, 2026-09-20 (verbatim):

> choosing better date, place, do not forget about meetings

Confirmed priorities: better date selection, better place selection, and not forgetting meetups. These refine the product promise beyond decision speed alone. “Do not forget” is an outcome; exact reminder behavior was not specified.

## Round 10 — what reminders should do

Should the product remind people about an already scheduled meetup, remind a group to arrange its next meetup, or both?

Founder answer, 2026-09-20 (verbatim):

> maybe reminders

Interpretation: reminders are a possible feature, not a committed initial requirement. The founder has not selected scheduled-meetup reminders, prompts to arrange another meetup, or both. Preserve the earlier desire not to forget meetups, while leaving the mechanism and scope open. Do not ask for reminder details again until scope decisions require them.

## Round 11 — launch coverage

For the first release, should place recommendations cover all of Uzbekistan, or start in one or a few cities and expand? If starting with specific cities, which ones?

Founder answer, 2026-09-20 (verbatim):

> lets start from tashkent

Confirmed: launch in Tashkent, including initial place recommendation coverage. Uzbekistan remains the broader market; any group remains the intended audience. Expansion timing and boundaries beyond the city are not specified.

## Round 12 — launch languages

Which languages should the first version support for the interface and AI conversation: Uzbek, Russian, both, or also English?

Founder answer, 2026-09-20 (verbatim):

> uzbek and russian

Confirmed: Uzbek and Russian for the first version's interface and AI conversation. Search-source languages are separate. Language selection, Uzbek script support, and mixed-language group behavior remain design details rather than confirmed requirements.

## Round 13 — recommendation or reservation

Should the first version help the group choose a date/place and agree on a plan, leaving any reservation to participants, or should it also book the venue?

Founder answer, 2026-09-20 (verbatim):

> yes, without booking for first versions but lets save for future

Confirmed: initial versions help groups choose and agree on a plan without booking venues. Participants handle reservations. Retain venue booking as a future expansion candidate, with no committed delivery date or implementation.

## Round 14 — free versus paid launch

Should the first version be free while we validate usage, or should it include paid features from launch? It is also fine to leave this undecided.

Founder answer, 2026-09-20 (verbatim):

> yes, lets begin from free, we will decide later monetization and spend on ai

Confirmed: launch free; decide monetization and AI spending later. No budget, paid tier, provider, or usage allowance is selected. Assistant proposal: track pilot AI/search usage and cost to inform later choices. Do not turn that proposal into a spending commitment or ask for a budget immediately after its deferral.

## Round 15 — delivery capacity and timing

Who will build the first version—you alone or a team—and when would you like the first groups to try it?

Founder answer: pending. Answers will shape delivery milestones; no date or staffing assumption has been made.

## Later rounds — adapt to answers

- Resume with the strategy note requested by the founder: advantage over Telegram polls and appeal beyond early adopters. Recommendations in that note are not approved requirements.
- Desired outcome: meeting frequency, organizer burden, and what would make the product indispensable.
- Member behavior: availability input, willingness, freshness, privacy, and acceptable effort.
- Product authority: proposals, attendance thresholds, silence, confirmation, booking, and cancellation.
- Experience: first useful session, adoption within a group, distribution channel, activity choices, and notification cadence.
- Inclusion and trust: hard constraints, subgroup formation, private intent, and repeated exclusion.
- Validation: recruitment, pilot design, baseline, and pass/revise/stop criteria.
- Business and delivery: buyer, revenue hypotheses, resources, launch horizon, and scope tradeoffs.
- Final synthesis: agreed overview, vision, MVP boundaries, prioritized roadmap, and remaining assumptions.

## Session record

- 2026-09-19: Founder requested a thesis review, dedicated session folder, collaborative product interview, and product overview/vision/plan.
- 2026-09-19: Assistant reviewed the thesis and created initial documents. No product direction has yet been confirmed through interview answers.
- 2026-09-20: Founder established the initial country, planning problem, growth ambition, and intended AI role. Updated overview, vision, plan, and decision register; saved round 2.
- 2026-09-20: Founder selected Telegram Mini App as the initial platform direction; updated documents before continuing round 2.
- 2026-09-20: Founder confirmed person-initiated planning and three recommendation inputs: preferences, recent meetups, and timetable. Updated drafts to version 0.3; autonomous initiation is superseded for the initial experience. Asked about timetable collection next.
- 2026-09-20: Founder chose per-meetup availability first and possible calendar integration later. Updated overview and plan to version 0.4; moved interview to preference setup.
- 2026-09-20: Founder defined known-place and assisted workflows, with three AI questions and internet/social discovery for assistance. Added workflow drafts and updated overview, vision, and plan to version 0.5. Next question concerns who answers.
- 2026-09-20: Founder is unsure who should answer the AI questions. Kept that decision open, proposed a prototype comparison, and moved the interview to initial outing types.
- 2026-09-20: Founder asked not to focus only on their group. Broadened interview framing and discovery to intended audiences across Uzbekistan; no audience segments or outing categories selected yet.
- 2026-09-20: Founder confirmed any group as the audience. Updated overview, vision, and plan to version 0.6 and superseded friend-group-only scope. Next question concerns persistent groups versus meetup-specific invitations.
- 2026-09-20: Founder confirmed Telegram Mini App first and standalone web app later, with a group bot as a tentative companion. Updated overview and plan to version 0.7. Membership rules remain open; next question concerns final decision authority.
- 2026-09-20: Founder requested flexible decision-making. Recorded support for voting and initiator selection, leaving configuration and default open. Shifted interview to the main value that should drive repeat use.
- 2026-09-20: Founder prioritized better dates, better places, and not forgetting meetups. Updated overview, vision, and plan to version 0.8; added proposed reminder behavior and asked for clarification of its scope.
- 2026-09-20: Founder described reminders tentatively. Marked them as a candidate feature, preserved the remembering-meetups outcome, and consolidated the agreed direction in `product-brief.md`. Moved the interview to launch coverage.
- 2026-09-20: Founder selected Tashkent for launch. Updated overview, vision, plan, and brief; scoped proposed pilot and venue-quality checks to Tashkent. Next question concerns interface and AI conversation languages.
- 2026-09-20: Founder selected Uzbek and Russian. Updated overview, plan, and brief; added bilingual workflow validation to the plan. Next question concerns whether the first version handles venue reservations.
- 2026-09-20: Founder excluded booking from initial versions and requested saving it for the future. Updated the scope and added a future expansion register. Next question concerns free versus paid launch.
- 2026-09-20: Founder chose a free launch and deferred monetization and AI spending. Updated overview, plan, and brief; proposed usage measurement for later decisions. Moved interview to team capacity and target first-test date.
- 2026-09-20: Founder requested analysis of how the product can outperform Telegram date/place polls and attract many users, saved separately for tomorrow, followed by a push to `main`. Researched selected official product sources and saved the strategy note; left team/timing unanswered.

## Founder request for tomorrow's strategy discussion

Verbatim, 2026-09-20:

> i want you to know think about this thing, people can already create a vote in telegram, with possible dates and places, how our app can be better than this pattern and in general think how our app can be more attractive for mass people, save your thoughts on different file and i will continue with it tomorrow, after you finish git push to main

Response artifact: `strategy-beyond-telegram-polls.md`. It distinguishes researched product facts, strategic judgments, proposed experiments, and existing founder decisions. Publication requested: commit session documents and push to `main`. Actual Git outcome is reported in the assistant's completion message rather than assumed here.
