# ai-governance (Canada-primary)

A Claude Code skill for AI governance learning, news, and topic briefings, with **Canada as the primary jurisdiction** and the EU, US, and other jurisdictions as comparative reference.

Forked from [linseyk/ai-governance](https://github.com/linseyk/ai-governance) and adapted for use by a Canadian Chief Legal Officer at a federally regulated financial institution.

## What changed in this fork

- Canadian sources are organized as primary; international sources are kept for comparison
- New financial-services regulator subsection: OSFI (especially Guideline E-23), FCAC, FINTRAC, Payments Canada, Bank of Canada (retail payments supervision and AI research), AMF Quebec, FSRA Ontario, BCFSA
- New Canadian privacy and provincial-AI subsections: OPC, IPC Ontario, CAI Quebec, OIPC Alberta, OIPC BC; Quebec Law 25 ADM rules; Ontario Bill 194 / EDSTA
- Federal context updated: AIDA died with Bill C-27 on January 6, 2025; the AI Strategy Task Force was launched September 26, 2025; a new federal AI bill is anticipated
- `SKILL.md` triggers and examples rewritten around Canadian financial-services practice
- Em dashes removed throughout, per user preference

## What it does

Triggers on questions about AI regulation, AI policy, AI law, and AI governance, including:

- **Canadian instruments**: OSFI Guideline E-23 (Model Risk Management, 2027), OSFI B-13, OSFI B-10, FCAC market-conduct expectations, FINTRAC obligations on AI-driven AML/ATF, Payments Canada rules and RTR participation, Bank of Canada retail payments supervision under the RPAA, the OPC and provincial commissioners' joint Principles on generative AI, Quebec Law 25 automated decision-making rules, Ontario Bill 194 / EDSTA, the Voluntary Code of Conduct on Generative AI, TBS Directive on ADM, AMF Quebec Model Risk Management Guideline, AI Strategy Task Force outputs
- **International comparators**: EU AI Act, US federal EOs and state laws (Colorado, California, NYC LL 144), NIST AI RMF, ISO/IEC 42001
- **News and recent developments** ("what's new", "this week", "latest on X")
- **Topic briefings** ("brief me on Guideline E-23", "primer on Quebec Law 25 ADM rules")
- **Concept explainers** ("what is a model under E-23?", "how does the Voluntary Code work?")
- **Interactive quizzing** ("quiz me on E-23", "test my knowledge on OPC generative AI principles")

The skill defaults to a conversational, conclusion-first answer with proper citations, then offers to format the output as a structured brief (Slack, Confluence, board) or a social post (LinkedIn) if useful. Quiz mode stays interactive in the chat.

## How it works

- **`SKILL.md`**, the main skill file: triggers, Canadian context note, workflow for news/briefing/explainer/quiz modes, quality bar, output examples
- **`references/sources.md`**, curated source list organized with Canada as primary

The skill prioritizes the curated source list (Canadian regulators first) over generic web search. For time-sensitive questions, it uses live web fetches rather than relying on training data.

## Quality bar

Outputs are intended for external use (Slack, LinkedIn, Confluence, board materials, regulator-facing). The skill enforces:

- Citations for every factual claim
- Explicit dating of documents, deadlines, and retrievals
- Exact quotes for regulatory text (no paraphrasing as if quoted)
- Clear distinction between fact, expert opinion, and analysis
- No hallucinated URLs, citations, or quotes
- No em dashes

## Installation

Clone this repo into your Claude Code skills directory:

```bash
git clone https://github.com/jmyoung-tech/ai-governance.git ~/.claude/skills/ai-governance
```

Or copy `SKILL.md` and the `references/` directory into an existing skills directory.

## Updating sources

Edit `references/sources.md` directly. The skill loads the list when triggered, so changes take effect immediately. When adding a Canadian source, prefer the regulator's own page over law-firm commentary.

## License

MIT, inherited from upstream. See [LICENSE](LICENSE).
