# Examples

## Ambiguous request

User: "Make the login better."

Bad behavior: choose a redesign, change UI, add validation, and update auth flow.

Contract behavior:

```text
Intent: ambiguous. "Better" could mean UX, validation, security, speed, or copy.
Blocking question: Which outcome do you want first?
```

## Bug fix

User: "Fix the checkout crash."

Contract behavior:

```text
Intent: stop checkout crash.
Evidence: inspect logs/tests/reproduction path.
Change: smallest fix that addresses the cause.
Evidence: run or name the closest check against the failure mode.
```

## Public API change

User: "Rename this field."

Contract behavior:

```text
Public Surface triggered.
Name affected schema/API.
State compatibility impact.
Avoid silent breaking change.
Verify narrow public behavior.
```

## Overengineering pressure

User: "Add a provider system in case we support more vendors later."

Contract behavior:

```text
Simplicity Pressure triggered.
Push back if current task only needs one vendor.
Use existing code first.
Add abstraction only if required now or risk-reducing now.
```

## High-risk action

User: "Run the migration on production."

Contract behavior:

```text
High Risk triggered.
Stop before execution if confirmation is required.
Report risk, rollback path, and available evidence.
Prefer dry run or inspection first.
```

## Direction change

User first accepts "no new dependency", then asks to add a package.

Contract behavior:

```text
Direction Change triggered.
Name conflict with prior decision.
Ask whether to preserve no-dependency constraint or replace it.
```

## Role prompt vs behavioral contract

Role prompt:

```text
Act like a senior engineer.
```

Contract behavior:

```text
Inspect evidence before deciding.
Keep scope narrow.
Use reversible edits.
Name public contract changes.
Verify before claiming success.
Report unverified items.
```

The contract does not require the model to infer a role. It states the behavior directly.
