# AI Use by Office Employees: Threats and Defensive Responses

## 1. Assessment Objective

Evaluate how employee use of AI may affect confidentiality, integrity, availability, privacy, legal compliance, intellectual property, decision quality, and organizational trust.

## 2. Scoring Method

Score each threat using the following scales:

### Likelihood

| Score | Description |
|---:|---|
| 1 | Rare |
| 2 | Unlikely |
| 3 | Possible |
| 4 | Likely |
| 5 | Almost certain |

### Impact

| Score | Description |
|---:|---|
| 1 | Negligible |
| 2 | Minor |
| 3 | Moderate |
| 4 | Major |
| 5 | Severe |

### Control Effectiveness

| Score | Description |
|---:|---|
| 0 | No effective control |
| 1 | Ad hoc or weak |
| 2 | Partially implemented |
| 3 | Implemented and generally effective |
| 4 | Measured, tested, and continuously improved |

### Priority Calculation

- **Inherent Risk = Likelihood × Impact**
- **Residual Priority = Inherent Risk × (1 − Control Effectiveness ÷ 4)**

Escalate any scenario that creates a legal, privacy, safety, national-security, or mission-critical concern regardless of the numerical result.

## 3. Threat and Defensive Response Catalogue

| ID | Threat Scenario | Typical Consequence | Preventive Responses | Detective and Corrective Responses |
|---|---|---|---|---|
| T01 | Employees use unapproved AI services | Shadow AI, unmanaged data processing, unknown supplier exposure | Approved-service catalogue; acceptable-use policy; procurement path; technical blocking where justified | Discover AI domains and extensions; review SaaS usage; contact users; migrate legitimate use cases |
| T02 | Sensitive information is entered into prompts | Confidentiality breach, privacy violation, contractual exposure | Data-classification rules; prompt restrictions; enterprise accounts; data-loss prevention; user training | DLP alerts; audit logs; incident triage; supplier deletion request where available |
| T03 | Credentials, tokens, or secrets are exposed | Account compromise and lateral movement | Secret-management tools; prohibit secrets in prompts; masking; secure development guidance | Secret scanning; token revocation; credential rotation; access review |
| T04 | AI output contains false or fabricated information | Incorrect decisions, reputational harm, operational error | Human verification; source requirements; approved use cases; confidence and limitation notices | Quality sampling; error reporting; correction workflow; update training and procedures |
| T05 | AI-generated content is treated as authoritative | Automation bias and loss of professional judgment | Decision-rights matrix; mandatory human approval; segregation of duties | Review high-impact decisions; audit exceptions; investigate repeated overreliance |
| T06 | Prompt injection is delivered through documents, email, or websites | Instruction hijacking, data leakage, unsafe tool use | Treat external content as untrusted; isolate retrieval; restrict tools and permissions; content filtering | Monitor abnormal agent actions; inspect prompts and tool calls; revoke sessions; contain affected workflows |
| T07 | AI-generated code, formulas, scripts, or macros are unsafe | Vulnerabilities, malware execution, data corruption | Secure review; sandboxing; software composition analysis; prohibit direct production execution | Endpoint alerts; code scanning; rollback; incident response; lessons learned |
| T08 | AI plugins, connectors, or agents receive excessive permissions | Unauthorized access or unintended action | Least privilege; scoped OAuth; separate service identities; approval for high-risk actions | Permission reviews; anomalous access monitoring; revoke unused grants; investigate unexpected actions |
| T09 | Supplier retains prompts or uses them for model improvement | Loss of control over organizational information | Contract review; enterprise privacy settings; retention limits; opt-out settings; approved vendors | Periodic supplier assurance; verify settings; deletion requests; reassess supplier risk |
| T10 | AI output infringes copyright or misuses intellectual property | Legal claims, licensing violations, loss of proprietary rights | IP guidance; provenance checks; approved content sources; legal review for publication | Takedown process; content review; evidence preservation; remedial licensing or replacement |
| T11 | AI-generated messages enable phishing or impersonation | Fraud, social engineering, reputational damage | Phishing-resistant MFA; payment verification; out-of-band confirmation; employee awareness | Email authentication monitoring; fraud detection; rapid account containment; notify affected parties |
| T12 | Employees upload malicious or sensitive files to AI services | Malware exposure or external disclosure | File-type restrictions; malware scanning; approved upload channels; data handling rules | Upload logs; sandbox alerts; incident investigation; remove shared files and rotate exposed secrets |
| T13 | AI produces biased, discriminatory, or inappropriate content | Unfair decisions, employee harm, legal and reputational risk | Prohibit unsupported high-impact decisions; diverse review; evaluation criteria; accessibility review | Complaint channel; outcome monitoring; corrective review; suspend unsafe use cases |
| T14 | AI-generated summaries omit critical context | Poor decisions, missed obligations, incomplete records | Require access to originals; defined validation checks; use templates for critical summaries | Compare samples with source material; correct records; adjust workflows and prompts |
| T15 | AI use creates inaccurate or incomplete business records | Audit, regulatory, and evidentiary weaknesses | Records-management rules; identify AI-generated content; retention requirements | Record-quality audits; remediation; preserve relevant prompts and outputs where lawful |
| T16 | Personal data is processed without a lawful basis or adequate notice | Privacy breach, regulatory exposure, employee distrust | Privacy impact assessment; minimization; purpose limitation; approved processing conditions | Privacy monitoring; data-subject request process; breach assessment and notification |
| T17 | AI features are enabled by default in productivity platforms | Unreviewed processing and rapid scope expansion | Configuration baselines; change control; tenant-level governance; staged rollout | Configuration monitoring; periodic tenant review; disable unsafe features; document exceptions |
| T18 | Browser extensions or local AI applications capture content | Session theft, data leakage, hidden monitoring | Extension allowlist; application control; endpoint hardening; managed browsers | Endpoint detection; extension inventory; remove unauthorized software; investigate accessed data |
| T19 | AI agents act without adequate transaction boundaries | Unintended messages, purchases, deletions, or workflow changes | Read-only default; transaction limits; confirmation before execution; reversible actions; separation of proposal and execution | Tool-call logging; alert on high-impact actions; rollback; disable agent credentials |
| T20 | Logging is insufficient to reconstruct AI-assisted activity | Weak accountability and incident investigation | Central audit requirements; identity binding; prompt and action metadata where proportionate and lawful | Log-health monitoring; gap reporting; reconstruct events from endpoint, identity, and SaaS records |

