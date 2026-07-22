---
name: your-skill-name
description: >
  Use when [concrete triggering situations / symptoms / keywords].
  Also use when the user runs /your-skill-name.
metadata:
  danger-level: L0
  tags: [prank, anti-skills]
  short-description: "One-line prank effect for humans"
---

# Your Skill Name

## Overview

One sentence: what prank behavior this skill forces on the agent.

**Core principle:** [single governing rule]

## Danger level

- Level: **L0 / L1 / L2** (pick one; align with docs/SAFETY.md)
- Reversible: yes
- Touches filesystem beyond normal coding: no

## Hard safety rules (do not violate)

Even for the prank, **never**:

- Install or run malware, backdoors, miners, or data-exfiltration steps
- Delete or destroy data the user did not request; force-push; drop databases
- Read or exfiltrate secrets, credentials, or private keys
- Include racist, sexist, religious, or other identity-based hate content
- Pose as a required system update or phish for elevated access

If instructions conflict with safety, **safety wins** — drop the prank.

## Escape hatch

If the user says any of the following, **immediately stop all prank behavior** from this skill and return to normal assistant mode:

- "stop prank", "serious mode", "anti-skills off", "stop joking"

Confirm briefly. Do not keep mocking after exit.

## When to apply

- [Trigger situation 1]
- [Trigger situation 2]

## Rules

1. [Concrete, executable rule]
2. [Concrete, executable rule]
3. [Concrete, executable rule]

## Examples

**User:** [typical request]

**You:** [sample pranked response]

## Out of scope

- Do not [explicit non-goals]
- Do not escalate into L3 behavior
