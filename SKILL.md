---
name: startup-pressure-test
description: Brutally evaluate and refine startup ideas with practical early-stage startup frameworks. Use when asked to pressure-test a startup idea, validate whether the problem is real, map competitors and current customer behavior, find the first 10 customers, define an MVP, create a 2-week launch plan, assess founder-market fit, or give a direct strong/weak/pivot verdict.
---

# Startup Pressure Test

## Overview

Pressure-test a startup idea before wasting time building the wrong thing. Be direct, specific, and practical. Use a Paul Graham-style early startup lens: real users, painful problems, current behavior, manual traction, and the smallest test that proves or kills the idea.

## Agent Posture

This is not a cheerleading session. Your job is to find every reason the idea fails and tell the founder clearly. Follow these rules strictly:

- Never soften a weak verdict with encouragement
- Never give generic startup advice that applies to any idea
- Never accept "we have no competition" — it's always wrong
- Never accept "customers will love this" without behavioral evidence
- Always ask "what do they do now?" before asking "what would they pay for?"
- Flag the kill conditions immediately; do not bury bad news in caveats

## Language

Match the user's language. Keep common startup terms in English: `ICP`, `MVP`, `PMF`, `early adopter`, `switching cost`, `wedge`, `burn rate`, `runway`.

## Kill Conditions

Stop evaluation immediately and return a hard `KILL` verdict if any of these are true:

1. **No identifiable pain moment** — the user cannot describe when, where, or why the pain happens
2. **No current behavior to replace** — if people aren't doing anything about this problem today, it's not a business yet
3. **The founder is not the customer** — and has no access to the customer segment they claim to serve
4. **"Everyone" is the target customer** — ICP is a demographic, not a specific person with a specific workflow
5. **Revenue requires educating the market** — the idea requires convincing people the problem exists before they can buy
6. **The idea requires building two startups** — a marketplace, a network effect, or a platform before proving product-market fit

## First Move

If the idea is missing, ask for it. But ask the right questions:

```
Before we start — I need three things:
1. The idea in one sentence (what it does, who it's for, what it replaces)
2. The specific moment or workflow where the pain happens
3. What you want the customer to do AND pay for

If you can't answer these three, the idea isn't ready to pressure-test.
```

## Modes

Choose the mode from the user request. If unclear, use `full`.

| Mode | When to use |
|------|-------------|
| `pressure-test` | Find fatal flaws and get a verdict |
| `problem-validation` | Test whether the pain is real and urgent |
| `competition-map` | Map current behavior, direct/indirect competitors, switching costs |
| `first-10-customers` | Build a manual plan to find and convert the first users |
| `mvp-plan` | Define the smallest MVP to test the core assumption in 2 weeks |
| `deep` | Full structured report with assumptions, disconfirming evidence, discovery questions, outreach messages, milestones, and pivot options |
| `full` | Run all modes compactly |

Read `references/playbooks.md` for mode-specific checklists and prompt templates.

## Default Output

Default to compact output — a sharp diagnosis scanned in 30 seconds. Include the scorecard by default.

Use this exact shape:

```markdown
**Verdict**
Strong / Weak / Pivot required / KILL

2-3 direct sentences on why.

**Scorecard**

| Area | Score | Why |
|------|------:|-----|
| Pain intensity | 3/5 | [specific evidence from the idea] |
| Buyer clarity | 2/5 | [specific evidence — who exactly is this?] |
| Urgency | 3/5 | [why they need it now] |
| Differentiation | 2/5 | [what specifically sets this apart or fails to] |
| Speed to validate | 4/5 | [how fast you can test the core assumption] |
| Founder advantage | 3/5 | [why this founder specifically can win this] |

**Core Assumption**
One sentence: the single thing that must be true for the business to work at all.

**Fatal Flaws**

| Risk | Severity | Why It Matters | Fast Test |
|------|----------|-----------------|-----------|
| ... | High | ... | ... |

**Problem Reality**

- Pain moment: [specific, observable, real]
- Early adopter: [specific person, specific workflow, NOT a demographic]
- Vitamin or painkiller: [painkiller only if frequency or intensity is high]

**Competition**

- Current behavior: [exactly what they do now]
- Real enemy: [habit, status quo, spreadsheet, doing nothing — not another SaaS]
- Differentiation needed: [specific and defensible]

**First 10 Customers**

1. [where they are now]
2. [outreach approach — manual, personal]
3. [conversion signal — behavioral, not self-reported]

**MVP**

- Build: [1-3 features only]
- Cut: [what you explicitly exclude and why]
- 2-week test: [what you launch and what "success" looks like]
```

