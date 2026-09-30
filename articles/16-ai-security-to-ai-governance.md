# Article 16: From AI Security to AI Governance: Turning Controls Into Evidence

After working through AI data, models, supply chains, infrastructure, storage, APIs, LLMs and agents, one question remains:

> **How do we govern all of this?**

A security control that exists only in a document is not enough.

We need to know:

- What is the risk?
- Who owns it?
- What control addresses it?
- How is the control tested?
- What metric demonstrates effectiveness?
- What evidence is retained?
- What happens when the control fails?

## The traceability chain

**RISK → THREAT → ATTACK → CONTROL → METRIC → EVIDENCE → OWNER → REVIEW**

### Example

**Risk:** Unauthorized agent action.

**Threat:** Prompt injection causes malicious tool selection.

**Control:** Tool allowlist + authorization + human approval.

**Metric:** Unauthorized Action Rate.

**Evidence:** Policy decision logs + approval records + test results.

**Owner:** AI product/security owner.

**Review:** Periodic control validation.

This is where frameworks such as NIST AI RMF become useful. NIST describes AI RMF as a voluntary framework for managing AI risks and improving trustworthiness across the design, development, deployment and use of AI systems. Its four functions are Govern, Map, Measure and Manage.

The same security architecture can therefore become part of an AI governance operating model.

The goal is not to create another giant checklist.

The goal is to create traceability:

**AI asset → risk → control → test → metric → evidence**

That is also where an AI BOM can become valuable.

An AI BOM should not only tell us what components exist.

It can become a bridge between:

**AI inventory → dependencies → vulnerabilities → risks → controls → ownership → evidence**

## The larger lesson

> **Responsible AI needs security.**
>
> **Security needs engineering.**
>
> **Engineering needs evidence.**
>
> **And governance is what connects all three.**

That is how we move from “AI security awareness” to an AI system that can actually be assessed, monitored and improved.

### Suggested visual

AI governance control loop linking asset, risk, threat, control, metric, evidence, owner and review.
