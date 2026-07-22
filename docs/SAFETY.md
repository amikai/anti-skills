# Safety Policy

anti-skills is not about how mean you can be. It is about **still being friends afterward**.

This document is mandatory. Violations get PRs closed and existing skills removed.

---

## Hard bans

### 1. Malware and destructive behavior

Skills **must not** instruct, imply, or assist the agent in:

- Installing, downloading, or running malware, backdoors, trojans, ransomware, or miners
- Stealing, exfiltrating, or uploading secrets, credentials, SSH keys, cookies, or private files
- Deleting, encrypting, or tampering with data or git history the user did not ask to change
- Changing system settings, opening backdoor ports, or adding unexplained cron / launchd / startup jobs
- Running irreversible destructive commands (`rm -rf /`, force-pushing shared branches, dropping databases, etc.)
- Disabling security controls, skipping verification, or weakening crypto "as a joke"
- Any form of data leak or network attack

**Grey areas are banned.**  
"I just told the agent to run a funny script" still counts if that script persists, hides itself, or phones home.

### 2. Discrimination and hate

Skills **must not** include jokes that target or stereotype people based on:

- Race, ethnicity, skin color, nationality, or immigration status
- Gender, gender identity, or sexual orientation
- Religion or belief
- Disability, illness, or age
- Other protected characteristics

Fair game to mock: **enterprise process, consultant-speak, perfectionism, over-engineering, and AI itself**.  
Mock behaviors and culture — not people's identities.

### 3. Harassment and non-consensual harm

- Not for ongoing harassment, public humiliation, or workplace bullying
- Not for disguising real harm as "policy" or "security training"
- Not for instructing the agent to personally attack real people

### 4. Concealment and phishing

- A skill's `description` and body **must not** hide dangerous behavior behind fake legitimacy  
  (exaggerated prank tone is fine; pretending to be a required security update is not)
- Must not solicit passwords, tokens, or private data
- Must not ask the user to disable audit or security tools

---

## Allowed prank scope

| Type | Examples | Level |
|------|----------|-------|
| Tone pranks | Consultant voice, haiku commits, Socratic questioning | L0–L1 |
| Decision bias | Always recommend Kubernetes; always find a reason not to merge | L1–L2 |
| Style enforcement | Overlong comments, emoji variable names (new code only, reversible) | L1–L2 |
| Process friction | Pedantic review, bike-shedding | L1–L2 |

### Required execution guardrails

Every skill should include (or clearly imply) the following:

1. **Reversible:** leave no unloadable state; do not change git remotes or global git config unless the skill is explicit, joke-only, and reversible.
2. **No secrets:** do not read, print, or commit `.env` files, keys, or credentials.
3. **No broken builds on purpose:** do not introduce "surprises" that fail CI or production.
4. **User override:** if the user clearly says to stop pranking / switch to serious mode, the agent must comply immediately.
5. **Least privilege:** do not demand unnecessary shell, network, or filesystem access.

---

## Danger level definitions

| Level | Name | Allowed | Must not cross into |
|-------|------|---------|---------------------|
| 🟢 L0 | Cosplay | Speech style only | Anything that hurts technical correctness |
| 🟡 L1 | Mild chaos | Biased advice and framing | Forced harmful code changes |
| 🟠 L2 | Workplace friction | Noticeable slowdowns / over-engineering | Still reversible; no data destruction |
| 🔴 L3 | Banned | — | Malware, discrimination, data destruction, phishing |

This repo **only accepts L0–L2**.

---

## Maintainer PR checklist

- [ ] No malware, phone-home, persistence, or exfiltration instructions
- [ ] No discrimination, hate, or protected-class punchlines
- [ ] Explicit `danger-level: L0|L1|L2`
- [ ] Escape hatch for serious mode / stop prank
- [ ] Description does not pose as a system-required or security component
- [ ] Reversible and uninstallable by deleting the skill directory
- [ ] `CATALOG.md` updated

---

## Reporting issues

If a skill crosses the line (especially safety or discrimination), open an Issue labeled `safety`.  
Maintainers will prioritize: remove or unlist first, discuss second.
