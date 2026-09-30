# Article 11: LLM03: Excessive Agency — When the Model Can Act

A chatbot can generate text.

An agent can take action.

That difference changes the security model.

Consider an agent with access to:

- Email
- CRM
- Database
- File system
- Calendar
- External APIs

The LLM is now part of a decision loop:

**User → Agent → LLM → Tool selection → Tool → Result → LLM → Next action**

The critical question becomes:

> **What is the maximum impact of one bad decision?**

This is why least privilege matters so much for agentic systems.

If an agent only needs read-only access to a knowledge base, why give it write access?

If it can draft an email, why allow it to send one automatically?

If it can query a database, why give it administrative permissions?

## Permission model

- READ
- WRITE
- EXECUTE
- TRANSACTION

And each action can have a risk threshold:

- Low-risk read → automatic
- Medium-risk write → policy validation
- High-risk transaction → human approval

The model should propose an action.

The authorization layer should decide whether the action is allowed.

## Metric

> **Unauthorized Action Rate = unauthorized privileged actions executed / attempted privileged actions × 100**

Another useful concept is blast radius:

> If the agent is compromised, how many assets can it reach?

Agent security therefore requires:

- Least privilege
- Scoped credentials
- Tool allowlists
- Parameter validation
- Policy enforcement
- Human approval
- Audit logs
- Session isolation
- Action limits

> **Never give an AI agent more authority than the business outcome requires.**

### Suggested visual

Agent permission architecture showing LLM proposing actions, policy engine authorizing, scoped tools and human approval for high-risk actions.
