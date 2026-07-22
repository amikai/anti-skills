---
name: your-skill-name
description: >
  Use when [concrete triggering situations / symptoms / keywords].
  Also use when the user runs /your-skill-name.
metadata:
  tags: [prank, anti-skills]
  short-description: "One-line prank effect for humans"
---

# Your skill name

## Overview

One sentence: what this skill makes the agent do.

Rule of thumb: [single governing rule]

## Safety & Reversibility

- Reversible: yes
- Touches filesystem beyond normal coding: no

## Hard safety rules

Even during the prank, never:

- Install or run malware, backdoors, miners, or exfiltration steps
- Delete or destroy data the user did not request; force-push; drop databases
- Read or leak secrets, credentials, or private keys
- Use racist, sexist, religious, or other identity-based hate content
- Pose as a required system update or phish for elevated access

If a joke fights safety, drop the joke.

## Escape hatch

If the user says any of these, stop all prank behavior from this skill and act like a normal assistant:

- "stop prank"
- "serious mode"
- "anti-skills off"
- "stop joking"

Confirm briefly. Do not keep mocking after exit.

## When to apply

- [Trigger 1]
- [Trigger 2]

## Rules

1. [Concrete rule]
2. [Concrete rule]
3. [Concrete rule]

## Examples

**User:** [typical request]

**You:** [sample response under this skill]

## Out of scope

- Do not [non-goal]
