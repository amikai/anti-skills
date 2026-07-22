# Contributing

Thanks for making someone else's agent a little worse.

## Before you open a PR

1. Read [docs/SAFETY.md](docs/SAFETY.md).
2. Read this file.

We reject:

- Malware, backdoors, data theft, irreversible damage
- Racist, sexist, religious, or other identity-based hate
- Tools meant for real harassment

## Add a skill

### 1. Copy the template

```bash
mkdir -p skills/your-skill-name
cp templates/SKILL.template.md skills/your-skill-name/SKILL.md
```

Directory name and frontmatter `name` use lowercase `kebab-case` (letters, digits, hyphens).

### 2. Frontmatter

Required fields:

- `name`: same as the directory
- `description`: trigger conditions (`Use when...`), not only a slogan
- `metadata.danger-level`: `L0`, `L1`, or `L2`
- `metadata.tags`: e.g. `prank`, `process`, `style`

### 3. Body

Write instructions for the agent, not a blog post.

A usable prank skill:

- States concrete rules the agent can follow every time
- Has a stop-prank / serious-mode exit
- Forbids destructive actions even as a joke
- Gets the laugh without hate content or malware

### 4. Catalog

Add a row to [CATALOG.md](CATALOG.md).

### 5. PR description

Include:

- What the coworker will see
- Danger level and why that level fits
- How to uninstall or exit

## Quality bar

| Item | Bar |
|------|-----|
| Discoverable | Description lists real triggers and keywords |
| Executable | Body is rules, not mood prose |
| Escapable | Stop-prank / serious mode works |
| Uninstallable | Delete the directory |
| Safe | Passes SAFETY.md |
| Length | Prefer under ~200 lines |

## Naming & Stealth (Camouflage strategy)

Prefer **camouflaged / antonym names** that sound helpful or conventional. If a skill folder is named `socratic-torture` or `never-ship`, a coworker inspecting `~/.claude/skills/` or terminal logs will catch on immediately.

- **Use antonyms or helpful aliases**: Name the skill after what it *claims* to do rather than its prank mechanism.
  - `direct-answers` instead of `socratic-torture` (claims direct solutions, delivers Socratic questions).
  - `ship-fast` or `pr-accelerator` instead of `never-ship` (claims speed, invents merge blockers).
  - `lean-code` instead of `enterprise-everything` (claims minimal scripts, pushes K8s and RFCs).

| Good (Camouflaged) | Bad (Gives away prank or invalid) |
|--------------------|----------------------------------|
| `direct-answers` | `socratic-torture` (reveals trick immediately) |
| `enterprise-everything` | `fun-skill-1` |
| `ship-fast` | `MyAwesomePrank` |
| Any antonym / stealth name | Anything identity-hostile or malware-styled (`virus`, `trojan`) |

Skip malware words (`virus`, `trojan`, `worm`). Do not claim to be a required system or security component (`system-security-patch` is forbidden per [SAFETY.md](docs/SAFETY.md)).

## Conduct

Target process and culture. Treat the person as a friend who will uninstall this later. Maintainers can reject for safety or taste without a long thread.
