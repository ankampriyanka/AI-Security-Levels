# Article 15: AI Security Monitoring: If You Cannot Observe It, You Cannot Investigate It

Preventive controls are important.

But no security architecture should assume that prevention will always work.

AI systems need detection and response too.

The challenge is that conventional logs may not capture enough context.

For an AI security investigation, we may need to know:

- Who made the request?
- Which model version responded?
- Which documents were retrieved?
- Which tools were called?
- Which parameters were passed?
- Which policy decisions occurred?
- Which identity executed the action?
- What data crossed the boundary?
- What changed?

## An auditable AI security event

**User → Request → Retrieval → Context → Model → Tool proposal → Policy decision → Tool execution → Result → Final response**

This creates an auditable chain.

Security monitoring can then look for patterns such as:

- Repeated injection attempts
- Abnormal retrieval
- Cross-tenant access
- Excessive tool calls
- Unusual token consumption
- Model extraction patterns
- Repeated authorization failures
- Unexpected model/version changes

Useful metrics include:

- Attack Detection Rate
- False Positive Rate
- Mean Time to Detect
- Mean Time to Contain
- Unauthorized Action Rate
- Security Event Coverage

The final objective is not simply more logs.

> **It is evidence.**

Can the security team reconstruct what happened?

Can they identify the affected asset?

Can they determine which control failed?

Can they contain the incident?

Can they prove recovery?

AI security operations should therefore connect technical telemetry to incident response and governance evidence.

Security is not complete when we deploy controls.

It is complete when we can also detect, investigate and respond to failure.

### Suggested visual

AI SOC telemetry pipeline from user/request through retrieval, model, tool execution, policy events and SIEM/incident response.
