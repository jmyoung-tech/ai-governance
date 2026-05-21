# ai-governance

A Claude Code skill for AI governance learning, news, and topic briefings.

## What it does

Triggers on questions about AI regulation, AI policy, AI law, and AI governance — including:

- Specific regulations (EU AI Act, US executive orders, NIST AI RMF, ISO/IEC 42001, state-level laws like the Colorado AI Act and NYC LL 144)
- News and recent developments ("what's new", "this week", "latest on X")
- Topic briefings ("brief me on the Colorado AI Act", "primer on FLOPs thresholds")
- Concept explainers ("what is a foundation model under the AI Act?", "explain ISO 42001")
- Interactive quizzing ("quiz me on the EU AI Act", "test my knowledge of NIST AI RMF") — one question at a time, mixed format, cited explanations

The skill defaults to a conversational answer with proper citations, then offers to format the output as a structured brief (for Slack/Confluence/email) or a social post (for LinkedIn) if useful. Quiz mode stays interactive in the chat.

## How it works

- **`SKILL.md`** — the main skill file: triggers, workflow for news vs briefing vs explainer modes, quality bar, output examples.
- **`references/sources.md`** — curated source list (regulators, standards bodies, law firms, research, trade press, trackers). Edit freely to add or remove sources.

The skill prioritizes the curated source list over generic web search. For time-sensitive questions, it uses live web fetches rather than relying on training data.

## Quality bar

Outputs from this skill are intended for external use (Slack, LinkedIn, Confluence, customer-facing). The skill enforces:

- Citations for every factual claim
- Explicit dating of documents, deadlines, and retrievals
- Exact quotes for regulatory text (no paraphrasing as if quoted)
- Clear distinction between fact, expert opinion, and analysis
- No hallucinated URLs, citations, or quotes

## Installation

Clone this repo into your Claude Code skills directory:

```bash
git clone https://github.com/linseyk/ai-governance.git ~/.claude/skills/ai-governance
```

Or copy `SKILL.md` and the `references/` directory into an existing skills directory.

## Updating sources

Edit `references/sources.md` directly — it is plain markdown. The skill loads the list when triggered, so changes take effect immediately.

## License

MIT — see [LICENSE](LICENSE).