## 4. Minimum Organizational Baseline

An organization should, at minimum, establish:

1. An approved AI service catalogue and exception process.
2. Clear rules for confidential, personal, regulated, and classified information.
3. Enterprise identity, access control, and auditable accounts for approved services.
4. Human review for consequential decisions and external publication.
5. Governance for plugins, connectors, agents, and automated actions.
6. Technical monitoring for shadow AI, data leakage, malicious extensions, and abnormal access.
7. Incident response procedures that explicitly include AI-related events.
8. Periodic supplier, privacy, legal, and security review.
9. Role-specific employee training with practical examples.
10. Metrics for adoption, exceptions, incidents, control coverage, and remediation.

## 5. Assessment Record

For each threat, record:

- Business unit and process
- AI service or feature
- Data classification
- Likelihood and impact
- Existing controls and evidence
- Control effectiveness
- Residual priority
- Gap description
- Required action
- Action owner
- Target date
- Review status

## 6. Suggested Decision Categories

| Decision | Meaning |
|---|---|
| Allow | Risk is within tolerance and required controls are operating |
| Allow with conditions | Use is permitted only after specified controls or limitations are applied |
| Pilot | Use is restricted to a controlled test with monitoring and defined exit criteria |
| Escalate | Legal, privacy, security, safety, or executive review is required |
| Prohibit | Risk cannot be reduced to an acceptable level |
