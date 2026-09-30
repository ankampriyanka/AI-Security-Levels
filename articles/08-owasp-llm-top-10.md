# Article 08: OWASP LLM Top 10: One Layer of the AI Security Stack

When someone says “AI security,” one of the first things we often hear is:

> “Let's check the OWASP LLM Top 10.”

That is useful.

But it is not the entire AI security architecture.

The 2026 OWASP GenAI LLM Top 10 is specifically focused on critical security risks facing applications powered by large language models.

That makes it highly relevant — but also defines its boundary.

The broader AI system may still include:

**DATA · MODEL · MLOps · SUPPLY CHAIN · API · VECTOR STORE · CLOUD · STORAGE · RUNTIME · EDGE**

OWASP LLM security sits primarily around the LLM/application interaction layer.

## Risks in this layer

- Prompt injection
- Sensitive information disclosure
- Excessive agency
- Supply-chain risks
- Data/model poisoning
- Unbounded consumption
- Misinformation
- Hidden context exposure
- Vector and embedding weaknesses
- Improper output handling

The important architectural insight is:

> **OWASP LLM Top 10 ≠ complete AI security.**

Instead:

**AI Security → LLM/Application Security → OWASP GenAI LLM Top 10**

Alongside it, we need other perspectives. MITRE ATLAS helps describe adversarial AI tactics and techniques. NIST AI RMF provides a broader AI risk-management structure. Other security frameworks remain relevant for APIs, cloud, software supply chains and infrastructure.

Use frameworks as lenses.

Do not make one framework the entire system.

### Suggested visual

AI security stack with OWASP LLM Top 10 highlighted as one application layer among data, model, supply chain, infrastructure and runtime.
