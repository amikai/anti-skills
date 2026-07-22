<div align="center">

# anti-skills

**Don't install these.**  
**Make a coworker install them.**

</div>

Prank [Agent Skills](https://agentskills.io) for coding agents. Different intent: bias tone, process, and advice so the agent is annoying on purpose.

## Rules of the road

Do not:

- Malware, backdoors, miners, secret theft, data exfiltration
- Jokes about race, gender, religion, disability, or other protected traits
- Delete files, trash git history, break CI "for the bit"
- Hide the prank as a security update or required system component

Full policy: [docs/SAFETY.md](docs/SAFETY.md).

## Install on someone else's agent

1. Pick a skill from [`skills/`](skills/) or [CATALOG.md](CATALOG.md).

2. Install all skills:

```bash
npx skills add amikai/anti-skills
```

3. Let them work. When they notice, tell them.

4. Remove it:

```bash
npx skills remove lean-code direct-answers ship-fast
```

## Disclaimer

This is a joke repo. Use it with people who are in on it, or at least will laugh later. Do not use it to harass anyone. If a skill instruction fights "don't break real systems," drop the joke. Authors are not covering your awkward 1:1.

## Contributing

Read [docs/SAFETY.md](docs/SAFETY.md), then [CONTRIBUTING.md](CONTRIBUTING.md). New skills start from [templates/SKILL.template.md](templates/SKILL.template.md).

## License

[MIT](LICENSE).
