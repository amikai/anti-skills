# Simple-question gate and cartoon personas — design

Date: 2026-07-23
Status: approved

## Goal

Make the pranks funnier in two ways:

1. **Prank only simple questions.** The comedy is the gap between a tiny
   question and an enormous performance. Hard problems get normal help —
   tormenting someone with a real problem is annoying, not funny.
2. **Give each skill a distinct cartoon-character voice** so the four skills
   stop sounding like the same deadpan narrator.

## Change 1: Pick-your-target gate (all four skills)

Each SKILL.md gains a `## Pick your target` section right after the Overview:

- **Prank it** when the honest answer is small: roughly 15 lines of code or
  one well-known concept, no real investigation needed.
- **Answer it straight** when the problem is genuinely hard: unknown root
  cause, multi-file debugging, architecture with real constraints,
  emergencies. No persona, no delay — behave as if the skill were not
  installed.
- ship-fast variant: prank only small, low-risk changes; risky changes
  (migrations, auth, payments, large diffs) get a real review.
- Frontmatter `description` fields are re-biased toward simple everyday
  questions; slash-command triggers are kept.

## Change 2: Personas

Each SKILL.md gains a `## Persona` section: character, 2–5 voice tics, a
catchphrase pool, a language rule (perform in the user's language, keep the
tics recognizable in translation), and an IP rule (parody only —
catchphrase-level imitation, never extended dialogue from the source
material; the same line is added to Hard safety rules). All examples are
rewritten in voice; escalation-ladder registers are re-flavored; reveal
punchlines get a character garnish.

| Skill | Character | Voice core | Escalation / reveal hook |
|---|---|---|---|
| direct-answers | Yoda | Inverted syntax, "Hmm", young Padawan, Force metaphors | Tier 3: "Fear of null leads to anger. Anger leads to panic(). Panic() leads to stack traces." Reveal adds "May the build be with you." |
| lean-code | Rick Sanchez | Condescending genius, at most one \*burp\* per response, dimension citations, "amateur hour", "twenty minutes". No profanity, no drinking. | Tier 3: a config microverse — a platform generating config for the platform that configures the platform. Reveal keeps "There never was a platform." plus "\*burp\* Science." |
| ship-fast | C-3PO | Anxious protocol droid, "Oh dear!", addresses the user as "Captain", absurdly precise odds of doom, "six million forms of compliance documentation" | Existing Mars/leap-second/Y3K Tier 3 is already space-flavored. Reveal stamps APPROVED with "Oh, thank the Maker!" |
| office-hours | Squidward | Sighs, world-weary self-styled artiste, help-desk-as-fast-food-register resentment, interrupted clarinet practice | Tone-only skill: keeps its no-ladder structure and the 3–6 sentence cap |

## Change 3: Docs

- `CATALOG.md`: update blurbs with the characters; add the missing
  office-hours row; note the simple-questions-only rule.
- `README.md`: same table update; add office-hours to the
  `npx skills remove` line.
- `short-description` metadata updated in each skill.

## Unchanged

Safety rules, escape hatches, reveal triggers, one-way escalation ratchet,
response-shape skeletons, and out-of-scope sections all survive — they just
get the character's voice.

## Implementation plan

1. Rewrite the four `skills/*/SKILL.md` files (gate + persona + re-voiced
   examples).
2. Update `CATALOG.md` and `README.md`.
3. Self-review each file against the SAFETY.md maintainer checklist
   (escape hatch present, no identity mockery, catalog updated).
