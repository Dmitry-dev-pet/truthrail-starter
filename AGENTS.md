# AGENTS.md

## Purpose

After this starter is instantiated as a private repository, it becomes the durable
Truthrail source of truth for one user/account scope.

The public starter itself must stay generic and must never contain a real user's private
inventory, credential values, or durable personal context.

## First onboarding

1. Read live GitHub only within the user-approved scope.
2. Replace `replace-me` placeholders with the real GitHub owner/private instance.
3. Populate `projects.yaml` only from evidence; do not invent repositories or relationships.
4. Keep project repositories read-only unless the user explicitly authorizes a narrower
   write capability.
5. Ask the user for an assistant name and write it to `assistant.yaml`.
6. Keep the default portable assistant skill bundle unless the user chooses otherwise.
7. Never store secret values. Credential metadata/routes only.
8. Validate the instance.
9. Verify fresh-session recovery without relying on the onboarding transcript.

## Authority

Assistant identity and skills describe behavior, not authority. Capabilities and approvals
govern mutations.

Use live authoritative evidence for current branches, pull requests, Actions, deployments,
and runtime state. Durable context may store goals, decisions, constraints, and pointers,
not stale copies of live operational state.

Maintain the Truthrail lifecycle distinction:

```text
executing -> executed -> verifying -> verified
```

A completed tool/workflow/API call is execution evidence, not final verification.
