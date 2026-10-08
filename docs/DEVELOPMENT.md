# AEQ-DEV-001 — Research-to-Demonstration Development Framework
**Revision 0.1 · Draft · 2026-10-08**

AEQUISON documents **both research and engineering development**. This page explains how each claim, digital model, laboratory investigation, and separately authorized low-speed demonstration is recorded. The Boom Prize remains a separate competition track.

## Lifecycle and evidence gates
| Stage | Purpose | Deliverables | Status |
|---|---|---|---|
| D0 — Needs and scope | Define mission questions and bounds | Charter, research objectives, competition comparison | Draft |
| D1 — Requirements and architecture | Compare subsystem options without assuming feasibility | Traceability matrix, concept reviews, trade studies | Planned |
| D2 — Modeling | Study physical behavior with independent reference material | MATLAB, CFD and FEA model reports | Planned |
| D3 — Verification | Test whether models and methods are implemented correctly | Mesh/solver convergence, unit tests, peer review | Planned |
| D4 — Non-flight experiments | Validate instruments, materials, and basic methods | Laboratory procedure, calibrated data, test report | Planned |
| D5 — Subsonic demonstrator | Verify low-speed systems only under appropriate authorization | Safety review, test readiness and verified results | Conditional |
| D6 — Research closeout | Evaluate evidence and remaining uncertainty | Accepted reports, limitations, next-phase review | Planned |

This framework is **not** a construction plan for a Mach 1 unmanned aircraft or authorization for supersonic flight.

## Research-build record requirements
For each approved physical research activity, record: purpose; linked requirement; hazards and approvals; responsible investigator; materials and equipment provenance; as-tested configuration; instrumentation calibration; raw data location; date; deviations; observations; reviewer; and release decision.

## Configuration states
**Proposed → Reviewed → Approved for limited research → Verified → Archived.** No item changes status without evidence and review. Proposed features such as variable sweep and specific propulsion technologies are **not adopted designs**.

## Data handling
Large files and sensitive internal records belong in private team storage/TrueNAS, not this public repository. Public summaries may link to sanitized, reviewer-approved results after scientific, licensing, safety and IP checks.

## First technical development tasks
1. Verify MATLAB atmospheric model against published reference values.
2. Reproduce a well-documented public compressible-flow CFD benchmark.
3. Compare published fixed-wing and variable-sweep data as a literature study.
4. Create an approved general-purpose low-speed instrumentation validation plan.
