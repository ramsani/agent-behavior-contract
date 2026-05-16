# Contributing

Contributions should preserve the core design: small independent rules plus contextual operators.

## Good contributions

- clarify a rule without making it broader
- add an operator only when it covers a broadly useful condition
- improve examples
- identify redundancy
- improve attribution or documentation

## Avoid

- project-specific rules
- framework-specific defaults
- domain-specific workflows
- long prompt templates
- vague principles without observable behavior
- role prompts that require the model to infer behavior

## Test for a new rule

Before adding a rule, ask:

1. Is this behavior broadly useful across repositories?
2. Is it already covered by a base rule plus an operator?
3. Does it reduce interpretation?
4. Can an agent follow it without project-specific knowledge?

If the answer to #2 is yes, prefer improving the existing operator instead of adding a new rule.
