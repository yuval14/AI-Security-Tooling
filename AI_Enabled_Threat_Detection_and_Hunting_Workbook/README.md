# AI-Enabled Threat Detection and Hunting Workbook

**Author:** Yuval Sinay  
**Version:** 1.0  
**Date:** 2026-08-05

## Workbook

- [Download the Excel workbook](./AI_Enabled_Threat_Detection_and_Hunting_Workbook_v1.0.xlsx)

## Purpose

This workbook supports defensive detection engineering and threat hunting for covert or operational use of artificial intelligence during cyberattacks.

It is designed for situations in which an adversary may use a commercial model, a local model, an AI coding assistant, an autonomous agent, an AI API, or AI-enabled infrastructure as part of reconnaissance, execution, credential access, persistence, lateral movement, command and control, collection, or exfiltration.

The workbook does not treat speed, sophistication, generated text, or generated code as proof of adversarial AI use. It prioritizes correlated technical evidence across identity, endpoint, network, cloud, AI-service, development, and data-security telemetry.

## Intended Users

- Chief Information Security Officers
- SOC managers and analysts
- Detection engineers
- Threat hunters
- DFIR and incident-response teams
- Cloud and identity security teams
- AI security architects
- Security researchers

## Main Components

### Executive Dashboard

Summarizes scenario counts, critical and high-priority items, implementation status, hunt activity, and estimated coverage.

### Detection Catalog

Provides fourteen detection and hunting scenarios with:

- Detection logic
- Threat hypothesis
- Primary and secondary data sources
- Key entities
- Detection windows
- Likelihood and impact scoring
- Calculated risk score and priority
- Suggested severity
- MITRE ATT&CK tactics
- Likely false positives
- Tuning guidance
- Initial response actions
- Ownership, coverage, confidence, and testing fields

### Hunt Worksheet

Provides a repeatable structure for documenting:

- Hunt scope and hypothesis
- Time period and environment
- Queries and tools used
- Systems reviewed
- Findings and evidence
- Outcome and escalation
- Case identifiers
- Follow-up actions and lessons learned

### Telemetry Matrix

Maps each scenario to required, recommended, optional, or non-applicable telemetry across:

- EDR and process events
- File and registry monitoring
- DNS and proxy
- Network and TLS
- AI gateway and model APIs
- Cloud and IAM
- Git and CI/CD
- DLP and CASB
- GPU and ML runtimes
- SaaS and Backend-as-a-Service
- Email and web security

## Detection and Hunting Scenarios

1. Unexpected process calls an LLM.
2. AI response followed by code execution.
3. Runtime compilation outside development environments.
4. AI agent or CLI accesses secrets.
5. AI share link followed by shell execution.
6. New-domain BaaS credential collection.
7. Unusual AI traffic from a server.
8. Self-modification after model interaction.
9. Abnormal GPU or local inference activity.
10. Multi-provider AI usage in a short sequence.
11. Service account performs agentic actions.
12. Excessive dead or AI-generated decoy code.
13. Lateral movement after agent activity.
14. Frequent API-key rotation or pooling.

## Scoring Method

The workbook calculates:

```text
Risk Score = Likelihood × Impact
```

Suggested interpretation:

| Risk score | Priority |
|---:|---|
| 20-25 | Critical |
| 15-19 | High |
| 8-14 | Medium |
| 1-7 | Low |

The values are starting points and should be adjusted to the organization's threat model, exposure, controls, sector, and operational consequences.

## Recommended Use

1. Inventory approved AI providers, local models, agents, coding assistants, service identities, model gateways, and AI API keys.
2. Identify which scenarios are relevant to the organization's architecture and threat model.
3. Validate whether the required telemetry exists and is retained for a sufficient period.
4. Assign scenario owners and implementation status.
5. Adapt the detection logic to local schemas and approved use cases.
6. Test each analytic against benign developer, administrator, security-testing, and automation activity.
7. Execute documented hunts and preserve both successful and failed adversary actions.
8. Review high-risk scenarios after major changes to models, agents, tools, permissions, infrastructure, or threat intelligence.

## Analytic Guardrail

No individual signal independently proves that an attacker used AI. A process connecting to a model API, runtime compilation, GPU use, or AI-assisted development can be legitimate.

Priority should be given to correlated sequences such as:

```text
Unexpected process -> model interaction -> generated file -> compilation -> child process -> sensitive-data access -> outbound communication
```

## Related Resources

- [Cybersecurity Detection Engineering](https://github.com/yuval14/Cybersecurity-Detection-Engineering)
- [AIDAF - Adversarial AI Detection and Assessment Framework](https://github.com/yuval14/Cybersecurity-Detection-Engineering/tree/main/AIDAF-Adversarial-AI-Detection-and-Assessment-Framework)
- [Artificial Intelligence Cyber Shield](https://github.com/yuval14/Artificial-Intelligence-Cyber-Shield)

## Important Note

This workbook is a defensive planning, assessment, detection-engineering, and threat-hunting aid. Detection logic must be validated against the organization's architecture, legal and privacy obligations, approved AI usage, operational-safety requirements, and incident-response procedures.

## Responsible Use

Use of this workbook is governed by the repository's [Responsible and Protective Use License](../LICENSE). It is intended only for lawful, ethical, authorized, defensive, and protective purposes.