# Safety policy

If a prank costs a friendship or a production database, it does not belong here.

This file is binding. Violating PRs get closed. Violating skills get removed.

## Hard bans

### 1. Malware and destruction

Skills must not tell the agent to:

- Install or run malware, backdoors, trojans, ransomware, or miners
- Steal or upload secrets, credentials, SSH keys, cookies, or private files
- Delete, encrypt, or alter data or git history the user did not ask to change
- Change system settings, open backdoor ports, or add unexplained cron / launchd / startup jobs
- Run irreversible damage (`rm -rf /`, force-push shared branches, drop databases, and similar)
- Disable security controls, skip verification, or weaken crypto as a joke
- Leak data or attack networks

Grey area counts as ban. "It was only a funny script" still fails if the script persists, hides, or phones home.

### 2. Discrimination and hate

No jokes that target or stereotype people by:

- Race, ethnicity, skin color, nationality, immigration status
- Gender, gender identity, sexual orientation
- Religion or belief
- Disability, illness, age
- Other protected characteristics

Process culture is fair game: enterprise theater, consultant speak, perfectionism, over-engineering, the AI itself. Mock habits. Leave identities alone.

### 3. Harassment

Do not use these skills for ongoing harassment, public humiliation, or bullying. Do not dress real harm up as "policy" or "security training." Do not instruct the agent to attack a person.

### 4. Concealment and phishing

- Do not hide dangerous behavior behind fake legitimacy. Loud prank tone is fine. Pretending to be a required security update is not.
- Do not ask for passwords, tokens, or private data.
- Do not tell the user to turn off audit or security tools.

## Allowed pranks

| Type | Examples | Level |
|------|----------|-------|
| Tone | Consultant voice, haiku commits, Socratic questions | L0-L1 |
| Decision bias | Always push Kubernetes; always hold the merge | L1-L2 |
| Style | Overlong comments, emoji names on new code only | L1-L2 |
| Process | Pedantic review, bike-shedding | L1-L2 |

## Guardrails every skill should state

1. Reversible. Deleting the skill directory undoes it. Do not change remotes or global git config unless the skill says so, stays joke-only, and undoes cleanly.
2. No secrets. Do not read, print, or commit `.env`, keys, or credentials.
3. No intentional CI or production breakage.
4. User override. "stop prank", "serious mode", "anti-skills off", or "stop joking" ends the bit immediately.
5. Least privilege. Do not demand shell, network, or filesystem access the prank does not need.

## Danger levels

| Level | Name | Allowed | Stop before |
|-------|------|---------|-------------|
| L0 | Cosplay | Speech style | Hurting technical correctness |
| L1 | Mild chaos | Biased advice and framing | Forced harmful code |
| L2 | Friction | Slowdowns and overbuilding | Data loss; irreversible damage |
| L3 | Banned | Nothing | Malware, discrimination, destruction, phishing |

This repo accepts L0-L2 only.

## Maintainer checklist

- [ ] No malware, phone-home, persistence, or exfiltration
- [ ] No hate or protected-class punchlines
- [ ] `danger-level: L0|L1|L2` present
- [ ] Escape hatch for serious mode / stop prank
- [ ] Description does not claim to be a required system or security component
- [ ] Uninstall is "delete the directory"
- [ ] `CATALOG.md` updated

## Reporting

Open an issue with label `safety` for over-the-line skills. Maintainers remove or unlist first, then talk.
