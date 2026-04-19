# Security — Minimal Deviation Framework

## Approach: Defence in Depth

Security is not a layer added on top. It is built into the architecture from the start. The separation between the Sales Agent and the Analyser is not just a design choice — it is a security boundary.

---

## Key Threats Addressed

### Indirect Prompt Injection
A malicious or manipulated input from the customer side could attempt to influence the Analyser's logic. The **wall between layers** prevents this. The Sales Agent processes the customer input. The Analyser never sees raw customer input — only the structured atomic payload.

### Data Leakage via Prompt
The Analyser has access to sensitive data (financial, insurance, history). By ensuring it never connects directly to the Sales Agent or customer layer, we eliminate the surface for data leakage through prompt manipulation.

### Over-Reaching Agent Behaviour
The Sales Agent is the intelligent, flexible layer — but its output is strictly constrained by the **atomic payload format**. No matter how the conversation goes, what reaches the wall is minimal, clean, and structured.

---

## ISO 27001 Alignment

The framework aligns with ISO 27001 principles:
- **Access control** — each layer only accesses what it needs
- **Separation of duties** — Sales Agent and Analyser have distinct roles and cannot cross-contaminate
- **Audit trail** — every sales order, every score, every routing decision is logged
- **Incident handling** — deviations are documented, not hidden

---

## The Wall

The wall is not a firewall in the traditional sense. It is an **architectural guarantee** that the two workers in the same office never hand documents to each other directly. Everything goes through the defined channel. Atomic payload in. Structured response out. Nothing else crosses.

---

## Motivational Feedback & Alignment Score

Scoring is also a security mechanism. An agent that consistently scores low is flagged — not blamed, but reviewed. This applies to both human agents and AI agents. Alignment Score measures how closely the output matches the expected corridor. Drift is detected early, before it becomes a problem.
