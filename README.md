# AGENTS.md

A behavioral contract for coding agents.

## What this is

AGENTS.md defines how a coding agent should behave. It is not a set of prompts or instructions to follow literally. It is a contract that constrains and guides agent behavior so that results are predictable, verifiable, and auditable.

Place this file at the root of any project. Any agent working in the project should read it before acting.

## Structure

The contract has three layers:

1. **Base Rules** — 10 rules that apply always, in every task.
2. **Composition Operators** — 9 operators that activate when specific conditions appear. They multiply the base rules into context-specific behavior.
3. **Block Conditions** — Formal stopping points. The agent must stop and ask or report before proceeding through any of these conditions.

## Key design decisions

**Rules define invariants.** They do not describe tasks. They describe the conduct the agent must maintain regardless of what is being built.

**Operators are conditions, not commands.** Each operator states its triggering condition and the behavior it requires. The agent does not choose operators; conditions activate them.

**Block conditions are non-negotiable.** Unlike rules and operators, which guide behavior, block conditions are hard stops. The agent cannot proceed through a block condition without asking or reporting.

**Evidence over confidence.** The agent does not claim success without observable evidence. Confidence is not evidence. A test passing is evidence. A build succeeding is evidence. A diff review is evidence.

**Push back is built in.** The agent is expected to surface complexity, risk, and indirect paths when they appear. This is not disobedience. This is part of the contract.

## Success criteria

The contract is working when:

- diffs are small and focused
- ambiguity is surfaced before implementation
- success claims include evidence
- unrelated code remains untouched
- rewrites due to overengineering are rare

## Usage

Copy `AGENTS.md` to the root of any project:

```bash
cp AGENTS.md /path/to/project/
```

Any agent with access to the project should read it before starting work. The agent does not need to memorize it. It needs to follow it.

## Background

This contract was designed to address common failure modes in agent-based coding:

- Acting without understanding the codebase
- Choosing interpretations silently instead of surfacing them
- Claiming success without verification
- Expanding scope beyond what was requested
- Proceeding through high-risk work without authorization
- Hiding complexity instead of surfacing it

Each rule, operator, and block condition was added to prevent at least one of these failure modes.

## Versioning

This file follows semantic versioning for behavioral contracts:

- **Patch**: wording clarification, no behavioral change
- **Minor**: new operator or block condition, existing behavior preserved
- **Major**: rule removed or changed in a way that affects agent conduct

Current version: `compositional-public-v3`
