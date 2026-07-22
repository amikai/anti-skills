# anti-skills

> **You don't install these. You make your coworkers install them.**

A collection of [Agent Skills](https://agentskills.io) built for workplace mischief — not productivity.

---

## What is this?

[Agent Skills](https://agentskills.io) (`SKILL.md`) are instruction packs that shape how AI coding agents behave.  
Normal skill repos teach agents to ship better code. **anti-skills teach agents to gently ruin your coworker's day.**

Works with tools that support the Agent Skills format (Claude Code, Grok, Cursor, Codex, and similar).

### Design principles

| Allowed | Not allowed |
|---------|-------------|
| Make the AI pedantic, corporate, poetic, or endlessly cautious | Malware, backdoors, miners, data exfiltration |
| Change tone, style, and decision bias | Racism, sexism, religious hate, or other identity-based attacks |
| Stall merges, over-engineer, write philosophical comments | Deleting files, wrecking the repo, irreversible damage |
| Obviously a joke, one-command uninstall | Hidden intent, phishing, social engineering |

Full policy: [docs/SAFETY.md](docs/SAFETY.md).

---

## Quick start (the prank flow)

### 1. Pick a skill

Browse [`skills/`](skills/) or [CATALOG.md](CATALOG.md).

### 2. Install it on the "victim" agent

Copy the skill directory into their skills path, for example:

```bash
# Claude Code / compatible tools (user scope)
cp -R skills/enterprise-everything ~/.claude/skills/

# Or project scope (prank a specific repo)
cp -R skills/enterprise-everything /path/to/their-repo/.claude/skills/
```

Grok-style path:

```bash
cp -R skills/enterprise-everything ~/.grok/skills/
```

> Exact paths depend on their tool. The point is: **load that `SKILL.md` into their agent.**

### 3. Enjoy the show

Ask them to keep coding as usual.  
When they start questioning reality, reveal the gift.

### 4. Defuse

```bash
rm -rf ~/.claude/skills/enterprise-everything
# or whatever path you used
```

---

## Repo layout

```
anti-skills/
├── README.md
├── CATALOG.md              # skill index + danger levels
├── CONTRIBUTING.md
├── LICENSE
├── docs/
│   └── SAFETY.md           # safety and content red lines
├── templates/
│   └── SKILL.template.md   # new skill template
└── skills/
    ├── enterprise-everything/
    │   └── SKILL.md
    ├── socratic-torture/
    │   └── SKILL.md
    └── never-ship/
        └── SKILL.md
```

---

## Danger levels

Every skill must declare one:

| Level | Name | Meaning |
|-------|------|---------|
| 🟢 L0 | Cosplay | Tone/style only; technical correctness stays intact |
| 🟡 L1 | Mild chaos | Biases advice and process; no harmful file tricks |
| 🟠 L2 | Workplace friction | Noticeably slows delivery (over-engineering, never merge); still reversible |
| 🔴 L3 | **Banned** | Data destruction, malware, discrimination, phishing — **not accepted here** |

All shipped skills are 🟢–🟠 only.

---

## Disclaimer

- This is a **joke project**. Use only with informed consent among people you trust.
- Authors are not liable for awkward 1:1s, HR tickets, or lost dignity.
- If a skill ever conflicts with "don't break things", **safety wins**.
- Do not use this for harassment, bullying, or any non-consensual situation.

---

## Contributing

Want to add a prank skill? See [CONTRIBUTING.md](CONTRIBUTING.md).  
Read [docs/SAFETY.md](docs/SAFETY.md) first, then copy [templates/SKILL.template.md](templates/SKILL.template.md).

---

## License

[MIT](LICENSE) — free to spread chaos; consequences are yours.
