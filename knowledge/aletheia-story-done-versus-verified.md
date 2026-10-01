# Done is not verified done — knowledge behind the story

[Aletheia Protocol](https://github.com/KarstenEvans/aletheia-protocol): evidence, provenance and uncertainty.  
[Thalia Protocol](https://github.com/KarstenEvans/thalia-protocol/blob/main/THALIA_PROTOCOL.md): optional humane humour.

**Status:** Research-informed Aletheia interpretation, 1 October 2026.

## The distinction

An agent or machine can report success when a tool invocation succeeded even though the *intended real-world outcome* did not occur.

Aletheia uses three useful operational labels:

| State | What it establishes | What it does not establish |
| --- | --- | --- |
| ATTEMPTED | An action was issued or attempted. | The target accepted it. |
| COMPLETED | The target system reported success. | The intended external result was achieved. |
| VERIFIED | Task-appropriate independent or observed evidence supports the intended outcome. | Absolute certainty about every downstream consequence. |

Example: a feeder motor turns, but the hopper is empty. The motor action can complete while the cat remains unfed.

## Sources and limits

[NIST AI RMF Core](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/) describes measuring, testing, documenting system functionality, human oversight and managing risk over the lifecycle. Its official four functions are Govern, Map, Measure and Manage. Aletheia's three-state vocabulary is our own teaching framework, not a direct NIST quotation.

[NIST Generative AI Profile](https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-generative-artificial-intelligence), July 2024, is a supplementary cross-sectoral risk-management profile, not a certification of specific agents.

[ICO guidance](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/individual-rights/individual-rights/rights-related-to-automated-decision-making-including-profiling/) discusses transparency, human intervention/contestation in relevant decision-making contexts, and checks that systems operate as intended. Its precise legal requirements depend on the use case.

## Five questions before DONE

1. What was supposed to happen?
2. What did the machine actually do?
3. What evidence supports the outcome?
4. What is still uncertain?
5. Who is authorised to determine whether that is enough?

## Engineering implications

- Carry a goal identifier through action receipts.
- Record tool response separately from independent outcome observation.
- Define task-appropriate verification. Not all benign actions require expensive checks.
- Use bounded retry and stop conditions.
- Escalate permission-changing, payment, publication or physical effects before acting where authority requires.
- Keep durable evidence separate from short-lived working context.

## Story links

- https://karstenevans.github.io/aletheia-app/aletheia-storyteller.htm?story=ToomorrowMan-and-the-AI-That-Said-It-Had-Finished
- https://karstenevans.github.io/aletheia-app/stories/ToomorrowMan-and-the-AI-That-Said-It-Had-Finished.htm

**Evidence boundary:** these fictional incidents illustrate engineering risks; they do not allege that the named fictional systems or characters exist.
