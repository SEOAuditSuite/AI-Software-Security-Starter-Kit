# Example: Read-Only Assessment of an Existing Application

**Illustrative workflow only; no audit was executed by this package.**

1. Supply the real repository, branch/commit, stack, environment and available tests. Attach the [security standard](../toolkit/01_AI_Software_Security_Standard.md) and select prompt **B. EXISTING SOFTWARE**.
2. Request a read-only inventory of endpoints, data flows, secrets handling, trust boundaries and security controls.
3. Separate `CONFIRMED`, `SUSPECTED`, `NOT TESTED` and `N/A`; do not infer vulnerabilities from generic checklists.
4. Prepare risk-specific cases: authorization, SSRF, process isolation, report escaping, CI permissions or payments *only where relevant*.
5. Obtain approval for target/environment and test execution; use synthetic data. Record real evidence, tool versions and exceptions.
6. If issues are confirmed, propose the smallest patch, expected side effects, focused regression tests and a rollback plan **before editing**.
7. Require independently reviewed evidence and an explicit PASS/FAIL/INCOMPLETE decision; keep deployment approval separate.

For the SEO Audit Suite example in the original standard, validate the **actual current commit** rather than copying acceptance claims from previous versions.
