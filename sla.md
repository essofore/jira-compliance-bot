# Service Level Agreement — MedTech Compliance Tracker

**Effective date:** 2026-05-25
**Vendor:** Essofore LLC (support@essofore.com)

---

## 1. Scope

This Service Level Agreement ("SLA") describes the support commitments, availability terms, and limitations that apply to MedTech Compliance Tracker ("the App") for customers who have installed the App from the Atlassian Marketplace.

---

## 2. Infrastructure availability

The App is built on the **Atlassian Forge** platform and runs entirely within Atlassian's managed cloud infrastructure. Accordingly:

- **Uptime and availability** of the underlying runtime, Jira APIs, and Forge platform are governed by Atlassian's Cloud SLA, available at [https://www.atlassian.com/legal/sla](https://www.atlassian.com/legal/sla).
- Essofore does not operate independent servers, databases, or network infrastructure. We cannot guarantee or extend uptime beyond what Atlassian's platform provides.
- Incidents originating from Atlassian infrastructure (outages, degraded performance, Forge platform issues) are outside the scope of this SLA and should be reported via the [Atlassian Status Page](https://status.atlassian.com).

---

## 3. Application-level commitments

Within the constraints of the Forge platform, Essofore commits to the following.

### 3.1 Functional correctness

The App will:

- Create compliance sub-tasks on new Jira issues whose summary or description matches a keyword rule, within the latency bounds of the Forge trigger runtime (typically seconds).
- Skip issues that are already sub-tasks (no recursion).
- Respect per-project enable/disable settings without delay.
- Produce backfill results consistent with the trigger path — the same rules, the same sub-task templates.

### 3.2 Rule accuracy

Compliance rules are maintained to reflect the standards listed in the App description (IEC 62304, ISO 14971, IEC 62366-1, IEC 81001-5-1 / AAMI TIR57, ISO 13485, 21 CFR Part 820, MDR 2017/745, HIPAA, GDPR). When a covered standard is revised and the revision materially affects the rule set, an update will be released within **90 days** of the effective date of the revision.

### 3.3 Compatibility

The App will remain compatible with Jira Cloud and the Atlassian Forge platform. If Atlassian introduces a breaking change to the Forge runtime or Jira APIs, a remediation release will be targeted within **14 calendar days** of general availability of the breaking change.

---

## 4. Support

| Tier | Criteria | Initial response target |
|------|----------|------------------------|
| **P1 — Critical** | App creates incorrect sub-tasks, creates sub-tasks on the wrong issues, or fails silently on all new issues | 1 business day |
| **P2 — High** | App fails on a subset of issues or a specific project; backfill does not complete | 2 business days |
| **P3 — Normal** | Incorrect keyword matches, missing rule coverage, UI issues, feature requests | 5 business days |

**Business hours:** Monday–Friday, 09:00–18:00 US Pacific Time, excluding US federal holidays.

**Support channel:** support@essofore.com. Include your Jira site URL, project key, and a description of the affected issue(s).

Response targets are acknowledgment windows, not resolution windows. Resolution time depends on root-cause complexity and, for Forge platform issues, on Atlassian's remediation timeline.

---

## 5. Exclusions

This SLA does not apply to:

- Downtime or degraded performance caused by Atlassian Forge, Jira Cloud, or Atlassian's CDN/network infrastructure.
- Issues arising from customer-side Jira configuration (workflow schemes, permission schemes, issue type schemes) that prevent sub-task creation.
- Regulatory interpretation or legal compliance advice. The App surfaces obligations derived from publicly available standards; it does not constitute legal counsel.
- Issues in App versions that have been superseded by a newer release for more than 30 days.
- Free-tier or trial installations where no paid license is active.

---

## 6. Planned maintenance

Because the App runs on Atlassian Forge, it has no independent maintenance windows. App updates are deployed as Forge function deployments and take effect within minutes with no service interruption to active Jira users. Changes to app manifest (new scopes or modules) require a brief Forge install step that does not affect existing data.

---

## 7. Incident reporting

For suspected App-level defects, email support@essofore.com with subject line `[INCIDENT] <brief description>`.

For suspected Atlassian platform issues, check [https://status.atlassian.com](https://status.atlassian.com) first. If the issue is confirmed to be platform-side, Essofore will track the Atlassian incident and notify affected customers once resolved.

---

## 8. Scope limitations

The App is a **compliance workflow aid**, not a substitute for regulatory counsel. It does not guarantee regulatory approval, audit readiness, or conformance to any standard. The customer remains solely responsible for verifying that generated sub-tasks satisfy their specific regulatory obligations. The app is provided on an as-is basis, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied, including, without limitation, any warranties or conditions of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A PARTICULAR PURPOSE. 

---

## 9. SLA revisions

Essofore may revise this SLA with 30 days' notice posted to the Marketplace listing or sent to the primary account contact. Continued use of the App after the effective date constitutes acceptance of the revised terms.

---

## 10. Contact

| Purpose | Contact |
|---------|---------|
| Support requests | support@essofore.com |
| Billing and licensing | support@essofore.com |
| Security disclosures | support@essofore.com |
| Atlassian platform issues | [https://status.atlassian.com](https://status.atlassian.com) |
