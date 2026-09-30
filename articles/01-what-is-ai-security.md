# Article 01: What Actually Is AI Security?

AI security is often reduced to prompt injection, jailbreaks, or model safety.

But a production AI system is much larger than an LLM.

It may include training data, data pipelines, model artifacts, registries, vector stores, APIs, containers, cloud infrastructure, identities, secrets, agents, external tools, storage and edge devices.

That means an attacker does not necessarily need to compromise the model itself.

They could compromise the data.
They could steal a model artifact.
They could abuse an inference API.
They could manipulate a dependency.
They could obtain excessive IAM permissions.
They could poison a vector store.
They could compromise the MLOps pipeline.
Or they could manipulate an agent into taking an action.

## A system-level view

I see AI security as a system-level discipline:

> **AI security = protecting the AI lifecycle + AI-specific assets + the infrastructure that enables them.**

A useful way to think about the attack surface is:

**DATA → MODEL → MLOps → API → APPLICATION → AGENT → INFRASTRUCTURE → STORAGE → RUNTIME**

Every transition is a potential trust boundary.

This is also why frameworks need to be used together rather than treated as interchangeable. OWASP GenAI LLM Top 10 is particularly useful for LLM-powered application risks. MITRE ATLAS provides an adversarial-AI threat knowledge base, while NIST AI RMF provides a broader risk-management structure for AI systems.

## The security question changes

Instead of only asking:

> “Can someone jailbreak my model?”

ask:

> “If one component is compromised, what can the attacker reach, influence or exfiltrate?”

That second question leads toward threat modeling.

## Five starting questions

1. What are the assets?
2. Where are the trust boundaries?
3. What identities and privileges exist?
4. What can an attacker manipulate?
5. What happens if a control fails?

This is where AI security starts becoming engineering rather than a checklist.

The remaining articles break down these layers technically — from AI data and model security to infrastructure, storage, supply chain, APIs, LLMs and agentic systems.

Because securing the LLM while leaving the rest of the AI system exposed is not really securing the AI system.

### Suggested visual

Layered AI security architecture showing Data, Model, MLOps, API, LLM/Agent, Infrastructure, Storage and Edge, with trust boundaries highlighted.
