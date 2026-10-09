# AEQ-PM-005 — First Team Meeting: Facilitator Script
**Project:** AEQUISON / AEQ-1  
**Document revision:** 0.2 (draft)  
**Meeting:** 001 — Program Kickoff  
**Duration:** 115 minutes (technical working session; no introductions)  
**Facilitator:** To be assigned  
**Minute-taker:** To be assigned  
**Meeting date / attendance:** Record privately

> **Use:** Read the italicized *Say* sections aloud as a starting script; use the **Ask**, **Decide**, and **Record** prompts to facilitate. Nothing below represents an approved team decision. Record names, contact details, internal budgets, IP agreements, and sensitive designs in the private workspace—not in this public file.

## Before everyone joins (5–7 minutes of preparation)
Open these materials:
- [Kickoff agenda and checklist](AEQ-PM-004-Kickoff-Meeting-Checklist.md)
- [Program overview](../RESEARCH.md)
- [Development process](../DEVELOPMENT.md)
- [Competition compliance](../COMPETITION.md) and [official Boom Prize rules](https://boomsupersonic.com/prize)
- [Research roadmap](../ROADMAP.md)
- [Documentation control](../DOCUMENT_CONTROL.md)
- [Safety and scope](../SAFETY.md)
- [AEQ-AER-001 literature review](../research/AEQ-AER-001-Transonic-Aerodynamics-Literature-Review.md)

Prepare a private decision log and action log. Nominate someone other than the facilitator to capture exact decisions. If this is being recorded, obtain everyone's consent and agree on secure retention before starting.

## 00:00–00:05 — Technical kickoff (skip introductions)

**Say:** *“We already know each other and our strengths, so let's get straight into AEQUISON. This is first and foremost a documented aerospace research project, with the Boom Prize as a separate competition objective. Today we need to agree on what we're studying, who owns which research tasks, how we'll review results, and what would make the project feasible or infeasible. We aren't approving a particular aircraft configuration today.”*

### Known team strengths (starting assignments, pending mutual confirmation)
| Team member | Known strengths | Proposed primary responsibility | Secondary contribution |
| --- | --- | --- | --- |
| Project initiator | Mechanical design and CAD | Design/CAD research lead; documentation of geometry concepts and engineering trade studies | Integrate project requirements and research records |
| Engineering partner | CAD and finite-element analysis | Structural/FEA research lead; benchmark validation and structural methods | CAD review, peer review of geometry assumptions |

**Ask:** “Does that split work for us? Who will cover MATLAB, CFD, competition rules, safety, and document reviews? Which subjects need an outside reviewer?”

**Decide:** Confirm the above roles; nominate a note-taker and research task tracker; record any uncovered responsibilities. **Do not assume either person's expertise extends to high-speed flight testing.**

**Record privately:** Role agreement, realistic availability, and gaps needing outside expertise.

## 00:05–00:20 — Define the program mission and success

**Say:** *“Our current working mission is to investigate transonic flight through repeatable calculations, published benchmark replication, structural research, and controlled experimental methods. The Boom Prize is a separate competition objective. We need success criteria for the research that don't depend on winning.”*

**Ask:**
- What would count as a successful research year even without competition qualification?
- Are our priorities technical publications, hands-on experimental learning, graduate research, the prize, or some combination?
- Should extended low-speed loiter be a core research question or a secondary concept?
- What are the current unknowns we must not pretend are solved?

**Decide:** Approve or revise a one-paragraph research mission and 3–5 measurable Phase 1 outcomes.

**Record:** AEQ-PM mission decision; what is explicitly outside Phase 1 scope.

## 00:20–00:35 — Competition, academic, and future-business boundaries

**Say:** *“We want to evaluate the prize seriously, but its eligibility, funding, verification, and testing rules are external constraints. We won't assume our software licenses, university resources, personal equipment, or future commercial uses are automatically permitted.”*

**Ask:**
- Who will own a current-version copy of official competition rules and change notifications?
- Which rules are verified, and which require clarification directly from Boom?
- What is permitted for donated materials, university software, academic facilities, personal funds and any commercial affiliation?
- How will contributions, authorship, research ownership, confidentiality and potential future use be documented?
- What is the intended relationship, if any, between AEQUISON and ORYJIN?

**Decide:** Appoint competition/eligibility owner; assign a written question list to organizers; identify qualified help for IP and licensing questions.

**Record:** Rule source/date; open interpretations; responsible contact and follow-up date. Do not claim organizer approval based on assumptions.

## 00:35–00:55 — Research workstreams and technical questions

**Say:** *“We are choosing what to investigate first—not choosing a final aircraft configuration. Our first results should be independently reproducible, with sources and uncertainty documented.”*

Discuss each workstream in turn:

| Workstream | Starter question | First evidence |
| --- | --- | --- |
| Atmosphere and MATLAB | Can we reproduce published speed-of-sound and atmospheric reference tables? | Checked script, data comparison, units and error |
| Aerodynamics and CFD | Can we reproduce a published transonic benchmark with a documented convergence study? | Source data, solver settings and comparison report |
| Wing architecture | What does published research show about variable sweep versus fixed alternatives and mass/endurance tradeoffs? | Literature matrix with contradictory evidence noted |
| Structures and ANSYS Mechanical | Which introductory structural benchmarks establish trust in our FEA workflow? | Independently checked benchmark result |
| Propulsion research | What broad air-breathing technologies have relevant operating constraints and evidence gaps? | Neutral literature trade report |
| Flight dynamics | Can we simulate and validate conventional low-speed dynamics, disturbances and sensor uncertainty? | Reproducible subsonic model tests |

**Ask:** “Which research questions can we answer with existing tools? Which claims depend on data we do not have? Who can independently review each other's work?”

**Decide:** Rank the first three research deliverables. Assign design/CAD literature work provisionally to the project initiator, structural/FEA benchmark work provisionally to the engineering partner, and nominate appropriate authors and independent reviewers for the remaining tasks.

**Record:** Deliverable IDs, acceptance evidence, dependencies, and review dates.

## 00:55–01:10 — Safety, regulatory reality and stop-work authority

**Say:** *“Simulation is not proof of flight safety. We currently have no authorization for supersonic operations. Any physical work must pass the applicable legal and independent safety reviews. The team must be able to stop unsafe work without pressure to meet a prize deadline.”*

**Ask:** 
- Who has explicit stop-work authority?
- Who checks applicable FAA rules and any test-site permissions?
- What incident, near-miss and hazard reporting procedure will we use?
- What conditions would force a no-go decision or redesign of the research program?
- Who is qualified to provide independent safety and regulatory review?

**Decide:** Safety lead; reporting channel; rule that unapproved tests do not proceed.

**Record:** Risk register owner, immediate hazards, and unresolved authorization needs.

## 01:10–01:25 — Documentation, computing and collaboration

**Say:** *“We already have SolidWorks, Inventor, MATLAB, partner-held ANSYS Mechanical, a workstation, and TrueNAS. The goal is to make results reproducible and accessible to authorized teammates without losing version history or publishing confidential files.”*

**Ask:**
- Which MATLAB toolboxes are available? Which ANSYS license terms actually permit this work?
- What is the authoritative location for source code, CAD masters, raw data, reports and meeting minutes?
- Who can publish to the public GitHub repository? Who approves a release?
- How do we handle file names, document numbers, revision history, issue assignments and pull-request review?
- Who verifies backups by actually restoring a sample dataset?

**Decide:** Public/private repository policy, NAS dataset ownership, backups, branch-review process, and document-control lead.

**Record:** AEQ-IT-001 inventory owner, AEQ-CFG-001 approval, data access and backup verification tasks.

## 01:25–01:35 — Money, time, and realistic feasibility

**Say:** *“Our initial research budget range is $5,000–$10,000. That is not a proven budget for a qualifying supersonic vehicle. We will protect cash by purchasing only what an approved research milestone needs.”*

**Ask:**
- Is the available amount committed, estimated, or contingent?
- What parts of the research can be completed with existing software and hardware?
- What spending amount can an owner approve without a team review?
- What external expertise or authorized testing resources would change program feasibility?
- What are our schedule and personal-availability constraints?

**Decide:** Initial spending cap, purchase-approval method, and first budget review date.

**Record privately:** Funding commitments, cost owner, and approval authority. Do not publicly disclose individual contributions without consent.

## 01:35–01:50 — Assign first actions and milestones

**Say:** *“Every action leaving this room needs one accountable owner, one due date, and a clear way to verify completion. ‘Research CFD’ isn't an action. ‘Deliver a reviewed bibliography and source-data inventory for one published benchmark’ is.”*

**Starter assignments — edit in the private meeting minutes:**

| ID | Action | Definition of done | Owner | Due |
| --- | --- | --- | --- | --- |
| ACT-001 | Reconcile competition rules | Official links, date checked, unresolved questions | TBD | TBD |
| ACT-002 | Confirm design/CAD and CAD/FEA roles and remaining coverage | Approved RACI with independent reviewers | Both partners | TBD |
| ACT-003 | Validate atmosphere model | MATLAB script, cited reference values, error table | TBD | TBD |
| ACT-004 | Identify a public CFD benchmark | Source paper, datasets, permitted use, validation criteria | TBD | TBD |
| ACT-005 | Review variable-sweep literature | Neutral comparison and uncertainty inventory | Design/CAD lead (proposed) | TBD |
| ACT-006 | Complete software/license inventory, including ANSYS Mechanical | Version, owner, license restrictions, permitted use | Both partners | TBD |
| ACT-007 | Test TrueNAS permissions and backups | Authorized access and a documented restore test | TBD | TBD |
| ACT-008 | Review safety and regulatory pathway | Written open questions and qualified-review needs | TBD | TBD |
| ACT-009 | Draft authorship/IP/publication principles | Items needing team consent or professional advice | TBD | TBD |

**Decide:** Owners, reviewers, due dates, and Meeting 002 date. Avoid assigning more work than the team can deliver.

## 01:50–01:55 — Decision read-back and close

**Say:** *“Before we end, I'm going to read back the decisions we actually made, the items we deferred, and the actions we assigned. If I misstate anything, correct me now. Our standard is evidence before claims and review before public release. We want this to remain worthwhile research whether or not we eventually qualify for the competition.”*

**Read back and confirm:**
1. Research mission and program scope
2. Competition eligibility questions and owner
3. Research deliverables and reviewer assignments
4. Safety lead and stop-work process
5. Documentation and data-sharing rules
6. Approved spending process
7. Action owners, due dates and next meeting

**Record:** Accepted / deferred / disputed decisions and the date of next review.

## Within 24 hours after the meeting
- [ ] Write accurate private minutes; distinguish proposals from actual decisions.
- [ ] Request corrections from attendees.
- [ ] Enter approved decisions into the decision log, with evidence.
- [ ] Create GitHub issues for approved non-sensitive action items.
- [ ] Update the roadmap only where the team approved a change.
- [ ] Update the private RACI, risks, budget, and evidence registers.
- [ ] Publish a short public meeting summary **only after publication approval**.

---

### Simple private meeting-minutes template

**Date / start–end / location:** TBD  
**Attendees:** TBD  
**Chair / minutes / reviewer:** TBD

**Approved decisions**  
| ID | Decision | Reason | Approver(s) | Reference |
| --- | --- | --- | --- | --- |
| DEC-001 | TBD | TBD | TBD | TBD |

**Open questions**  
| ID | Question | Owner | Answer needed by |
| --- | --- | --- | --- |
| OPEN-001 | TBD | TBD | TBD |

**Actions**  
| ID | Action | Deliverable / done criteria | Owner | Reviewer | Due |
| --- | --- | --- | --- | --- | --- |
| ACT-001 | TBD | TBD | TBD | TBD | TBD |

**Next meeting:** TBD

*This script is a facilitator aid. It does not assert that the team has agreed to any proposed decision or that regulatory approvals have been obtained.*
