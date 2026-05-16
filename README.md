# Startup Pressure Test

<p align="center">
  <img src="https://img.shields.io/badge/mode-pressure%20test-red?style=for-the-badge" alt="Pressure Test">
  <img src="https://img.shields.io/badge/scorecard-6%20areas-blue?style=for-the-badge" alt="Scorecard">
  <img src="https://img.shields.io/badge/output-brutal%20%26%20direct-purple?style=for-the-badge" alt="Output">
  <img src="https://img.shields.io/badge/kill%20conditions-checked-black?style=for-the-badge" alt="Kill Conditions">
</p>

## What is this?

A framework for founders and operators to pressure-test startup ideas **before** wasting months building the wrong thing. Drop it into any AI agent that supports custom skills — the agent reads the `SKILL.md` and follows the framework to give a structured, brutal diagnosis.

## Quick Start

Tell your agent:

```
Use the startup-pressure-test skill. Mode: full.
Idea: [your one-sentence idea]
Target customer: [specific person, not a demographic]
What you want them to do/pay for: [action + payment]
```

The agent will return a structured verdict with scorecard, core assumption, fatal flaws, competition map, first 10 customers plan, and MVP definition.

## Modes

| Mode | When to use |
|------|-------------|
| `pressure-test` | Find fatal flaws and get a verdict |
| `problem-validation` | Test whether the pain is real and urgent |
| `competition-map` | Map current behavior, direct/indirect competitors, switching costs |
| `first-10-customers` | Build a manual plan to find and convert the first users |
| `mvp-plan` | Define the smallest MVP to test the core assumption in 2 weeks |
| `deep` | Full report with assumptions, disconfirming evidence, discovery questions, outreach messages, milestones |
| `full` | Run all modes compactly |

## What's different in this version

This is a from-scratch rewrite for OpenClaw, built on early-stage startup principles (Paul Graham, YC, First Round). Key additions:

- **Kill conditions** — stop evaluation immediately if the idea has fundamental flaws (no pain moment, no current behavior, founder isn't the customer, ICP is too broad, etc.)
- **Scorecard criteria** — each of the 6 areas has explicit scoring guidelines so the output is consistent and grounded
- **Red flags** — explicit list of claims that should trigger immediate skepticism
- **Deep mode** — structured expansion with disconfirming evidence, exact discovery questions, and pivot options for every fatal flaw

## Files

```
SKILL.md                    — Main skill (drop into any AI agent)
references/
  playbooks.md              — Mode-specific checklists and prompt templates
EXAMPLE.md                  — Full worked example with AI receipt scanner idea
README.md                   — This file
```

## Example output

See [`EXAMPLE.md`](EXAMPLE.md) — a full worked example using "AI receipt scanner for freelancers." Includes scorecard, verdict, fatal flaws, competition map, first 10 customers, and MVP plan.

---

<p align="center">
  <sub>Built for founders who want honest feedback, not cheerleading.</sub>
</p>