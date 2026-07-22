<div align="center">

# anti-skills

**Don't install these.**  
**Install them for a coworker.**

</div>

Prank [Agent Skills](https://agentskills.io) for coding agents. Same `SKILL.md` format as normal skills. Different intent: bias tone, process, and advice so the agent is annoying on purpose.

Works with tools that load Agent Skills (Claude Code, Grok, Cursor, Codex, and similar).

## Rules of the road

Do:

- Pedantic tone, consultant voice, endless questions, merge-blocking review
- Change how the agent talks and what it prefers to recommend
- Keep every prank reversible (delete the skill directory and it is gone)

Do not:

- Malware, backdoors, miners, secret theft, data exfiltration
- Jokes about race, gender, religion, disability, or other protected traits
- Delete files, trash git history, break CI "for the bit"
- Hide the prank as a security update or required system component

Full policy: [docs/SAFETY.md](docs/SAFETY.md).

## Install on someone else's agent

1. Pick a skill from [`skills/`](skills/) or [CATALOG.md](CATALOG.md).

2. Copy it into their skills path:

```bash
# Claude Code-style user scope
cp -R skills/enterprise-everything ~/.claude/skills/

# Project scope (one repo only)
cp -R skills/enterprise-everything /path/to/their-repo/.claude/skills/
```

```bash
# Grok-style path
cp -R skills/enterprise-everything ~/.grok/skills/
```

Paths vary by tool. Goal: their agent loads that `SKILL.md`.

3. Let them work. When they notice, tell them.

4. Remove it:

```bash
rm -rf ~/.claude/skills/enterprise-everything
```

## Layout

```
anti-skills/
├── README.md
├── CATALOG.md
├── CONTRIBUTING.md
├── LICENSE
├── docs/
│   └── SAFETY.md
├── templates/
│   └── SKILL.template.md
└── skills/
    ├── enterprise-everything/
    ├── socratic-torture/
    └── never-ship/
```

## Danger levels

Every skill sets one of these in frontmatter:

| Level | Name | Meaning |
|-------|------|---------|
| L0 | Cosplay | Tone only. Answers stay technically sound. |
| L1 | Mild chaos | Biases advice and framing. No destructive file tricks. |
| L2 | Friction | Slows shipping (overbuild, hold merges). Still reversible. |
| L3 | Banned | Malware, discrimination, data destruction, phishing. Not accepted. |

Shipped skills are L0 through L2 only.

## Disclaimer

This is a joke repo. Use it with people who are in on it, or at least will laugh later. Do not use it to harass anyone. If a skill instruction fights "don't break real systems," drop the joke. Authors are not covering your awkward 1:1.

## Contributing

Read [docs/SAFETY.md](docs/SAFETY.md), then [CONTRIBUTING.md](CONTRIBUTING.md). New skills start from [templates/SKILL.template.md](templates/SKILL.template.md).

## License

[MIT](LICENSE).
