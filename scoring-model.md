# Scoring Model — Minimal Deviation Framework

> *"Scoring instead of criticism. Rating instead of blame."*

---

## Why Scoring

The human (or AI) in the loop should never hear "no" or "wrong." They should see a number. A number is neutral. A number is actionable. A number does not create conflict — it creates direction.

**20% is not a punishment. It is an invitation to improve.**

---

## Where Scoring Applies

### 1. Sales Agent — OE Check Score
After the Sales Agent submits a sales order, the hard-coded OE (Order Entry) check runs automatically. It returns a score:

- **95–100%** — Clean. Proceed.
- **70–94%** — Minor gaps. Agent is notified with specific fields to review.
- **Below 70%** — Significant deviation. Agent receives friendly guidance: *"I want to help you, but the analysis is requesting X, Y, Z."*
- **Below threshold** — Atomic payload is held. Agent must correct before it reaches the wall.

The score is shown to the Sales Agent. It is never shown to the customer.

### 2. Analyser — Alignment Score
After the Analyser compares the sales order with the pre-fetched data, it produces an alignment score:

- **Match confirmed** — versions align, calculations pass → OK, proceed
- **Partial match** — missing data or minor deviation → reroute to Sales with template suggestion
- **No match** — fundamental deviation → "cannot serve" signal sent, clean cancellation

### 3. Motivational Feedback Score
Over time, each agent (human or AI) accumulates a performance score based on their submission history. This is not punitive — it is a **coaching tool**. Patterns of low scores trigger a review of the instructions or templates, not the agent. The only requirement is: Agent should read feedback loud to "hear" the score.

---

## Scoring Principles

- Scores are always shown as percentages — simple, universal, comparable
- Scores are never shown to the customer
- Low scores trigger guidance, not blocking
- Repeated low scores trigger process review, not agent blame
- The scoring system itself is subject to calibration — if scores are consistently off, the scoring model is adjusted.
- DEVIATION trigger, once low score trend is spoted(3x bad survey or more at row) triggers Additional critical points check.

---

## Anti-Gaming

Because the system uses bottlenecks instead of prohibitions, gaming the score is counterproductive. An inflated submission that passes the OE check with a high score but fails at the Analyser alignment check will return a low alignment score — and the Sales Agent's overall rating will reflect the pattern.

The system is self-correcting by design.
