# Thesis review

Basis: `thesis-source.txt`. This is an analysis of the supplied thesis, not independent market validation.

## Strongest elements

1. A concrete outcome: more real meetups with less organizing work. This gives the product a better test than calendar usage or poll responses.
2. A focused proposed entry point: existing friend groups, with Telegram as a possible participation and distribution channel.
3. Private constraints address a social problem as well as a scheduling problem: people may avoid admitting budget, energy, or activity preferences publicly.
4. Proposals can become more useful through feedback and history. This is a plausible retention mechanism, subject to actual repeated use.
5. The core matching behavior can be tested with rules and manual assistance before investing in complex AI.

## Gaps and tensions

- **Free time does not imply willingness.** An empty calendar may mean rest, household obligations, or time someone does not want to offer. Match explicitly offered social availability.
- **An organizer may still be needed.** Someone recruits members, handles reservations, follows up on silence, and manages cancellations. Establish which work the product actually removes.
- **Autopilot versus permission.** Detecting an overlap, proposing a plan, confirming attendance, and booking a venue are different levels of authority. Each needs a clear boundary.
- **Privacy versus explanations.** Even a helpful public explanation can reveal a member's private budget or social preference. Define what can be inferred from proposals as well as what fields are hidden.
- **Group inclusion versus feasible plans.** Requiring everyone can prevent any meetup; repeatedly selecting the available majority can exclude the same people. The group needs an understandable rule.
- **Availability freshness.** Weekly manual updates may become more work than sending a message. Calendar integration does not solve willingness or trust by itself.
- **One option versus voting.** The thesis alternates between one best plan and up to three options. Test whether choice improves acceptance or restarts negotiation.
- **Recommendation reliability.** A good category match is not a usable plan if the venue is closed, too expensive, or unavailable. Begin with a bounded, verified activity set if venue detail is necessary.
- **Differentiation is still a hypothesis.** Combining features does not establish why groups switch or keep using the product. The thesis's analog claims need verification before external use.
- **Impact is difficult to attribute.** A completed meetup alone cannot prove it would not otherwise have happened. Use baseline behavior, participant reports, and a comparison design where practical.

## Questions that most affect the strategy

Who is the first specific group? What recently stopped them from meeting? Is coordination the cause, or are willingness and competing priorities the cause? What recurring effort will members accept? What action can the product take without an organizer? How can the founder reach initial groups?

Expert access, creator windows, and professional capacity should remain separate expansion hypotheses until the initial audience is chosen and the core outcome is demonstrated.
