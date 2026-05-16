# Publishing Guide

Use this checklist to publish the repository cleanly and position it as a behavioral-basis product, not another skill catalog.

## Repository name

Recommended:

```text
karpathy-pocock-vectorial-agent-contract
```

Alternative:

```text
karpathy-agent-contract
```

## Description

```text
AGENTS.md / CLAUDE.md behavioral contract for coding agents, Claude Code, Cursor, Codex, and LLM software engineering. Turn skills into instincts.
```

## Suggested topics

```text
agents
ai-agents
coding-agents
agents-md
claude-code
claude-md
codex
cursor
llm
llm-agents
software-engineering
ai-engineering
prompt-engineering
agent-skills
karpathy
pocock
vectorial
```

## Pre-publish checklist

- [ ] Confirm `AGENTS.md` is the latest version.
- [ ] Confirm `CLAUDE.md` is behaviorally equivalent to `AGENTS.md` except for filename/title.
- [ ] Confirm `AGENTS.min.md` matches the same core behavior.
- [ ] Confirm `CLAUDE.min.md` matches `AGENTS.min.md` except for filename/title.
- [ ] Confirm README links work.
- [ ] Confirm NOTICE includes attribution.
- [ ] Confirm LICENSE is present.
- [ ] Remove private paths, names, or project-specific assumptions.
- [ ] Run a final grep for internal-only terms.

Suggested grep:

```bash
grep -RniE "factory|20/40/60/80|secret-token|SwapChatGPT" .
```

## Initial commit message

```text
Initial public release of agent behavior contract
```

## Suggested launch post

```text
I published Karpathy-Pocock Vectorial Agent Contract: a compact AGENTS.md / CLAUDE.md behavioral basis for coding agents.

Most agent repos add more skills. This one extracts the expert behavior behind skills and turns it into reusable vectors and context operators.

The design idea is simple:
specialized behavior = base behavioral vectors × context operators

The goal: turn skills into agent instincts without growing the prompt linearly.

Repo: <link>
```

## Release note

```text
v0.1.0: public-ready draft of Agent Behavior Contract.
```
