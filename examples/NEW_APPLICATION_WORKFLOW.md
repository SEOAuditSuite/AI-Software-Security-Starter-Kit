# Example: Secure a New Application from Day One

**Illustrative workflow only; no application was built or tested.**

1. Attach [the complete standard](../toolkit/01_AI_Software_Security_Standard.md) and use prompt **A. NEW SOFTWARE** from [AI instructions](../toolkit/02_AI_Instructions.txt).
2. Provide app idea, deployment/exposure, assets, roles, trust boundaries, dependencies and external-service needs.
3. Request a threat model and control matrix: risk, relevant component, mitigation, evidence expected, approval owner.
4. Review design before implementation; keep credentials in approved secret stores, enforce server-side authorization and resource limits, and use approved dependencies.
5. Approve a narrowly scoped implementation and a separate testing plan. No unapproved payments, deployments or attacks.
6. Generate synthetic fixtures and run applicable scanners/tests only after authorization. Record actual versions and outputs.
7. Apply Section 9 release gate and obtain separate deployment sign-off.

**Example test-row template:** `Broken object authorization | /api/orders/{id} | User B must not read User A's order | two synthetic users | NOT RUN | evidence pending`.
