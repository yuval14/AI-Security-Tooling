# AI SOC Observability and Incident Detection

**Author:** Yuval Sinay  
**Version:** 1.0  
**Year:** 2026

## Workbook

- [Download AI_SOC_Observability_Incident_Detection_v1.0.xlsx](./AI_SOC_Observability_Incident_Detection_v1.0.xlsx)

## Purpose

This workbook helps security operations teams define, assess, and improve observability and incident-detection capabilities for AI systems, generative AI applications, RAG pipelines, model gateways, autonomous agents, tools, and supporting infrastructure.

It connects AI telemetry to measurable SOC outcomes, detection engineering, threat hunting, investigation, evidence collection, and SOAR response.

## Main Components

- **AI SOC Dashboard** - summarizes the overall observability score, assessed metrics, red metrics, trace coverage, and mean time to detect.
- **AI Observability Metrics** - provides measurable targets across logs, operational metrics, distributed traces, detections, and threat hunting.
- **Telemetry Sources** - defines the minimum visibility expected from SIEM, SOAR, model gateways, AI runtimes, API gateways, RAG platforms, agent runtimes, IAM/PAM, EDR/XDR, DLP, proxy, and NDR systems.
- **Trace Model** - maps the required evidence chain from identity and request context through prompts, policy decisions, model execution, retrieval, tool actions, outputs, downstream effects, and SOC correlation.
- **Incident Repository Mapping** - converts external AI incident and vulnerability repositories into SOC use cases, hunts, detections, and response improvements.
- **Incident Detection Use Cases** - documents AI-focused detection scenarios, required events, telemetry, detection logic, investigation steps, severity, and SOAR actions.
- **Detection Response Matrix** - links threats such as prompt injection, data leakage, unauthorized actions, RAG poisoning, model extraction, denial of wallet, telemetry loss, and workload compromise to operational response procedures.

## Intended Users

- SOC analysts and managers
- Detection engineers and threat hunters
- Incident responders and SOAR engineers
- AI security architects
- AI platform, model gateway, and RAG engineering teams
- IAM, DLP, cloud security, EDR/XDR, and data-security teams

## Recommended Use

1. Identify the AI services, identities, models, data stores, agents, tools, and infrastructure in scope.
2. Map available telemetry to the **Telemetry Sources** and **Trace Model** sheets.
3. Enter current values in the metrics assessment and review gaps against the defined targets.
4. Select relevant incident use cases and tailor detection logic to the local architecture.
5. Validate detections through simulation, replay, or authorized red-team testing.
6. Connect approved containment actions to SOAR workflows and human-approval requirements.
7. Review the dashboard regularly and track improvements over time.

## Important Note

The workbook is an assessment and engineering aid. Targets, thresholds, detection logic, and automated responses must be validated against the organization's architecture, risk tolerance, regulatory obligations, and operational safety requirements.

## Responsible Use

Use of materials in this folder is governed by the repository's [Responsible and Protective Use License](../LICENSE). Use is permitted only for lawful, ethical, authorized, defensive, and protective purposes.