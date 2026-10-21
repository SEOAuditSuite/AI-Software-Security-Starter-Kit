# Security Acceptance Criteria

This document summarizes [Section 9 of the original standard](../toolkit/01_AI_Software_Security_Standard.md); the original file controls in case of ambiguity.

## Evidence contract

Record app/version/commit, architecture and deployed features, approved test environment, applicable controls, test procedure, actual results and evidence. Record **NOT RUN** for unexecuted checks and explain **N/A** when a control is irrelevant. Capture scanner versions, false-positive triage, regression results, risks and limitations.

| Decision | Minimum meaning | What it does not mean |
| --- | --- | --- |
| **PASS — Release Candidate Security Verified** | All mandatory *applicable scoped* checks executed/passed; confirmed blocking issues resolved; regressions passed and residual risks documented | A universal absence-of-vulnerabilities claim or automatic deployment permission |
| **FAIL — Release Blocked** | Blocking security defect or essential test/regression failure remains | The entire system is necessarily unsafe for every possible limited use |
| **INCOMPLETE — Verification Pending** | Essential evidence, authorization, access or validation missing | A PASS, or permission to bypass mandatory checks |

## Approval separations

1. Read-only assessment and planning.
2. Explicit authorization for edits, scanning and active validation, specifying target and constraints.
3. Independent review of execution evidence and risk ownership.
4. Distinct merge, release and deployment approval.

This is a workflow contract; it does not itself execute scans, enforce firewalls or certify software.
