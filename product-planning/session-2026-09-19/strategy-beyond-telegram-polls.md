# Why use OpenWindow instead of a Telegram poll?

Strategy note for tomorrow's discussion — 2026-09-20.

Status: assistant analysis and proposals, not new founder-approved requirements. Product facts below come from official sources checked on this date; recommendations and adoption predictions are hypotheses. This is a focused comparison, not an exhaustive market study or validation with Tashkent users.

## My assessment

The objection is correct. If people already have a few acceptable places and times, a Telegram poll can be enough. Asking them to open a Mini App and repeat the same work may make the experience worse. Adding AI wording, prettier cards, or reminders does not establish a strong reason to switch.

The strongest opportunity is to do the work people must perform around a poll: discover worthwhile options, check practical constraints, find a date-and-place combination that works for the same people, and turn the result into an agreed plan. Voting can remain one step inside that experience.

My proposed promise is: **“Find a date and place that work for your group, with less searching and back-and-forth.”** The product must demonstrate that benefit on the first meetup, before it has history or everyone has created preferences.

## 1. The baseline we must actually beat

Telegram's March 2026 update added media and locations to poll questions/options, participant suggestions for new options, time limits, and a dedicated tab for current and past polls. Older poll functionality includes multiple answers and visible or anonymous votes. We should not position OpenWindow around pictures, deadlines, visibility of responses, or the claim that polls inevitably disappear in chat. [Telegram's current poll features](https://telegram.org/blog/ai-editor-mighty-polls-and-more?setln=en), [multiple-answer and visible-vote polls](https://telegram.org/blog/polls-2-0-vmq).

The wider category also sets a high bar. Doodle offers time polling, participant tracking, deadlines, reminders, and calendar invitations. Partiful lets hosts poll dates/times, select a time, and notify guests. Howbout offers shared calendars and availability discovery. These sources establish overlapping capabilities, not that the products solve our entire intended problem. [Doodle Group Poll](https://doodle.com/en/product/polls/), [Partiful Find a Time](https://help.partiful.com/en-us/articles/15525423-using-find-a-time-to-poll-guests-on-date-and-time), [Howbout calendar and availability](https://howbout.app/get-help/is-there-a-free-shared-calendar-app-for-friends/).

The practical competitor is also a combination: Telegram + a person searching Instagram/maps + perhaps a general AI assistant. We must reduce total effort across that combination. Being able to search online is useful, but is not by itself a durable advantage.

| Planning job | What an ordinary poll-based workflow can do | What OpenWindow must earn |
| --- | --- | --- |
| Choose from known options | Collect votes with very little setup | At least comparable participant effort; otherwise a poll wins |
| Find candidate places | People search and supply options | A short, credible shortlist that saves real search work |
| Coordinate date and destination | Organizer compares responses or polls combined options | Joint matching that makes attendance and tradeoffs clear |
| Handle constraints | Chat, poll options, and organizer judgment | Collect essential constraints without public awkwardness or long forms |
| Finish the decision | Organizer posts a final message | A clear, current plan and explicit participation state |
| Arrange another meetup | Repeat the process or reuse familiar places | Useful reuse of actual meetup history with little maintenance |

These are intended advantages to prove. Telegram users can manually reproduce much of this. The question is how much work the product removes, not whether the work is theoretically impossible in chat.

## 2. Three advantages worth testing

### A. Find good options before asking the group to vote

The initiator should get value before recruiting everyone into a new workflow. After the agreed three-question interaction, show a small set of relevant places with enough information to assess them: what the activity is, location, a sourced price or explicitly marked estimate, practical suitability, and a link to inspect the source.

Use date constraints when available, but call early suggestions preliminary if participant availability is still missing. Do not claim the group can attend before collecting responses.

An attractive result is a useful shortlist the initiator would otherwise have spent time assembling. A long list of generic restaurants or a confidently invented recommendation is not success. If a person can get the same quality from one general-AI prompt and paste it into a poll, our next advantage must come from group coordination and reliable local detail.

### B. Match date and place together

Separate popularity winners can produce a bad combined plan. For example, in an eight-person group, six people may accept Friday and six may accept a particular venue, but only four may be in both sets. Another date/place combination could suit five. These numbers are illustrative, not research findings.

The app can compare actual combinations using availability, duration, venue hours where known, and relevant participant constraints. It should explain outcomes such as “five respondents can attend; two have not answered,” rather than treating silence as availability.

This is also possible with carefully constructed polls. The benefit is automatically generating and comparing feasible combinations without making the organizer enumerate every combination. The result depends on choosing an attendance rule: everyone, required participants, or a sufficient subset. That rule remains undecided.

Respect hard limits and distinguish them from preferences. Do not label one option universally “best.” Explain whether it fits more respondents, costs less, or requires less travel, and preserve the group's ability to choose. Private constraints should shape a result without publishing who supplied them.

### C. Keep a useful plan and learn from actual meetups

The output should make the selected time, place, responses, and next action clear. A group-agreed plan is not a venue reservation; booking remains outside the first versions.

Later, a small amount of confirmed history can help: which place was actually visited, whether people liked it, and whether they want a similar option or something different. A repeated favorite can be a good recommendation; novelty is not automatically better.

This is a possible reason to return, not a proven moat. It must work without full-calendar access, imported chat history, or a long initial profile. Learning and preferences need to fit the current participants rather than blindly copying the taste of a different subgroup.

## 3. How it could appeal to many kinds of people

The audience remains any group. Broad appeal should come from a familiar job with a simple interface, rather than a separate complicated mode for every relationship type.

**Use ordinary language.** Lead with finding a date and place. “AI coordination layer,” “availability graph,” and the original autopilot promise describe machinery or imply more autonomy than we have agreed. Uzbek and Russian wording should be checked with users for clarity and naturalness.

**Two clear starting choices.** “We have a place” and “Help us choose.” Keep the known-place path short. A person who already knows the destination should not have to complete an AI discovery conversation.

**Let one person start and benefit.** Show a useful draft before requiring a fully activated group. Test a shareable entry into the Mini App and a compact group summary; exact Telegram behavior requires technical verification. Treat adding a group bot as a possible convenience, not a mandatory first obstacle unless testing establishes a need.

**Make participant work small.** People should understand what they are responding to and be able to state availability quickly. Treat “under a minute to respond” as a prototype target, not a promise. No required calendar connection, upfront preference questionnaire, or irrelevant discovery questions in the initial experience.

**Accommodate partial certainty.** Someone may know the place but not the date, know the date but not the place, or know neither. The two agreed workflows should preserve information already supplied. This is a design proposal, not a request to add three new products.

**Show useful results, not a conversation transcript.** A concise comparison can be easier to act on than paragraphs of AI advice. Keep the number of options small in the prototype and test it; the founder has not selected a number.

**Make trust visible.** Show source links, distinguish known details from estimates, and allow people to reject or correct a suggestion. A recommendation can look appealing and still fail on travel, opening hours, group suitability, or cost. Do not invent reservation availability.

**Support passive members without pressure.** Easy responses may help people who dislike organizing. They will not manufacture interest among people who do not want to attend. Show unanswered responses accurately; never silently count them as consent. Reminders remain tentative and should not become the claimed differentiator.

**Keep flexibility behind a simple default.** The founder wants voting and initiator-led decisions. That does not require presenting every setting before a person can start. Prototype an understandable default, expose the choice when relevant, and treat the default as a proposal until selected.

**Measure return at the right moment.** A meetup product can be valuable without daily use. Evaluate whether people return when they next need to arrange something, rather than designing a feed or notifications to manufacture daily activity.

## 4. Local discovery is both an opportunity and a dependency

Tashkent is a useful boundary for learning whether recommendations are reliable. Uzbek and Russian are confirmed launch languages. Neither localization nor city coverage alone proves competitive advantage; the advantage would be consistently better results with less effort.

For a manageable pilot, propose a small, maintained set of real places combined with online discovery. Choose representative occasions across friends, families, colleagues, and communities; do not base the catalog only on the founder's tastes. Exact categories and catalog size remain open.

Keep source links and the time essential information was checked. Track missing or contradictory prices, hours, and location details. Treat social posts as leads that may need corroboration. Instagram is a desired source, not a verified integration or a promise of comprehensive access.

An optional future interaction to test is “add a place link you already found.” That could connect social discovery to planning without asking users to abandon how they find ideas. It is not yet a requirement or a verified link-import capability.

If open-ended web search is unreliable, a curated starting catalog is an implementation experiment rather than a reason to present unreliable results as facts. If neither approach produces sufficiently good local suggestions, the main assisted-discovery proposition needs revision.

## 5. The hardest unresolved issue: who answers the three questions?

The founder explicitly deferred this, and it should remain open. My proposed experiment starts with the initiator answering three discovery questions, while participants provide availability and an easy way to flag a constraint. Compare that with participants each answering questions.

The first may reduce effort but represent the organizer's preferences too strongly. The second may improve fit but reduce completion. Measure both, rather than calling either the correct approach now.

Keep the questions within the agreed limit. Do not hide a long questionnaire behind three headings. Possible topics are occasion/activity, budget, and area; date information may come from the meetup setup. The total input burden, including availability, matters more than the number of AI messages. Avoid re-asking information already supplied.

## 6. A concrete test against ordinary Telegram planning

Run a small directional pilot with, for example, 8–12 independent Tashkent groups across several group types. The number is a proposed feasibility target, not a statistical power claim. Groups should plan real meetups they already want, without being pushed to invent extra events for the study.

Compare their usual Telegram workflow—including polls and their normal search tools—with the prototype. Where groups have comparable repeated occasions, alternate the order of methods to reduce novelty and order effects. Otherwise use comparable parallel groups and report the limitations. Do not make the same participants plan the same outing twice and call the result an unbiased comparison.

Record any manual assistance behind the prototype. If researchers curate every option or chase every participant, that effort must count when assessing the eventual product.

| Measure | What it tells us |
| --- | --- |
| Organizer's active minutes, including search | Whether we remove work rather than move it into the app |
| Participant response time and completion rate | Whether added friction erases the organizer's benefit |
| Elapsed time to an agreed date/place | Whether decisions actually get easier |
| Participant-rated date/place suitability | Whether the result improves, not merely the interface |
| Completed meetups and reasons for cancellations | Whether accepted suggestions become real plans |
| Unprompted reuse at the next planning occasion | Whether groups prefer it after the novelty wears off |
| Incorrect venue details and unsupported claims | Whether discovery can be trusted |

Agree numeric thresholds before running the pilot, once baseline behavior is known. A provisional success condition is a meaningful reduction in organizer work with no material decline in participant completion or attendance, plus clear preference for using the product again. For discovery-heavy occasions, also require better-rated place choices. Include abandoned attempts in the results.

If people like the look but still prefer native polls, improve or remove the extra steps. If they use discovery but decline group coordination, consider making the shortlist-to-share flow the strongest entry point while keeping the larger vision open. If coordination helps only complex occasions, market those occasions honestly rather than claiming every poll needs replacement.

## 7. Adoption and what might accumulate over time

A plausible distribution loop is: an initiator gets a useful shortlist, shares a planning invitation, participants experience a quick decision, and one participant later starts a meetup with another group. This is a hypothesis; invitations alone do not prove viral growth. Track completed participant journeys and subsequent initiators, not just shares.

The first product must be useful at low adoption. Requiring an entire social network or months of history before recommendations improve would undermine this loop.

Potential lasting strengths are reliable Tashkent venue data, demonstrated understanding of local planning needs, and reusable preferences/history for groups that choose to retain them. All are earned through usage. A generic model call, a three-question conversation, or a Telegram wrapper can be copied easily. Neither free launch nor being “AI-powered” guarantees mass adoption.

Do not add booking, calendar integrations, a social feed, paid features, or autonomous meetup creation to compensate for a weak core result. Booking and calendars remain future candidates; launch is free; monetization and AI spending remain deferred. Usage measurement can inform later economics without deciding them now.

## Where I would take the product next

I would test this proposition first: **a person in Tashkent can obtain a credible, suitable shortlist and turn it into a group plan with less effort than searching and running Telegram polls themselves.** Preserve the known-place path as a fast utility, but expect assisted discovery plus joint time/place matching to carry most of the differentiation.

For tomorrow, review three questions rather than reopening every detail:

1. Does “better options with less organizer work” capture the advantage we want to prove?
2. What would make a date/place suggestion good enough to share immediately?
3. Which flow should we prototype to compare fairly with Telegram: known place, assisted discovery, or both?

The existing team/timing question is still unanswered and can wait until after this strategy discussion. None of these proposals changes the recorded founder decisions without further discussion.
