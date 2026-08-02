# OT Network Monitoring Metrics Workbook

**Author:** Yuval Sinay  
**Version:** 1.0  
**Date:** 02.08.2026

## Workbook

- [Download OT_Network_Monitoring_Metrics_Workbook_v1.0.xlsx](./OT_Network_Monitoring_Metrics_Workbook_v1.0.xlsx)

## Purpose

This workbook is a practical reference, assessment aid, monitoring log, and management dashboard for operational technology environments. It helps OT security teams define measurable monitoring requirements, establish approved baselines, identify deviations, prioritize alerts, and communicate operational risk to engineering, SOC, plant, and management stakeholders.

## Main Components

- **START HERE** - explains the workbook structure, recommended users, and operating model.
- **Executive Dashboard** - presents current-state indicators, 30-day trends, critical events, availability, packet loss, telemetry health, and daily risk status.
- **KPI Catalog** - defines monitoring indicators, formulas, data sources, review frequency, green/amber/red thresholds, priority, ownership, immediate response, framework mapping, and measurement units.
- **Daily Monitoring** - provides a 30-day monitoring dataset with formulas for daily risk scoring and status classification.
- **Alert Playbook** - documents priority events, trigger logic, immediate actions, escalation paths, and response guidance.
- **Protocol Coverage** - identifies protocol-specific operations, functions, and anomalies that should be monitored.
- **References** - provides operating assumptions, calibration guidance, the scoring model, and APA 7 references.

## Monitoring Domains

The KPI catalog covers areas such as:

- Asset visibility and inventory accuracy
- Network availability, latency, jitter, packet loss, errors, and redundancy
- New communication pairs, unexpected protocols, traffic deviations, and session failures
- Unauthorized write commands, program downloads, operating-mode changes, and firmware modifications
- Identity, privileged access, remote access, and session compliance
- IT-to-OT segmentation, direct internet connectivity, firewall events, and DMZ bypass
- Endpoint, server, application, process, historian, and telemetry health
- Data integrity, stale or frozen values, alarms, time synchronization, and safety-relevant events

## Intended Users

- OT SOC analysts and managers
- Control and automation engineers
- OT network and security engineers
- Detection engineers and incident responders
- Plant managers, CISOs, and risk owners
- Asset owners and remote-access administrators

## Recommended Use

1. Inventory OT assets, zones, conduits, safety systems, control servers, engineering workstations, and remote-access paths.
2. Select relevant metrics from the **KPI Catalog** and tailor thresholds to each process state and site.
3. Collect passive network telemetry, device logs, authentication events, historian data, and change-management records.
4. Review the **Executive Dashboard** and investigate deviations using the **Alert Playbook**.
5. Revalidate baselines and thresholds after process, topology, firmware, vendor, or operating-mode changes.

## OT Safety Considerations

- Validate thresholds with control engineering, process safety, network engineering, and asset owners.
- Prefer passive monitoring for initial visibility.
- Test and approve active discovery or scanning before use on production control networks.
- Correlate cyber telemetry with process state, alarms, operator logs, maintenance windows, and physical observations.
- Do not automate containment without evaluating process safety, availability, and recovery consequences.

## Reference Frameworks

The workbook is informed by NIST SP 800-82 Rev. 3, ISA/IEC 62443, MITRE ATT&CK for ICS, and NIST OT security guidance.

## Responsible Use

Use of materials in this folder is governed by the repository's [Responsible and Protective Use License](../LICENSE). Use is permitted only for lawful, ethical, authorized, defensive, and protective purposes.