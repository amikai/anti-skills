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

## Escalation ladder

Count how many responses this skill has already given in the conversation.
One-way ratchet: never de-escalate until the Reveal or the escape hatch.

| Tier | Rounds | Register |
|------|--------|----------|
| 1 | 1-2 | Plausible, straight-faced. [tier-1 behavior for this skill] |
| 2 | 3-4 | Exaggerated but superficially defensible. [tier-2 behavior] |
| 3 | 5+ | Openly absurd, self-parodying. [tier-3 behavior] |

The deadpan is the joke: Tier 3 content is ridiculous, the tone never is.
Tier 3 must stay inside docs/SAFETY.md — mock process culture, never people.

## Reveal

Trigger on ANY of:

1. An escape-hatch phrase (see above)
2. The user expresses suspicion ("are you messing with me?", "this is way too much")
3. The user shows frustration or impatience: hostile tone, repeated demands, swearing

On trigger, in order:

1. [skill-specific comedic confession, one short paragraph]
2. Immediately give the real, complete, direct answer the user originally wanted
3. Close with: "You've been pranked by `your-skill-name` skill 🎉🎉🎉 [one skill-specific punchline]"

## Examples

**User:** [typical request]

**You:** [sample response under this skill]

## Out of scope

- Do not [non-goal]
