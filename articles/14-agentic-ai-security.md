# Article 14: Agentic AI Security: The Attack Surface Expands When AI Can Act

An LLM generates.

An agent acts.

That single difference expands the security architecture.

An agent may have:

- Identity
- Memory
- Tools
- Permissions
- Goals
- Planning
- External connections
- Long-running sessions

Now imagine:

**User → Agent → Planner → Tool → External system → Result → Memory → Next action**

There are many more trust boundaries.

## Agent security review

### Identity
What identity does the agent use?

### Authorization
Which actions is it allowed to perform?

### Memory
What information can persist between interactions?

### Tools
Which tools can it invoke?

### Context
Which instructions and data enter its reasoning context?

### Action
Which actions require approval?

### Observability
Can we reconstruct what happened?

One particularly important concept is delegated authority.

The agent should not automatically inherit all permissions of the human or service account behind it.

Instead:

**Human identity → Agent identity → Scoped permission → Specific action**

This creates a controllable trust boundary.

For high-impact actions:

**PROPOSE → VALIDATE → APPROVE → EXECUTE → LOG**

For lower-risk actions:

**PROPOSE → POLICY CHECK → EXECUTE → LOG**

The security objective is not to make agents incapable of acting.

It is to make their authority explicit, bounded and observable.

> **That is the difference between autonomous capability and uncontrolled autonomy.**

### Suggested visual

Agent trust-boundary architecture with identity, memory, tools, policy engine, human approval and audit trail.
