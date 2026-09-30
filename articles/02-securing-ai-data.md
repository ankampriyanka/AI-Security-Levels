# Article 02: Securing AI Data: The First Security Boundary

Before an AI model produces an answer, someone had to give it data.

That data may include:

- Training datasets
- Fine-tuning datasets
- User prompts
- Inference data
- Customer information
- RAG documents
- Logs and traces
- Feedback data
- Embeddings

From a security perspective, data is not simply an input.

> **It is an asset.**

## Four questions

A useful AI data security model asks:

1. WHO can access the data?
2. WHAT data can they access?
3. WHY can they access it?
4. WHAT happens to the data afterwards?

Consider a RAG system:

**User → retrieval → document context → response**

If retrieval authorization is weak, the LLM may become the final step in a data-leakage path.

The problem is not necessarily that the model “leaked” information. The problem may have occurred earlier:

**User → unauthorized retrieval → document context → response**

This distinction matters.

## Controls

AI data security should include:

- Classification
- Identity and access control
- Encryption in transit and at rest
- Data minimization
- Tenant isolation
- Data lineage
- Retention and deletion
- Audit logging
- Data integrity controls
- Poisoning detection

## Measuring data security

One example is:

> **Data Leakage Rate = Sensitive-data disclosures / relevant test cases × 100**

But leakage is only one dimension.

We should also ask:

- Can the wrong user retrieve the document?
- Can one tenant retrieve another tenant’s embeddings?
- Can training data be modified without detection?
- Can a malicious dataset enter the training pipeline?
- Can sensitive prompts remain in logs indefinitely?

### Key insight

> **AI security starts before the model.**

If the data boundary is broken, model-level controls may be too late.

### Suggested visual

Secure AI data lifecycle from ingestion → storage → training/RAG → inference → logging, showing access-control and encryption checkpoints.
