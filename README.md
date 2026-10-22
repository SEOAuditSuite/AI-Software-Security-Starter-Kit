# AI Software Security Starter Kit

**Version 1.1 · Security workflow and governance toolkit · Public repository**

Reusable security standards, AI coding instructions, verification workflows, and evidence-based release gates for AI-assisted software development.

> **Not a security scanner or certification.** These are instructions and review templates, not executable controls. Adding the toolkit to a chat, IDE, or project does not automatically inspect code, run tests, block attacks, or make an application secure. Results depend on authorized access, appropriate tools, independent evidence, and human review.

## Why this exists

AI coding tools can accelerate delivery while overlooking threat models, permissions, unsafe external requests, secrets, or failed deployment gates. This toolkit helps developers and operators request explicit security reviews, plan test evidence, and distinguish completed checks from assumptions.

## What is included

| Resource | Intended use |
| --- | --- |
| [Security standard](toolkit/01_AI_Software_Security_Standard.md) | Threat modeling, implementation guidance, and Section 9 release gates |
| [AI instructions](toolkit/02_AI_Instructions.txt) | Copy/paste prompts for new software, existing applications, projects, and handoffs |
| [Security test instructions](toolkit/03_SECURITY_TEST_INSTRUCTIONS.txt) | Read-only-first test planning, authorized execution, and evidence reports |
| [Beginner guide (Roman Urdu)](toolkit/README_START_HERE.txt) | Practical introduction from the original v1.1 archive |
| [New application example](examples/NEW_APPLICATION_WORKFLOW.md) | Apply the standard before building a new product |
| [Existing application example](examples/EXISTING_APPLICATION_AUDIT.md) | Baseline assessment before altering code |
| [Release checklist](examples/SECURITY_RELEASE_CHECKLIST.md) | Reusable approval and evidence table |
| [Acceptance criteria](docs/SECURITY_ACCEPTANCE_CRITERIA.md) | Meaning of PASS, FAIL, INCOMPLETE and N/A |
| [Compatibility guidance](docs/TOOL_COMPATIBILITY.md) | How to use files with chat and coding tools |
| [References](docs/REFERENCES.md) | Starting points for official security guidance |

The four files under `toolkit/` are **unchanged originals**. See [source preservation manifest](docs/SOURCE_MANIFEST.json).

## Quick start

1. Open the [security standard](toolkit/01_AI_Software_Security_Standard.md) and provide its **complete contents** to your AI assistant or make the file accessible to the agent.
2. Open [AI instructions](toolkit/02_AI_Instructions.txt) and select **A. NEW SOFTWARE**, **B. EXISTING SOFTWARE**, or **C. CHATGPT PROJECT** as appropriate.
3. Supply the actual app/repository, version, environment and desired scope. Ask the AI to confirm it **can access** the standard; a filename alone is not access.
4. Start with a **read-only baseline and risk matrix**. Approve changes and active testing separately.
5. Use the [test instructions](toolkit/03_SECURITY_TEST_INSTRUCTIONS.txt) after scoping and authorization. Record **actual tools run, evidence, skips, limits and regressions**.
6. Require a separate human decision before merging, deploying or publishing.

### ChatGPT chat and Projects
Attach the standard in the same chat; for a Project, add it as a Project source and verify retrieval. Use the corresponding prompt in `02_AI_Instructions.txt`. ChatGPT Work may inspect repositories/files and execute supported multi-step checks when properly connected and authorized; **do not assume** it has local-device or production access.

### Claude, Claude Code, Cursor and other assistants
Give the assistant the full standard through its supported attachment, project instruction or repository context. Use the relevant prompt, then verify it genuinely read the file and can access the current code. Agent features, tool access and security controls vary by product and configuration; confirm the effective permissions before testing or editing.

### Existing software versus new applications
For **existing** apps, freeze the actual baseline, inspect architecture and tests, classify proven versus suspected issues, then propose minimally scoped fixes and regression coverage. For **new** apps, define users, assets, data flows, entry points and trust boundaries before coding. The standard includes a concrete SEO Audit Suite example but is not limited to that application.

## Security coverage

Applicable topics include secrets, private data, authentication/authorization and IDOR, input/output injection, SSRF and external requests, browser automation, rate and resource limits, payments where present, dependencies, CI/CD and AI agent permissions. **Not every control applies to every application**: justify N/A decisions.

## Evidence-based release decisions

- **PASS — Release Candidate Security Verified:** mandatory applicable checks within a declared scope executed and passed; significant findings were triaged; regression evidence recorded. This is **not deployment approval**.
- **FAIL — Release Blocked:** a confirmed blocking issue or essential security/regression test failure remains.
- **INCOMPLETE — Verification Pending:** required authorization, environment, execution, or evidence is missing. Never convert unexecuted checks into PASS.

See [acceptance criteria](docs/SECURITY_ACCEPTANCE_CRITERIA.md) and [release checklist](examples/SECURITY_RELEASE_CHECKLIST.md). Any sample table is a **blank template**, not actual validation evidence.

## Boundaries and responsible use

Perform active security testing **only** on assets you own or are explicitly authorized to test, preferably in isolated non-production environments with synthetic accounts and fake secrets. Never paste real credentials into prompts or reports. Third-party scanners and advisory tools must be configured independently and their output reviewed. Avoid presenting toolkit adherence as a penetration test, certification, OWASP endorsement or a guarantee of security.

## License and publication status

**MIT license text is included** in [LICENSE](LICENSE), with copyright holder **Muhammad Noman Siddique** (2026), as selected by the project owner. Independent verification of rights to license all original material remains outside this package review. See [licensing review](docs/LICENSING-REVIEW.md). **Public GitHub publication has not been authorized.**

## Contributing

Before accepting external contributions or publishing: confirm the license, remove sensitive information, use review branches, include minimal reproducible evidence for security-related changes, and do not disclose live vulnerabilities or secrets publicly. See [SECURITY.md](SECURITY.md).

## Project history

See [CHANGELOG.md](CHANGELOG.md). This package wraps the original v1.1 toolkit without changing it. No security-scan or integration-test claims are made for other software.
