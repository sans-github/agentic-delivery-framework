This is an AI-assisted software development framework built on Claude Code. It comes with specialized agents that mimic a real scrum team, designed to deliver reliably through role-specific skills and predefined rules that enforce engineering and coding conventions. They collaborate with each other the way real team members do, stop at every major milestone to wait for your input, and pick up exactly where you left off if a session is interrupted. Nothing moves forward without your approval.

Used to ship [full-stack web applications](https://github.com/sans-github/fitness-tracker-app) (Java, Spring Boot, React) deployed on AWS with Terraform, and Mac desktop applications.

---

## Get started

### Install

`bash <(curl -fsSL https://raw.githubusercontent.com/sans-github/agentic-delivery-framework/main/install.sh)`

Copies agents, rules, skills, and templates into `.claude/`, and wires up `CLAUDE.md` so Claude Code loads your stack config automatically. Commit the result to lock the version.

### Try it first (recommended)

Type `/feature-init-dry-run` before committing to a real feature. Every agent writes placeholder output instead of real artifacts, but all checkpoints, commits, and progress steps fire for real. You see exactly how the team operates before anything real gets built.

### Run your first feature

Type `/feature-init` to start. Claude asks for your requirements, coordinates the team, and checks in with you at each step before moving on.

```mermaid
journey
    title Your checkpoints in /feature-init
    section Kickoff
      💬 Share requirements: 5: You
      ⭕ Approve kickoff plan: 5: You
    section Discovery
      ⭕ Approve PRD: 5: You
    section Design
      ⭕ Approve mocks: 5: You
    section Planning
      ⭕ Approve system architecture: 5: You
      ⭕ Approve high-level design: 5: You
    section Implementation
      ⚙️ Agents build autonomously: 3: Agents
      ⭕ Approve deployment plan: 5: You
    section Validation
      ⭕ Sign off on release: 5: You
```

After release, three wrap-up stages run automatically: documentation refresh, consolidating the product baseline, and release sign-off. None are skippable.

---

## Learn more

- [How it works](docs/how-it-works.md)
- [Contributing](CONTRIBUTING.md)
