# Clinical-Support Workspace: QA, Privacy, and Safety Guide

Aegis is a clinical-support workspace concept. This repository is a software project, not evidence of clinical validation. Verify the actual modules, user roles, and data flows before describing them as implemented.

## Setup

```bash
git clone https://github.com/kandisaikishore/Aegis-Clinical-Bipolar-Workspace.git
cd Aegis-Clinical-Bipolar-Workspace
```

Use the runtime and scripts declared by the repository's manifests. Configure any credentials locally and never commit real patient records, sensitive notes, or API keys.

## Privacy and access-control testing

For implemented records and workflows, test:
- Consent and permission checks for reading, editing, exporting, and deleting records
- Attempts to access another user's or role's records by changing identifiers
- Session expiry and authorization failures
- Export contents and deletion behavior for related stored/derived data
- Partial failure during save/delete and recovery
- Sensitive text redaction from application logs

Use synthetic fixtures only. Keep audit records minimal and access-controlled; never include passwords, tokens, or unnecessary sensitive details.

## Safety and clinical boundaries

- Do not describe the application as diagnosing, treating, or replacing a clinician.
- Label generated or illustrative content clearly and avoid unsupported clinical claims.
- If crisis-resource information is implemented, verify its accuracy for the intended deployment region.
- Document human review and escalation boundaries; do not imply a human clinician has been contacted unless that action occurred.
- Do not claim regulatory compliance or clinical effectiveness without formal evidence.

## Pull-request checklist

- [ ] Add tests for authorized and denied access.
- [ ] Verify privacy-sensitive data is not exposed in logs or exports.
- [ ] Run declared test/build checks and record results.
- [ ] State any checks that could not be run.
- [ ] Keep product limitations and clinical disclaimers visible.
