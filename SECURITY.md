# Security Policy — MedTech Compliance Tracker

**Effective date:** 2026-05-19

## Reporting a vulnerability

If you discover a security vulnerability in this app, please report it by email to **support@essofore.com** with the subject line **"Security vulnerability report — MedTech Compliance Tracker"**.

Please include:
- A description of the vulnerability and its potential impact
- Steps to reproduce or a proof-of-concept
- The version of the app where you observed the issue (visible on the Atlassian Marketplace listing)

We will acknowledge your report within **3 business days** and aim to provide a resolution or remediation plan within **14 business days**. We ask that you practice responsible disclosure and give us the opportunity to address the issue before making it public.

## Security architecture

MedTech Compliance Tracker is built on **Atlassian Forge**, Atlassian's serverless app platform. This has the following security implications:

- **No external infrastructure.** The app has no servers, databases, or cloud accounts of its own. All code executes inside Atlassian's Forge sandbox.
- **No data leaves Atlassian's platform.** The app reads Jira issue fields (summary, description, issue type, project key) in-memory to perform keyword matching. No data is transmitted to third-party services or external APIs.
- **No personal data stored.** Forge Storage is used only for project-enable flags and backfill progress counters — no personal or user-identifiable information is persisted.
- **No credential handling.** The app uses Forge's built-in authentication (`asUser()` / `asApp()`). End users are never asked to provide passwords, Personal Access Tokens, or any other credentials to the app.
- **Atlassian governs the runtime.** Atlassian is responsible for the security of the Forge platform itself, including sandboxing, network isolation, and infrastructure hardening. See [Atlassian's Trust & Security page](https://www.atlassian.com/trust) for details.

## Scope

The following are **in scope** for vulnerability reports:

- Logic bugs that could cause the app to create subtasks in unintended projects
- Privilege escalation — the app acting with more permissions than a user should grant it
- Information disclosure — the app surfacing issue content to users who should not see it

The following are **out of scope** (governed by Atlassian's own security program):

- Vulnerabilities in the Forge runtime, Atlassian APIs, or Jira itself
- Denial-of-service attacks against Atlassian infrastructure

## Authentication and authorization

The app acts as a Forge app bot (service account) using permissions granted at installation time by a Jira administrator — it does not inherit or act on behalf of the user who created the issue. Two controls gate subtask creation:

1. **Install-time grant:** a Jira administrator must install the app, which grants it the `write:jira-work` scope across the instance.
2. **Per-project toggle:** administrators can enable or disable the app on a per-project basis via the app's project settings page; disabled projects are skipped entirely.

## Dependency security

The app's runtime dependencies are limited to Atlassian's own Forge packages (`@forge/api`, `@forge/events`, `@forge/resolver`, `@forge/react`, `@forge/bridge`). No third-party npm packages are used in production code, eliminating supply-chain risk from external dependencies.

## Contact

For security issues: **support@essofore.com**
For general support and privacy questions: **support@essofore.com**
Privacy policy: https://github.com/essofore/jira-compliance-bot/blob/main/privacy-policy.md
