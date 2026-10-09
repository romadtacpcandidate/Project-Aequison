# AEQ-PM-004 — Project Kickoff Meeting Checklist and Agenda

**Decision reference:** [AEQ-PM-006 — Project Planning and Decision Checklist](AEQ-PM-006-Project-Decision-Checklist.md). Use this as the master list of topics and decisions; this file remains a shorter timed agenda.

**Companion document:** [AEQ-PM-005 — Full First-Meeting Facilitator Script](AEQ-PM-005-First-Meeting-Facilitator-Script.md). It expands this 90-minute checklist into a 120-minute moderator's script with questions and decision prompts.

| Control field | Value |
| --- | --- |
| Program | AEQUISON — independent aerospace research & experimental development |
| Meeting | Kickoff / Meeting 001 |
| Revision | 0.2 |
| Prepared | 2026-10-08 |
| Status | Draft — decisions not yet approved |
| Planned duration | 90 minutes (focused technical meeting; no introductions) |
| Chair / note-taker / reviewer | Assign at meeting |
| Location and date | TBD |
| Sensitive minutes | Store in private team workspace, not this public repository |

> **Meeting purpose:** Align the existing AEQUISON team on a credible graduate-level research program with a separate Boom Prize track and possible future ORYJIN/commercial applications. Establish **who owns each task and where evidence is recorded** before spending or testing.

## Before the meeting — circulation checklist

