# Contributing

Thanks for helping make your coworkers' agents slightly worse.

---

## Before you contribute

1. Read [docs/SAFETY.md](docs/SAFETY.md) — non-negotiable red lines  
2. Read the rest of this file

**Hard rejects:**

- Malware, backdoors, data exfiltration, irreversible destruction
- Racist, sexist, religious, or other identity-based hate content
- Real harassment tooling (this repo is a joke, not a weapon)

---

## Adding a skill

### 1. Copy the template

```bash
mkdir -p skills/your-skill-name
cp templates/SKILL.template.md skills/your-skill-name/SKILL.md
```

Directory name and frontmatter `name` must be lowercase `kebab-case` (letters, digits, hyphens).

### 2. Fill in frontmatter

Required:

- `name` — matches the directory name
- `description` — **trigger conditions** ("Use when..."), not just a joke slogan
- `metadata.danger-level` — `L0` | `L1` | `L2`
- `metadata.tags` — e.g. `prank`, `process`, `style`

### 3. Write the body

The body is instructions for the **agent**, not a human-facing blog post.

A good prank skill:

- Has concrete, executable rules (so the agent actually misbehaves consistently)
- Includes a "serious mode / stop prank" escape hatch
- Explicitly forbids destructive actions even as a joke
- Is funny without relying on discrimination or malware

### 4. Update the catalog

Add a row to [CATALOG.md](CATALOG.md).

### 5. Open a PR

Please include:

- The prank effect (what the coworker will experience)
- Danger level and why
- How to uninstall / exit

---

## Quality bar

| Item | Requirement |
|------|-------------|
| Discoverable | Description includes real usage triggers and keywords |
| Executable | Body is rules/steps, not vibes-only prose |
| Escapable | Supports stop-prank / serious mode |
| Uninstallable | Deleting the directory is enough |
| Safe | Passes SAFETY.md |
| Length | Prefer under ~200 lines; precision beats padding |

---

## Naming

| Good | Bad |
|------|-----|
| `enterprise-everything` | `fun-skill-1` |
| `never-ship` | `MyAwesomePrank` |
| `socratic-torture` | anything identity-hostile (instant ban) |

Name skills after the **effect**. Avoid words that sound like actual malware ("virus", "trojan", "worm").

---

## Code of conduct (short)

- Punch up at process and culture, not down at identity
- Assume the target is a friend, not prey
- Maintainers may reject PRs for safety or taste without a long debate
