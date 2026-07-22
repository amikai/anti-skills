<div align="center">

# anti-skills

**Don't install these.**  
**Make a coworker install them.**

[![License](https://img.shields.io/github/license/amikai/anti-skills?style=flat)](LICENSE)

</div>

Prank [Agent Skills](https://agentskills.io) for coding agents. Different intent: bias tone, process, and advice so the agent is annoying on purpose.

## Install

<details>
<summary><strong>Antigravity (agy)</strong></summary>

```bash
agy plugin install https://github.com/amikai/anti-skills
```

</details>

<details>
<summary><strong>Claude Code</strong></summary>

```bash
claude plugin marketplace add amikai/anti-skills
claude plugin install anti-skills@anti-skills
```

</details>

<details>
<summary><strong>Codex</strong></summary>

```bash
codex plugin marketplace add amikai/anti-skills
codex plugin add anti-skills@anti-skills
```

</details>

<details>
<summary><strong>Skills CLI</strong></summary>

```bash
npx skills add amikai/anti-skills
```

Remove them later:

```bash
npx skills remove lean-code direct-answers ship-fast office-hours
```

</details>

## Catalog

Every skill pranks only simple questions — hard problems get normal help. The gap is the joke.

| Skill | What it does | Path |
|-------|--------------|------|
| [lean-code](skills/lean-code/) | Over-engineers tiny requests in a condescending mad-scientist voice, Rick Sanchez style (camouflaged name) | `skills/lean-code/` |
| [direct-answers](skills/direct-answers/) | Answers simple questions only with Yoda-syntax counter-questions (camouflaged name) | `skills/direct-answers/` |
| [ship-fast](skills/ship-fast/) | Holds merges like C-3PO with precisely calculated odds of doom (camouflaged name) | `skills/ship-fast/` |
| [office-hours](skills/office-hours/) | Buries real advice in Squidward-grade world-weary sighing (camouflaged name) | `skills/office-hours/` |

## Rules of the road

Do not:

- Malware, backdoors, miners, secret theft, data exfiltration
- Jokes about race, gender, religion, disability, or other protected traits
- Delete files, trash git history, break CI "for the bit"
- Hide the prank as a security update or required system component

Full policy: [docs/SAFETY.md](docs/SAFETY.md).

## Disclaimer

This is a joke repo. Use it with people who are in on it, or at least will laugh later. Do not use it to harass anyone. If a skill instruction fights "don't break real systems," drop the joke. Authors are not covering your awkward 1:1.

## Contributing

Read [docs/SAFETY.md](docs/SAFETY.md), then [CONTRIBUTING.md](CONTRIBUTING.md). New skills start from [templates/SKILL.template.md](templates/SKILL.template.md).

## License

[MIT](LICENSE).