- [ ] Share the [project README](../README.md), [program research overview](RESEARCH.md), [development plan](DEVELOPMENT.md) and [roadmap](ROADMAP.md).
- [ ] Ask everyone to read the [Boom Prize compliance summary](COMPETITION.md) and the current official [Boom rules](https://boomsupersonic.com/prize).
- [ ] Distribute [AEQ-AER-001 transonic literature review](research/AEQ-AER-001-Transonic-Aerodynamics-Literature-Review.md); mark **Draft / not peer reviewed**.
- [ ] Collect voluntary summaries of team skill sets, availability and preferred roles **privately**.
- [ ] Confirm current software access: SolidWorks, Inventor, MATLAB; partner's ANSYS Mechanical access and license restrictions.
- [ ] Confirm NAS location, permissions, backups and secure access approach (no credentials in public notes).
- [ ] Bring an itemized **Phase 1 research** budget proposal of $5,000–$10,000; do not treat it as a full competition vehicle budget.
- [ ] Nominate a meeting chair, minutes owner, and independent action-item reviewer.

## Agenda — 90 minutes total

| Time | Topic | Decision / output |
| --- | --- | --- |
| 00:00–00:10 | Confirm known CAD and FEA roles; identify remaining coverage | Design/CAD lead and CAD/FEA lead proposed; research gaps identified |
| 00:10–00:20 | Project mission and success criteria | Approve or revise research-first mission statement |
| 00:20–00:30 | Three tracks: grad research, competition, potential company use | Track separation and unresolved IP / resource issues |
| 00:30–00:40 | Competition constraints and regulatory feasibility | Name competition compliance owner and unanswered organizer questions |
| 00:40–00:53 | Research priorities and technical scope | Select first validated research deliverables; **no aircraft concept prematurely selected** |
| 00:53–01:05 | Documentation, tools, TrueNAS, GitHub, review policies | Assign repository, data and verification owners |
| 01:05–01:15 | Budget, safety, and project risks | Approve an initial research spending cap, identify stop-work authority |
| 01:15–01:25 | Work assignment and near-term calendar | Owners, deadlines, evidence and next meeting |
| 01:25–01:30 | Read-back of decisions | Record accepted, deferred, and disputed items |

## Meeting checklist — record decisions, not just discussion

### A. Program purpose, identity and scope (10 minutes)
- [ ] Confirm name **Project AEQUISON** and research designation **AEQ-1**.
- [ ] Agree on a one-paragraph mission focused on reproducible aerospace research.
- [ ] Confirm Boom Prize as an independent competition objective, **not the sole definition of success**.
- [ ] Confirm graduate-thesis possibilities are exploratory until a university/adviser approves them.
- [ ] Confirm potential commercial use requires separate ownership and permissions review.
- [ ] Agree Phase 1 does **not** claim aircraft performance or authorize high-speed testing.

### B. Team organization (10 minutes)
- [ ] Confirm the project initiator as proposed design/CAD research lead and engineering partner as proposed CAD/FEA and structural research lead; assign a meeting note-taker.
- [ ] Confirm the proposed division: initiator covers design/CAD; partner covers CAD and FEA. Assign or mark gaps for aerodynamic literature/CFD, MATLAB/flight physics, competition compliance, software/data, and safety oversight. Identify independent reviewers.
- [ ] Establish an independent technical reviewer for AEQ-AER-001 and subsequent reports.
- [ ] Confirm team meeting cadence and preferred written communications channel.
- [ ] Define who approves document releases, financial commitments and research changes.
- [ ] Record actual names, contact details and personal commitments in **private minutes**.

### C. Competition, graduate-school and company separation (10 minutes)
- [ ] Review organizer terms; assign someone to recheck live eligibility and rule revisions.
- [ ] Record outstanding questions on variable-sweep eligibility, team funding, institutional facilities and competition measurement requirements.
- [ ] Plan to obtain written organizer clarification **before** relying on academic or company resources.
- [ ] List candidate academic research topics, without claiming they are accepted theses.
- [ ] Discuss team authorship, IP ownership, university research agreements and ORYJIN reuse; consult qualified counsel or university offices when needed.
- [ ] Decide how to separate the records, costs, equipment and permissions of each track.

### D. Engineering research and development priorities (13 minutes)
- [ ] Review [AEQ-AER-001](research/AEQ-AER-001-Transonic-Aerodynamics-Literature-Review.md) and nominate an independent reviewer.
- [ ] Agree first computational milestone: independently check an atmospheric MATLAB reference model.
- [ ] Agree first CFD research milestone: reproduce a **published benchmark**, document numerical uncertainty and compare with reference observations.
- [ ] Define the scope of an evidence-based fixed versus variable-sweep **literature trade study**.
- [ ] Assign a structural methods/FEA **benchmark study** rather than claiming a vehicle design is validated.
- [ ] Assign a propulsion **literature review**; do not presume a selected configuration.
- [ ] Establish test-data definitions and physical experiment approval gates.
- [ ] Record unresolved requirements as open, not silently accepted.

### E. Documentation and collaboration (12 minutes)
- [ ] Approve document IDs, required metadata and revision-controlled reports using [AEQ-CFG-001](DOCUMENT_CONTROL.md).
- [ ] Confirm source-code and document workflow: GitHub issues → branch → pull request → independent review → merge.
- [ ] Decide GitHub public vs private separation and publication approvals.
- [ ] Confirm where large data lives on TrueNAS, who can access it, and how backups/restores will be tested.
- [ ] Verify MATLAB toolboxes and partner ANSYS Mechanical license terms before use in competition-related work.
- [ ] Adopt [AEQ-VER-001](VERIFICATION.md): assumptions, model versions, sources, convergence, validation and uncertainty.
- [ ] Agree to keep an experiment/development log, including failed investigations and negative results.

### F. Budget, hazards, and stop/go criteria (10 minutes)
- [ ] Confirm Phase 1 research funding range **$5,000–$10,000**, separate from future full vehicle development.
- [ ] Set a provisional spending authority and expense-approval procedure.
- [ ] Record funded, in-kind, personally owned and institution-provided resources separately.
- [ ] Identify project-level risks: technical uncertainty, false confidence in simulations, personnel safety, aviation authorization, funding eligibility, software rights, IP and schedules.
- [ ] Confirm no unapproved high-speed tests and no physical activities without appropriate reviews/authorizations.
- [ ] Assign safety lead and explicit stop-work authority.

### G. First action assignments (10 minutes)
- [ ] Assign owner/due date for completion of **AEQ-AER-001 independent review**.
- [ ] Assign owner/due date for **AEQ-MAT-001** source and atmosphere-reference verification.
- [ ] Assign owner/due date for **AEQ-CFD-001** benchmark literature and data inventory.
- [ ] Assign owner/due date for **Boom Prize eligibility written questions**.
- [ ] Assign owner/due date for **software/license inventory**.
- [ ] Assign owner/due date for **TrueNAS access and independent backup restore test**.
- [ ] Assign owner/due date for **team/IP/publication agreement review**.
- [ ] Set date, chair and measurable agenda for Meeting 002.

## Decisions and action-item templates

### Decision record
| ID | Topic | Decision or deferred question | Evidence / rationale | Owner | Review date |
| --- | --- | --- | --- | --- | --- |
| DEC-001 | Research-first mission | TBD | TBD | TBD | TBD |
| DEC-002 | Roles and independent reviews | TBD | TBD | TBD | TBD |
| DEC-003 | Budget authorization | TBD | TBD | TBD | TBD |
| DEC-004 | Public/private information policy | TBD | TBD | TBD | TBD |

### Action register
| ID | Action | Deliverable / acceptance evidence | Owner | Due | Status |
| --- | --- | --- | --- | --- | --- |
| ACT-001 | Independent literature review | Reviewed AEQ-AER-001 with comments | TBD | TBD | Open |
| ACT-002 | Verify atmospheric MATLAB results | Script, test table, source references | TBD | TBD | Open |
| ACT-003 | Inventory CFD benchmark sources | Reference list, permissions, uncertainties | TBD | TBD | Open |
| ACT-004 | Revalidate competition rules | Written rule/eligibility register | TBD | TBD | Open |
| ACT-005 | Check licenses and software | Approved software inventory | TBD | TBD | Open |
| ACT-006 | Check TrueNAS sharing and backups | Access and restore test record | TBD | TBD | Open |
| ACT-007 | Define research/competition/company IP boundaries | Reviewed policy/questions | TBD | TBD | Open |

## Meeting closeout — complete within 24 hours

- [ ] Save dated minutes in the controlled **private** workspace.
- [ ] Publish an approved, non-sensitive meeting summary to GitHub if appropriate.
- [ ] Create/assign GitHub issues with owners, due dates and acceptance criteria.
- [ ] Update project roadmap **only for decisions actually made**.
- [ ] Record unresolved matters and identify next review points.
- [ ] Send the team links to the approved meeting notes and action register.

## Meeting success test

The kickoff meeting succeeds if the team leaves with: **(1)** a shared research mission, **(2)** agreed program/competition/company boundaries, **(3)** named owners and reviewers, **(4)** an initial approved spending process, **(5)** a controlled documentation and data workflow, and **(6)** a first set of verifiable research tasks. Nothing on this page is pre-approved merely because it is checked in a template.
