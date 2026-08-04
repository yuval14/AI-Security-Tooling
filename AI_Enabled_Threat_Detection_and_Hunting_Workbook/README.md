# AI-Enabled Threat Detection and Hunting Workbook

**Author:** Yuval Sinay  
**Version:** 1.0  
**Date:** 2026-08-05

## Workbook

- [Download AI_Enabled_Threat_Detection_and_Hunting_Workbook_v1.0.xlsx](./AI_Enabled_Threat_Detection_and_Hunting_Workbook_v1.0.xlsx)

## Purpose

This workbook provides a structured defensive aid for identifying, prioritizing, testing, and documenting detections and threat hunts related to covert or operational use of artificial intelligence during cyberattacks.

It focuses on observable workflows rather than attempting to identify AI involvement from writing style, code style, speed, or sophistication alone. It connects AI-service and agent activity with endpoint, network, identity, cloud, development, data, GPU, and SaaS telemetry.

## Intended Users

- Chief Information Security Officers
- SOC managers and analysts
- Detection engineers
- Threat hunters
- Digital forensics and incident-response teams
- Cloud and identity security teams
- AI security architects
- AI platform and model-gateway teams

## Workbook Sheets

### Detection Catalog

Documents fourteen detection and hunting scenarios with detection logic, primary telemetry, MITRE ATT&CK tactics, severity, likelihood, impact, calculated risk score, status, owner, and notes.

### Hunt Worksheet

Provides a repeatable structure for recording hunt scope, dates, analyst, environment, status, outcome, systems reviewed, queries, tools, findings, evidence, and next actions.

### Telemetry Matrix

Maps every scenario to required, recommended, or optional visibility across EDR, DNS and proxy, AI gateway, cloud and IAM, Git and CI/CD, DLP and CASB, GPU and ML runtime, SaaS and Backend-as-a-Service, email, and web telemetry.

### README

Provides workbook metadata, purpose, use guidance, and the core analytic guardrail.

## Detection and Hunting Scenarios

1. Unexpected process calls an LLM.
2. AI response followed by code execution.
3. Runtime compilation outside development environments.
4. AI agent or CLI accesses secrets.
5. AI share link followed by shell execution.
6. New-domain Backend-as-a-Service credential collection.
7. Unusual AI traffic from a server.
8. Self-modification after model interaction.
9. Abnormal GPU or local inference activity.
10. Multi-provider AI usage in a short sequence.
11. Service account performs agentic actions.
12. Excessive dead or AI-generated decoy code.
13. Lateral movement after agent activity.
14. Frequent API-key rotation or pooling.

## Scoring Model

```text
Risk Score = Likelihood × Impact
```

Likelihood and impact are scored from 1 to 5.

| Risk score | Priority |
|---:|---|
| 20-25 | Critical |
| 15-19 | High |
| 8-14 | Medium |
| 1-7 | Low |

## Recommended Use

1. Identify approved AI services, agents, local models, APIs, gateways, identities, tools, and development environments.
2. Review the detection catalog and adjust likelihood, impact, severity, ownership, status, and notes.
3. Use the telemetry matrix to identify collection and correlation gaps.
4. Prioritize critical and high-risk scenarios for engineering and testing.
5. Execute hunts using the Hunt Worksheet and retain supporting evidence.
6. Validate analytics against benign AI use, conventional automation, authorized security testing, and non-AI alternative explanations.
7. Review the workbook after material changes to models, agents, permissions, infrastructure, suppliers, or threat intelligence.

## Analytic Guardrail

No individual signal proves that an adversary used AI. A model endpoint connection, compiler execution, GPU process, coding agent, or service-account action may be legitimate. Findings should be based on correlated telemetry, complete timelines, direct artifacts where available, and explicit consideration of conventional alternatives.

## Important Note

This workbook is a defensive planning, assessment, detection-engineering, and threat-hunting aid. It does not replace organization-specific architecture reviews, risk assessments, legal and privacy analysis, incident-response procedures, vendor guidance, or production validation.

## Responsible Use

Use of this workbook is governed by the repository's [Responsible and Protective Use License](../LICENSE). Use is permitted only for lawful, ethical, authorized, defensive, and protective purposes.