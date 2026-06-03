---
name: cdt-change-prep
description: Update agents, rules, skills, templates, or docs in the claude-delivery-team repo. Reads key files in sequence, produces a verification summary, and primes for accurate, thorough changes. Use at the start of any session involving structural or content changes to this framework.
---

# CDT Change Prep

This repo is installed by engineering teams at scale. Every agent, rule, skill, and template ships to real production workflows. **Accuracy and depth are non-negotiable. Speed is not a goal.** A single missed reference in a rename, a stale line in the README, or an unreviewed diagram breaks the experience for everyone who depends on it.

Read the files below in sequence. Do not skim. When done, produce the verification summary described at the end.

---

## Reading sequence

**1. `CLAUDE.md`**
Repo structure, agent conventions, folder hierarchy, and the mandatory structural-change verification checklist. Internalize the checklist fully -- it governs every change in this session.

**2. `CONTRIBUTING.md`**
How agents, skills, and rules are added or modified.

**3. `.claude/skills/collaboration-contracts/SKILL.md`**
The backbone of the framework: the full dependency graph across all agent pairs. Who produces what, who gates what, who depends on what. This is the real spec.

**4. `.claude/template/feature/workflow/workflow.md`**
The canonical end-to-end workflow a consumer feature follows: all stages, phases, and human gates.

**5. `.claude/template/kickoff-prompt.md`**
The consumer entry point. Shows how the framework is actually invoked.

**6. `.claude/framework-config.md`**
File path conventions and the authoritative File locations table. All artifact path resolution derives from this.

**7. `docs/how-it-works.md`**
User-facing narrative describing the delivery sequence, all roles, and how contracts work. Any change to an agent, role, or rule may require an update here.

**8. `.claude/agents/senior-engineering-manager.md` (first 40 lines only)**
One representative agent to internalize the mandatory section order all agents follow.

---

## Confirmation (produce this after reading)

Reply with a single short message confirming you have read all files and are ready to collaborate. No summaries, no lists, no digests. Example:

> Read. I have full context on agents, rules, contracts, workflow, and the verification checklist. Ready when you are.

---

## Expanded verification (beyond grep)

CLAUDE.md defines a grep-based structural-change checklist. Grep is necessary but not sufficient. Before making any change:

**Enumerate all reference forms AND owned concepts.** For the thing being changed, list:
- Canonical name, file name, human-readable form, role abbreviation
- Every concept, artifact, or contract it owns or produces (e.g. changing `senior-backend-engineer` also means checking references to "BE", "Issues List (BE)", "BE Detailed Design", "DB Schema", "API Contract" throughout rules, contracts, and docs)

**Check all surfaces -- not just text files.**
- Text files: `grep -irn` from repo root, no filters, no exclusions
- Diagrams: `Collaboration.excalidraw` and any files under `docs/` -- grep cannot read these; review manually and flag if the change affects them
- User-facing docs: `README.md` -- verify it stays accurate after every change

**Fix every gap.** Edit each file individually. Do not batch. Do not defer. Show the full grep evidence before declaring done.
