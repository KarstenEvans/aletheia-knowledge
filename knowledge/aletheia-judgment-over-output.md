# Aletheia Judgment Over Output

Aletheia Protocol: https://github.com/KarstenEvans/aletheia-protocol  
Thalia Protocol: https://github.com/KarstenEvans/thalia-protocol/blob/main/THALIA_PROTOCOL.md

Status: source-traced design knowledge  
Created: 30 September 2026  
Purpose: extract reusable decision-support principles from current AI workplace/research articles without copying vendor prose or adopting marketing claims uncritically.

## Executive principle

**Aletheia should optimise for better judgment, not maximum output.**

AI can generate alternatives, summaries and research faster than humans can evaluate them. The design response is not to generate still more. It is to make assumptions, evidence, contradictions, uncertainty and stopping criteria visible while preserving the human decision point.

## Reusable knowledge cards

### JUD-001 — Define the decision before generating options
A topic is not yet a decision. Ask what actual choice, action or approval is required. This prevents a research system from expanding indefinitely around a vague subject.

### JUD-002 — Identify assumptions
Expose what must be true for the current proposal to work. Hidden assumptions are often more important than additional generated ideas.

### JUD-003 — Evidence before confidence
Preserve source links/snippets where permitted, date/freshness, observation versus inference, and any contradictions. A confident summary without provenance is not a stronger result.

### JUD-004 — Challenge the strongest assumption
Do not merely strengthen the user's initial view. Ask what evidence could overturn it and search for material contrary evidence. This is verification rather than confirmation.

### JUD-005 — Pre-mortem
For a planned action, assume it failed after the relevant period. Record plausible failure causes, early warning signs and mitigations. These are scenarios, not predictions.

### JUD-006 — Find missing information
State what remains unknown and whether obtaining it could change the decision. An unknown that cannot change the next action should not automatically trigger endless research.

### JUD-007 — Reduce alternatives
AI can generate more options than people can use. Remove duplicates and weak variants; surface a small number of materially distinct survivors unless the user asks for breadth.

### JUD-008 — Show remaining uncertainty
A finished answer can still be uncertain. Report source disagreement, stale evidence, unverified claims and the conditions that would change the conclusion.

### JUD-009 — STOP is a feature
Define a practical sufficiency threshold. When enough evidence exists for the stated task, report that state and stop generating by default. **Go deeper** is deliberate. STOP means sufficient, not certain.

### JUD-010 — Quiet Mode
For evidence-heavy or monitoring interfaces, default to:
1. What changed?
2. What matters?
3. What needs your attention?

Keep full evidence available through progressive disclosure.

### JUD-011 — Evidence Grid
Apply consistent questions across multiple sources/options and present them in a compact grid: source/item, claim/factor, supports/contradicts, date, evidence and uncertainty. This is a generic research pattern; do not copy a vendor's protected interface.

### JUD-012 — Measure mistakes prevented and insight added
Useful success signals can include:
- found something previously missed;
- caught an error;
- challenged an assumption;
- confirmed a claim with evidence;
- changed the next action;
- did not materially help.

Speed and output volume are not always the right primary metrics.

### JUD-013 — Model-agnostic architecture
The durable asset is the workflow, evidence, project history, corrections and structured domain knowledge. Store these in portable formats so one provider/model can be replaced without losing the project.

### JUD-014 — Invisible AI needs visible accountability
AI may become embedded in ordinary tools and workflows rather than appearing as a named chatbot. Invisible operation can be useful, but material influence should remain inspectable: what changed, why, evidence, uncertainty, override and final human action.

### JUD-015 — Attention is finite infrastructure
Treat human cognitive capacity as a constrained resource alongside tokens, API budget and compute. A system that creates an unreviewable stream of AI output can reduce rather than improve decision quality.

## Source/evidence register

