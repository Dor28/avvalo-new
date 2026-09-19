# Decisions and assumptions

## Confirmed session decisions

| ID | Decision | Basis |
| --- | --- | --- |
| D01 | Develop a product overview, vision, and product plan through a collaborative interview. | Founder request, 2026-09-19. |
| D02 | Save session work in a dedicated folder. | Founder request; folder created at `product-planning/session-2026-09-19/`. |
| D03 | Build initially for Uzbekistan, addressing groups trying to meet during holidays. | Founder answer, 2026-09-20; initial city and meaning of holidays remain open. |
| D04 | Address difficulty agreeing on time and place, including uneven participation. | Founder-reported problem, 2026-09-20; not independently validated. |
| D05 | Pursue a large product helping people meet and decide faster. | Founder ambition, 2026-09-20; expansion scope and business model remain open. |
| D06 | AI should assist in selecting a suitable time and place. | Founder direction, 2026-09-20; implementation and decision authority remain open. |
| D07 | Start with a Telegram Mini App. | Founder initial platform direction, 2026-09-20; detailed interaction and integration design remain open. |
| D08 | A person initiates meetup planning. | Founder answer, 2026-09-20; supersedes autonomous opportunity detection as the initial trigger. |
| D09 | AI proposals use preferences, recent meetups, and timetable information. | Founder answer, 2026-09-20; collection methods and ranking rules remain open. |
| D10 | Collect availability separately for each meetup in the initial product. | Founder answer, 2026-09-20; replaces the previously open timetable-source choice. |
| D11 | Consider calendar integration later. | Founder tentative expansion, 2026-09-20; outside initial scope, with no release commitment. |
| D12 | Support known-place planning and AI-assisted discovery as separate workflows. | Founder answer, 2026-09-20; other workflows may follow. |
| D13 | In the assisted workflow, AI asks three questions before helping with search. | Founder answer, 2026-09-20; questions, respondent, and relationship to availability entry remain open. |
| D14 | Use internet search for assisted discovery, including social media and Instagram as desired sources. | Founder direction, 2026-09-20; source access and coverage unverified. |
| D15 | Do not focus product discovery or scope only on the founder's own group. | Founder correction, 2026-09-20; intended segments across Uzbekistan still to be defined. |
| D16 | Serve any group arranging a meetup, including friends, families, colleagues, and communities. | Founder answer, 2026-09-20; Uzbekistan remains the initial market. Resolves the audience question in D15. |
| D17 | Launch initial versions as a Telegram Mini App, with a standalone web app later. | Founder answer, 2026-09-20; no schedule or later feature scope committed. |
| D18 | Consider a bot added to Telegram groups as a companion to the initial Mini App. | Tentative founder idea, 2026-09-20; roles and feasibility remain open. |
| D19 | Keep decision-making flexible between group voting and initiator selection. | Founder response “lets be flexible,” 2026-09-20, to those two options. Default, configuration, and attendance confirmation remain open. |
| D20 | Prioritize better date selection, better place selection, and helping people remember meetups. | Founder answer, 2026-09-20; exact reminder scope and behavior remain open. |

## Working directions from the thesis — awaiting confirmation

| ID | Direction | Status |
| --- | --- | --- |
| T01 | Begin with existing friend groups and proactive plan creation. | Superseded: D08 selects person-initiated planning; D16 expands the intended audience to any group. |
| T02 | Use Telegram as an initial distribution and interaction channel. | Founder selected Telegram Mini App as initial direction; audience adoption and distribution effectiveness remain untested. |
| T03 | Use private constraints and group history to improve proposals. | Preferences and recent meetup inputs confirmed by D09; privacy behavior and detailed history use remain proposals. |
| T04 | Keep most matching deterministic and use AI selectively. | Proposed design principle; no implementation selected. |
| T05 | Defer experts, creators, and professional capacity. | Proposed focus, subject to founder direction. |

## Assumption register

| ID | Assumption | How to investigate |
| --- | --- | --- |
| A01 | Coordination prevents meetups people actually want. | Recent planning stories and baseline group behavior. |
| A02 | Enough members will supply and update availability for each meetup. | Availability response rate, effort, and freshness across repeated planning attempts. |
| A03 | Autonomous proactive proposals will feel helpful. | Deferred: initial flow is person-initiated under D08. |
| A04 | Private constraints improve fit without undermining trust. | Member interviews and permission-aware pilot. |
| A05 | A sufficiently good local plan can be produced reliably. | Bounded activity catalog and proposal/attendance outcomes. |
| A06 | Groups get repeated value beyond novelty. | Repeated participation and completed meetups. |
| A07 | A viable buyer and revenue model exist. | Buyer discovery and willingness-to-pay experiments. |
| A08 | Passive members will respond to a concrete proposal even if they avoid planning. | Interview active and passive members; observe proposal responses without assuming silence is agreement. |
| A09 | AI assistance can shorten decisions while producing plans people attend. | Track time to agreement, participant effort, and attendance against baseline. |
| A10 | Preferences, recent meetups, and timetable data can be collected with acceptable effort and kept useful. | Test initial setup, a group with no history, and repeated planning; measure missing/stale inputs and member effort. |
| A11 | Three questions provide sufficient information for useful place discovery. | Pilot question completion, missing constraints, and suitability of suggestions. |
| A12 | Internet and social sources provide accessible, sufficiently current local venue information. | Verify access methods and test coverage, essential details, and fallbacks for the chosen city. |

## Open decisions

Next clarification: reminders for confirmed meetups, prompts to arrange another meetup, or both. The founder confirmed the outcome of not forgetting meetings, not a specific reminder mechanism.

Explicitly deferred by the founder, 2026-09-20: who answers the three AI questions. No default selected. Proposed next step is to compare initiator-only and individual-answer prototypes after clarifying the use case.

First city within Uzbekistan and pilot group composition; initial outing categories; meaning of holidays; problem severity across group types; persistent groups versus meetup-specific invitations; three-question content and respondent; per-meetup availability entry details; preference reuse; history capture and use; search source feasibility; Telegram entry/sharing/notification flow and bot responsibilities; required member participation; number of proposals; final decision and attendance confirmation rules; privacy and inclusion rules; pilot access; success thresholds; team capacity; budget; launch horizon; later web app scope; and revenue model.

Competitive statements remain source claims, not verified findings from this session.