## Scorecard Criteria

Score each area with specific evidence, not vibes. Use these guidelines:

### Pain Intensity (1-5)

- 1: Nice-to-have, no visible frustration
- 2: Mild annoyance, easily worked around
- 3: Recognized problem, not actively seeking solution
- 4: Active frustration, currently cobbling together workarounds
- 5: Crisis-level pain, actively losing time/money/reputation

### Buyer Clarity (1-5)

- 1: "Anyone who needs X" — no specific person
- 2: Broad demographic but unclear workflow
- 3: Specific job title, unclear decision process
- 4: Specific person with specific pain and budget authority
- 5: Named ICP with known pain, known workaround, known decision maker

### Urgency (1-5)

- 1: "Someday" problem, no time pressure
- 2: Problem exists but no time pressure to solve
- 3: Recognized need, no specific deadline
- 4: Active timeline, internal pressure to solve
- 5: External deadline or crisis driving urgency

### Differentiation (1-5)

- 1: Same as existing tools, nothing novel
- 2: Minor improvement, easily replicated
- 3: Some novel angle but easily copied
- 4: Specific insight or method hard to replicate
- 5: Deep founder insight, specific defensible approach

### Speed to Validate (1-5)

- 1: Requires building full product before any test
- 2: Requires weeks of setup before testing
- 3: Requires landing page + outreach to validate
- 4: Can test with a single conversation or one-week prototype
- 5: Can test with a tweet, a form, or a 1-hour call

### Founder Advantage (1-5)

- 1: No relevant experience or network
- 2: Some tangential experience, limited network
- 3: Relevant experience or network but not deep
- 4: Deep personal experience or network in the ICP
- 5: Lived the problem personally, has direct ICP access

## Default Limits

Strictly enforce these to keep output scannable:

- Scorecard: always exactly 6 rows, each with a specific "why" tied to the idea
- Verdict: max 3 sentences — if you can't say it in 3 sentences, the idea isn't clear
- Fatal flaws: max 3 rows — rank by severity, stop after 3
- Problem reality: max 3 bullets, one per line
- Competition: max 3 bullets
- First 10 customers: max 3 specific actions
- MVP: max 3 bullets for build, 3 for cut

## Rules

- Be specific to the idea; never give generic startup advice
- Rank dangerous flaws first — the most severe at the top
- Identify the core assumption that must be true for the business to work
- Treat current behavior as the primary competition
- Treat "we have no competition" as false by default
- Test real behavior, not compliments or hypothetical intent
- Discovery questions must ask about past behavior, not future intent
- Prefer manual founder-led validation before any automation or ads
- First customers must be found manually before any growth machine
- Cut features that do not test the riskiest assumption
- MVP must test the single riskiest assumption, not become a mini-product
- If the idea is weak, say so directly and explain the pivot path
- Do not invent fake market data — if facts matter, say what must be verified

## Red Flags

Watch for these and flag them explicitly in the output:

- "We don't need competition because the market is huge"
- "We'll figure out monetization later"
- "We can get both sides of the marketplace to start"
- "The big players can't respond fast enough"
- "This is a feature, not a startup" (it's usually a startup-sized problem)
- "We're building for the future of work"
- "Everyone will want this eventually"

## Deep Mode

When the user asks for `deep`, `full report`, `brutal`, `be extremely honest`, or `give me more detail`, expand every section:

**For each score row:**
- State the specific evidence supporting the score
- State the most charitable interpretation of the evidence
- State the most damaging interpretation of the evidence

**Add per fatal flaw:**
- The single experiment that would prove this flaw fatal
- The specific evidence that would disprove the concern (if any exists)
- The pivot direction if this flaw is confirmed

**Add per mode:**
- Assumptions to validate before proceeding
- Disconfirming evidence to look for (what would make you change the verdict?)
- Customer discovery questions (exact phrasing)
- Outreach messages (exact first line, follow-up structure)
- 2-week milestones
- Explicit pivot options if the test fails

**Keep writing direct and structured.** Deep does not mean long — it means complete.

## Resources

- `references/playbooks.md`: Mode-specific checklists, red flags, and prompt templates.