### Source A — AlphaSense: AI decision fatigue
URL: https://www.alpha-sense.com/resources/research-articles/ai-decision-fatigue/  
Status this run: URL supplied by owner; automated fetch was restricted. Earlier extraction identified themes including limiting recommendations, defining “good enough”, completion signals and avoiding infinite option loops. Treat as **vendor thought leadership / discovery**, not independent proof.

### Source B — AlphaSense: Invisible AI
URL: https://www.alpha-sense.com/resources/research-articles/invisible-ai/  
Status this run: URL supplied by owner; automated fetch was restricted. Reusable theme: AI may move from visible assistant to embedded infrastructure; contextual/proprietary knowledge and workflow design become differentiators. Treat as **vendor thought leadership / discovery**.

### Source C — AlphaSense: The Impacts of AI Beyond Efficiency
URL: https://www.alpha-sense.com/resources/research-articles/ai-beyond-efficiency/  
Observed 30 September 2026: argues that AI impact may include broadened perspective, challenged assumptions and outcome quality, not only efficiency; discusses hyper-personalised AI and measurement difficulty.  
Evidence class: vendor research/article; useful design hypothesis, not neutral market evidence.

### Source D — TechRadar: Accuracy over volume
URL: https://www.techradar.com/pro/accuracy-over-volume-heres-why-high-value-pros-are-using-ai-to-work-slower-not-faster  
Published 13 April 2026. Reports Use.AI survey findings including use of AI for decision validation, error prevention and challenging thinking among senior respondents. The article explicitly cautions that the survey is self-reported and that verification may blur into confirmation bias.  
Evidence class: secondary report of survey data; use cautiously.

### Source E — AlphaSense: Generative AI tools for market research
URL: https://www.alpha-sense.com/blog/product/generative-ai-tools-for-market-research-buyers-guide/  
Observed 30 September 2026: promotes source transparency, domain-specific context, internal-content integration, monitoring and research workflows; describes a “Generative Grid” applying prompts across documents.  
Evidence class: product/vendor material. Extract the general research pattern, not AlphaSense superiority claims.

### Source F — AlphaSense: AI tools for financial analysis
URL: https://www.alpha-sense.com/resources/research-articles/ai-tools-for-financial-research/  
Observed 30 September 2026: describes source-level citations, multi-document analysis, structured extraction/tables, internal-content integration, alerts and comparison workflows across several tools.  
Evidence class: vendor comparison; product strengths/weaknesses may be commercially framed.

### Source G — Harvard Business Review: When Using AI Leads to “Brain Fry”
URL: https://hbr.org/2026/03/when-using-ai-leads-to-brain-fry  
Published 5 March 2026. Public summary states that certain patterns of AI use can drive cognitive fatigue while others may reduce burnout. HBR's product description reports participant experiences such as mental fog, difficulty focusing, slower decision-making and headaches, and links excessive AI oversight to errors, decision fatigue and intention to quit.  
Evidence class: research summary/paywalled article; stronger basis for cognitive-load design than vendor opinion, but full methods/results should be checked before making precise causal claims.

## Aletheia implementation

Implemented 30 September 2026:
- `KarstenEvans/aletheia-app/aletheia-GUI.md`: judgment-first UI rules, Quiet Mode, evidence grid and visible human decision point.
- `KarstenEvans/aletheia-app/aletheia-dev.md`: nine-stage pipeline, stop criteria, perspective expansion, model-agnostic architecture and cognitive budget.
- `KarstenEvans/aletheia-app/aletheia-decision-check/`: working local-first Decision Check browser app.
- Storyteller fiction: `ToomorrowMan-and-the-Case-of-the-Missing-AI.md`.
- Cabinet of Curiosities evidence/story bridge: **Case File 42: The Artificial Intelligence That Vanished Into Everything**.

## Story bridge

The public metaphor is deliberately simple:

> The artificial intelligence did not disappear. The visible assistant disappeared while automated decisions remained embedded in ordinary systems.

The story question is therefore not merely “Where did AI go?” but **“Where did the human decision go?”**

That is a fictional framing of the design issue, not a factual claim that all real-world AI systems have become invisible.
