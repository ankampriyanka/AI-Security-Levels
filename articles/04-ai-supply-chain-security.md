# Article 04: AI Supply-Chain Security: Can We Trust What We Import?

Modern AI systems are assembled from components.

A single application might depend on:

- Foundation models
- Fine-tuned models
- Python packages
- Open-source libraries
- Datasets
- Embedding models
- Docker images
- Plugins
- Connectors
- APIs
- Agent frameworks

Every imported component introduces a trust relationship.

That makes the AI supply chain a security boundary.

## Chain of trust

**Developer → package → container → model → dataset → pipeline → registry → production**

If one component is compromised, the attacker may gain a route into the AI system.

Traditional software security already uses dependency management, SBOMs and artifact integrity.

AI systems extend the problem. We also need:

- Model provenance
- Dataset provenance
- Model lineage
- Fine-tuning lineage
- Training configuration
- Embedding-model origin
- AI-specific dependencies
- Model and artifact signatures

This is why AI BOM thinking is useful.

An AI BOM could connect:

**AI component → version → supplier → dependency → provenance → vulnerability → deployment → owner**

That creates a security inventory rather than a simple asset list.

## A useful control pattern

**IDENTIFY → VERIFY → SIGN → SCAN → AUTHORIZE → MONITOR**

And one example metric is:

> **Supply-Chain Integrity Coverage = AI components with verified provenance / total AI components × 100**

The objective is not to eliminate every external component.

The objective is to make the trust relationships visible and controllable.

> **In AI, “open source” or “pre-trained” does not automatically mean “trusted.” Trust needs evidence.**

### Suggested visual

AI supply-chain chain-of-trust from dataset/model/package/container to registry and production.
