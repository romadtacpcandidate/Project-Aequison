# AEQ-CFG-001 — Documentation & Configuration Control
**Rev 0.1 | Draft**

## Identifiers
Use AEQ-[DISCIPLINE]-[NUMBER], such as AEQ-MAT-001 or AEQ-COMP-001.

## Required document header
Title, identifier, revision, date, author, reviewer, status (Draft/In Review/Approved/Superseded), source references, applicable requirements, and a revision history.

## Workflow
1. Open a tracked issue describing a problem or deliverable.
2. Create a named feature branch.
3. Add reproducible research, sources and limitations.
4. Request independent review through a pull request.
5. Record consequential decisions in AEQ-DEC-001.
6. Merge approved updates; tag approved baselines.
7. Link verification evidence to requirement identifiers.

## Internal control registers
AEQ-REQ-001 requirements; AEQ-RACI-001 team responsibility assignments; AEQ-RISK-001 risks; AEQ-DEC-001 decision log; AEQ-VER-001 verification; AEQ-IT-001 licensed tools; AEQ-PM-002 budget; AEQ-CFG-003 publication approval.

Internal budgets, team identities, proprietary CAD, sensitive aircraft data, access credentials, and unapproved work must not be placed in a public repository. Use a private team repository and TrueNAS backups.

## Public release checklist
Scientific accuracy; source and license permission; privacy; safety; legal/export-control implications; competition rules; team approval.
