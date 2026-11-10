# Session 01 — Program Orientation, Eligibility & Development Environment Setup

| Field | Detail |
|---|---|
| **Program** | Claude Certified Architect – Foundations (CCAR-F) |
| **Track** | 30-session structured preparation program (Anthropic Academy courses, hands-on builds, timed practice) |
| **Date** | Tuesday, November 10, 2026 |
| **Status** | ✅ Complete |
| **Author** | Manu — Senior Software Engineer (Flutter · Android/iOS · React/Next.js) |

## Objective

Establish the foundation for the certification track: confirm exam eligibility, provision the learning and development accounts, and set up a safe, cost-controlled API environment before beginning coursework.

## Summary of Work Completed

1. **Certification eligibility assessment**
   - Reviewed Anthropic's certification policy: CCAR-F registration is currently limited to employees of organizations in the Claude Partner Network, verified against a company email domain on the partner record.
   - Checked my employer against the public Claude Partner Network directory (Claude Marketplace, service partners listing).
   - **Outcome:** Employer is not currently a network partner, so exam registration is deferred. All preparation — courses, builds, and practice — is open to the public and proceeds as planned; the credential will be pursued when partner access becomes available.

2. **Learning platform provisioning**
   - Created an Anthropic Academy (Claude Academy) account and verified access to the six-course curriculum: AI Fluency Foundations, Claude 101, Building with the Claude API, Claude Code in Action, Introduction to Model Context Protocol, and Introduction to Agent Skills.

3. **API environment setup (security-first)**
   - Created an Anthropic Console account and generated an API key for development use.
   - Configured a low monthly spend limit in the Console as a cost-control guardrail for coursework and experiments.
   - Stored the key in a local `.env` file excluded from version control via `.gitignore`. The key is never committed, shared, or embedded in source code.

## Key Concepts Established

- **Certificate vs. certification:** Course completion certificates attest to coursework; the CCAR-F certification is a proctored examination (60 scenario-based questions, 120 minutes, pass mark 720/1,000, Pearson VUE). The two are tracked separately throughout this program.
- **Credential safety model:** An API key functions as both identity and billing credential. Standard handling applies: least exposure, local-only storage, immediate revocation and rotation if compromised, and spend limits as a blast-radius control.
- **Program structure:** Five weighted exam domains, led by Agentic Architecture & Orchestration (27%); preparation is organized as 30 one-hour sessions combining official Anthropic coursework, four hands-on builds, and timed practice assessments.

## Decision Log

| Decision | Rationale |
|---|---|
| Proceed with full preparation despite exam-registration deferral | Coursework and portfolio builds are publicly accessible and independently valuable; eligibility may change, and readiness should not wait on it |
| Enforce a spend limit before writing any API code | Prevents uncontrolled cost from experimental or looping code during learning |
| Document the program in a public repository | Provides verifiable evidence of skills and sustained, structured self-directed learning |

## Next Steps

- **Session 02:** Read the official CCAR-F Exam Guide (v1.0) end to end; produce a one-page brief covering the five domains, the six published exam scenarios, and the out-of-scope topics.
