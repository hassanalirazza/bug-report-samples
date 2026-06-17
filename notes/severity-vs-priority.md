# Severity vs. Priority

Two terms often confused in QA. Understanding the difference is essential for correct defect triage.

---

## Definitions

**Severity** — how badly the defect affects the system's functionality. Set by the tester. Technical impact.

**Priority** — how urgently the defect should be fixed. Set by the team/product owner. Business impact.

---

## The Four Combinations

| Combination | Meaning | Example |
|---|---|---|
| **High Severity + High Priority** | Major breakage, fix immediately | App crashes on checkout — users cannot pay |
| **High Severity + Low Priority** | Serious bug, but rarely hit | Crash on a deprecated feature used by almost no one |
| **Low Severity + High Priority** | Minor issue, but highly visible | Company name misspelled on the homepage |
| **Low Severity + Low Priority** | Minor and not urgent | Slight padding misalignment on a settings page |

---

## Why the Distinction Matters

A misspelled brand name on the landing page is technically a **low severity** defect — nothing is broken — but it is **high priority** because it damages credibility and is seen by every visitor.

Conversely, a crash deep inside a rarely used admin feature is **high severity** but may be **low priority** if it affects almost no users.

Triaging defects correctly on both dimensions ensures the team fixes what matters most, first.

---

## Quick Rule

- **Severity** answers: *How bad is the damage?*
- **Priority** answers: *How soon must we fix it?*
