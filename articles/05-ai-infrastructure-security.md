# Article 05: Securing AI Infrastructure: The LLM Is Not the Infrastructure

An AI model can be perfectly protected while the infrastructure hosting it remains exposed.

Consider a typical deployment:

**Internet → API Gateway → Authentication → AI Service → Kubernetes → GPU Node → Model Runtime → Data Store**

Every layer has its own security requirements.

## Infrastructure security includes

- IAM
- RBAC
- Network segmentation
- Secrets management
- Container security
- Kubernetes security
- Host security
- GPU isolation
- TLS
- Firewalls
- Runtime monitoring
- Workload isolation

The AI-specific question is not simply:

> “Is the server secure?”

It is:

> “What can the AI workload reach?”

Suppose an inference service is compromised.

Can it access the model registry? Training data? Another tenant? Cloud credentials? Internal databases? Administrative APIs?

This is where least privilege and segmentation become critical.

## A useful architecture

**Internet → WAF/API Gateway → Authentication → Authorization → AI Service → Restricted Network Zone → Model Runtime → Explicitly authorized data/services**

The principle is simple:

> **Compromise one workload. Contain the blast radius.**

We should therefore ask not only whether an attack succeeds, but:

> “How far can the attacker move after success?”

That is a blast-radius question.

### Suggested visual

Zero-trust AI infrastructure architecture with WAF, IAM, Kubernetes, GPU runtime, network zones and explicit service permissions.
