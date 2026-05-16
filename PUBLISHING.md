# Publishing Guide

Use this checklist to publish the repository cleanly.

## Repository name

Recommended:

```text
agent-behavior-contract
```

Alternative:

```text
compositional-agents-md
```

## Description

```text
Behavioral contract for coding agents: base rules, context operators, block conditions, and auditable handoff.
```

## Suggested topics

```text
agents
ai-agents
coding-agents
agents-md
claude-code
codex
cursor
llm
software-engineering
prompt-engineering
```

## Pre-publish checklist

- [ ] Confirm `AGENTS.md` is the latest version.
- [ ] Confirm `CLAUDE.md` mirrors `AGENTS.md`.
- [ ] Confirm `AGENTS.min.md` matches the same core behavior.
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
I published a small AGENTS.md / CLAUDE.md contract for coding agents.

Most agent instructions assign a role. This one models behavior.

The contract uses:
- base behavioral rules
- context operators
- block conditions
- auditable handoff

The design idea is simple:
specialized behavior = base rules × context operators

Repo: <link>
```

## Release note

```text
v0.1.0: public-ready draft of Agent Behavior Contract.
```
