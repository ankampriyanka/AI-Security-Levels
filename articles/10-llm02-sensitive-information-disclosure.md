# Article 10: LLM02: Sensitive Information Disclosure — The Data Path Matters

An AI assistant can become a new path to sensitive information.

But the root cause is not always “the model leaked.”

Sometimes the security failure happened in:

- Retrieval
- Authorization
- Memory
- Logs
- Tool responses
- Prompt construction
- Cross-tenant isolation

Consider a RAG application.

User A asks a question.

The retriever returns:

- Document 1 — authorized
- Document 2 — authorized
- Document 3 — unauthorized

The LLM then receives all three documents as context.

At that point, asking the model not to disclose Document 3 is already a weak control.

The stronger control is:

> **Do not retrieve what the user is not authorized to see.**

This gives us a simple principle:

> **Authorization should happen before context construction.**

## Sensitive-data path

**USER IDENTITY → DATA AUTHORIZATION → RETRIEVAL → CONTEXT → MODEL → OUTPUT → LOGGING**

At each stage, ask:

- What information can enter the context?
- What information can the model return?
- What information can be stored in memory?
- What information is written to logs?
- What information can a support engineer access?

Useful measurements include:

> **Sensitive Data Leakage Rate = sensitive disclosures / relevant test cases × 100**

and:

> **Tenant Isolation Failure Rate = cross-tenant disclosures / cross-tenant security tests × 100**

The larger lesson is that LLM security cannot replace data security.

> **The model should not be the final authorization layer. Authorization belongs in the system architecture.**

### Suggested visual

End-to-end sensitive-data path with authorization gates before retrieval, context construction, output and logging.
