# AEQ-AER-001 — Transonic Aerodynamics: Fundamentals and Literature Review

| Document field | Value |
| --- | --- |
| Program | Project AEQUISON — AEQ-1 |
| Document ID | AEQ-AER-001 |
| Revision | 0.1 |
| Date | 2026-10-08 |
| Status | **Draft — literature review; not peer approved** |
| Author | AEQUISON research team (working draft) |
| Technical reviewer | **Unassigned — required before approval** |
| Research track | Graduate-level foundational aerodynamics |
| Companion documents | [Research overview](../RESEARCH.md), [verification policy](../VERIFICATION.md), [development framework](../DEVELOPMENT.md) |

> **Research integrity statement:** This report reviews publicly documented aerodynamic science. The team has not yet run or independently validated its own transonic CFD results. Figures currently on AEQUISON's website are conceptual illustrations, not numerical or experimental evidence. This report does not establish the feasibility of an actual Mach 1 UAV.

## Abstract

Transonic flow presents a mixture of subsonic and supersonic local flow regions, compressibility effects, shock waves, and potentially strong interactions between shocks and turbulent boundary layers. Consequently, the onset of locally sonic flow, the subsequent rapid increase in drag, and the transition to globally supersonic flight are distinct phenomena. This report surveys foundational concepts and public NASA technical resources relevant to these effects, identifies an independent validation reference case, and outlines evidence standards for subsequent AEQUISON research. The central conclusion is that reliable computational predictions must be verified numerically and validated against experiment before being used to justify engineering decisions.

**Keywords:** transonic flow; compressibility; critical Mach number; drag divergence; shock wave; boundary layer; CFD verification; experimental validation; RAE 2822.

## 1. Research objective and scope

**Research question:** What physical phenomena and numerical uncertainties make transonic aerodynamic predictions challenging, and what publicly documented evidence can the AEQUISON team use to evaluate its computational methods?

**Objectives**
1. Summarize relevant compressible-flow concepts with primary references.
2. Distinguish onset of local sonic flow from drag divergence and free-stream Mach 1.
3. Identify why shocks, viscous effects, and flow separation complicate predictions.
4. Select a published experimental benchmark as a foundation for future validation.
5. Define reproducibility, verification, and independent technical review expectations.

**Outside the present scope:** selection or optimization of an AEQUISON airframe, detailed high-speed vehicle sizing, propulsion integration, supersonic flight-test planning, or claims that a competition entry can meet the Boom Prize requirements.

## 2. Fundamental concepts

### 2.1 Mach number and compressibility

Mach number is the ratio of flow speed to the **local** speed of sound:

```text
M = V/a
a = sqrt(gamma * R * T)
```

Here `V` is the flow speed, `a` is local sound speed, `gamma` is the ratio of specific heats, `R` is the specific gas constant, and `T` is absolute temperature. For calorically perfect air, `gamma ≈ 1.4` and `R ≈ 287 J/(kg·K)` are common introductory assumptions. They are not universal constants for all temperatures and gases.

NASA explains that compressibility changes the local density and therefore the forces associated with airflow. Near Mach 1, compressibility cannot generally be neglected. It is essential to distinguish free-stream Mach number `M_inf` from a *local* Mach number evaluated near an aircraft surface [1].

### 2.2 Critical Mach number versus drag divergence

The **critical Mach number** is the free-stream Mach number at which sonic flow is first encountered locally on a body. This can occur while the free stream is still subsonic [2].

**Drag-divergence Mach number** describes the onset of a pronounced increase in drag associated with compressibility effects. It is conceptually different from critical Mach number and from Mach 1 in the undisturbed free stream [2].

These definitions matter for scientific interpretation: a visualization showing a local sonic patch does not demonstrate that the aircraft itself reached Mach 1.

### 2.3 Shocks and shock–boundary-layer interaction

Sharp compressive disturbances can produce shock waves, across which flow properties change rapidly. NASA's overview identifies shocks and their influence on lift, drag, and downstream flow conditions [1]. In viscous flows, an adverse pressure gradient near a shock can interact with the boundary layer and contribute to separation. Where separation is present, a steady-state model may not capture every important unsteady phenomenon [3].

Reported shock locations or pressure peaks must therefore be interpreted in light of turbulence-model choices, grid quality, boundary conditions, and experimental uncertainty.

### 2.4 Other relevant effects

- **Geometry and three-dimensionality:** Real wings display spanwise flow, tip effects, and other behavior absent from two-dimensional reference airfoil cases.
- **Reynolds number:** Viscous behavior depends on flow scale, velocity and fluid properties.
- **Transition and turbulence:** Boundary-layer transition assumptions can influence simulated pressure and separation.
- **Unsteadiness:** Not every transonic flow field is adequately represented by a steady solution.
- **Structural coupling:** Aeroelastic effects are a separate multidisciplinary research concern, but this report does not analyze a specific airframe.

These factors help explain why a two-dimensional benchmark is an important learning exercise but cannot validate a complete three-dimensional vehicle design.

## 3. Literature review: verified primary research sources

### [1] NASA Glenn Research Center — Role of the Mach Number
**Link:** https://www1.grc.nasa.gov/beginners-guide-to-aeronautics/role-of-the-mach-number/

**Contribution:** Provides definitions and introductory physical explanations of compressibility and flow disturbances as Mach number increases.

**Use within AEQUISON:** Check the meaning, units and assumptions of baseline atmosphere and Mach calculations. This source is introductory, not a substitute for advanced experimental validation.

### [2] NASA — Research in Supersonic Flight and the Breaking of the Sound Barrier
**Link:** https://www.nasa.gov/history/SP-4219/Chapter3.html

**Contribution:** Historical technical discussion distinguishing the onset of surface-sonic flow from subsequent drag divergence, and documenting early compressibility investigations.

**Use within AEQUISON:** Establish accurate terminology, avoid conflating local critical Mach number with aircraft free-stream Mach 1, and provide research history.

### [3] NASA Glenn — Overview of CFD Verification and Validation
**Link:** https://www.grc.nasa.gov/www/wind/valid/tutorial/overview.html

**Contribution:** Distinguishes computational model implementation, verification, validation and uncertainty. Reviews compressible flow, boundary layers, shocks and separation as CFD challenges.

**Use within AEQUISON:** Establish the verification and validation requirements to be applied to numerical studies before interpreting predictions.

### [4] NASA Glenn — RAE 2822 Transonic Airfoil Validation Archive
**Link:** https://www.grc.nasa.gov/www/wind/valid/raetaf/raetaf.html

**Contribution:** A documented two-dimensional transonic airfoil experimental comparison case, including geometry, pressure-coefficient and boundary-layer measurement references. The archive describes an experimental case at Mach 0.725, Reynolds number 6.5 million and nominal angle of attack 2.92 degrees. These are **published benchmark conditions**, not suggested operating parameters for AEQUISON.

**Use within AEQUISON:** A candidate *independent reference dataset* for learning numerical model validation. Any later report must acknowledge details of experimental corrections and source-data limitations.

### [5] NASA Glenn — RAE 2822 Transonic Airfoil Study #5
**Link:** https://www.grc.nasa.gov/www/wind/valid/raetaf/raetaf05/raetaf05.html

**Contribution:** NASA's comparison of multiple turbulence modeling approaches against experimental pressure data in two-dimensional transonic flow.

**Use within AEQUISON:** Investigate sensitivity of conclusions to physical modeling assumptions, rather than assuming that agreement from one turbulence model proves validity.

### [6] NASA Glenn — Tutorial on CFD Verification and Validation
**Link:** https://www.grc.nasa.gov/www/wind/valid/tutorial/tutorial.html

**Contribution:** Organizes discussions of iterative, spatial and temporal convergence, validation, uncertainty and related terminology, drawing on an established AIAA V&V framework.

**Use within AEQUISON:** Define document review checklists and repeatability standards for published computational research.

### [7] NASA Technical Reports Server — Grid Convergence for Three Dimensional Benchmark Turbulent Flows
**Link:** https://ntrs.nasa.gov/citations/20190000713

**Contribution:** Describes grid-refinement and code-to-code comparisons for multiple benchmark flows, including a transonic ONERA M6 wing case.

**Use within AEQUISON:** Understand how conclusions from a simpler two-dimensional benchmark can lead into a more rigorous study of three-dimensional numerical uncertainty. This is a **future literature extension**, not a completed AEQUISON validation activity.

## 4. Synthesis of the literature

| Topic | Supported conclusion | Limitation / unresolved question |
| --- | --- | --- |
| Mach number | Compressibility matters increasingly as Mach number rises [1]. | Ideal-gas assumptions and local atmospheric conditions require disclosure. |
| Critical Mach | Local sonic flow can appear before free-stream Mach 1 [2]. | Depends on body geometry and operating state. |
| Drag divergence | A pronounced drag rise is distinct from the first occurrence of local sonic flow [2]. | No AEQUISON drag estimate has been produced. |
| Shock behavior | Shocks change downstream flow and aerodynamic force distributions [1,3]. | Shock–boundary-layer interaction may require careful turbulence and unsteadiness modeling. |
| CFD credibility | Verification, validation and uncertainty are essential [3,6]. | A solver converging does not alone validate its physical predictions. |
| Published benchmarks | NASA provides reference airfoil and three-dimensional cases [4,5,7]. | Reproducing a benchmark does not establish complete-aircraft predictive accuracy. |

**Initial research finding:** The key technical challenge in transonic aerodynamic research is not simply calculating a speed threshold; it is faithfully representing compressible and viscous flow while measuring the numerical and experimental uncertainty associated with the predicted behavior.

## 5. Proposed validation methodology for a subsequent study

A separate document, `AEQ-CFD-001`, will describe a benchmark-only comparison against NASA's published RAE 2822 dataset. Before generating results, that study must record:

1. Which public reference geometry and dataset revision are used.
2. The simulation software, precise version and permitted license status.
3. All referenced assumptions and the intended model-validation scope.
4. Numerical consistency, iterative and mesh-convergence evidence.
5. Defined comparison quantities and acceptance criteria chosen *before* viewing results.
6. Experimental-data provenance, uncertainty and known corrections.
7. Discrepancies, negative results and independent reviewer comments.

This literature review **does not** provide a vehicle-specific simulation setup or a validated high-speed aircraft configuration. Any future results should be published only after the team has assessed licensing, safety, IP, and publication permissions.

## 6. Open research questions

1. Which published datasets offer sufficient measurement quality and metadata for independent validation?
2. How sensitively do different turbulence assumptions influence publicly documented transonic airfoil predictions?
3. What numerical error can be separated from physical modeling error?
4. Under what circumstances are two-dimensional benchmark results an insufficient proxy for three-dimensional flow?
5. How should evidence from a literature study be translated into graduate-level research questions without overstating predictive validity?

## 7. Relevance to AEQUISON's three pathways

**Graduate research:** This review is a starting point for a potential adviser-approved thesis proposal involving compressible-flow modeling, benchmark reproducibility or numerical uncertainty. It does not represent accepted graduate work.

**Boom Prize:** The competition is a distinct feasibility and compliance context. This report makes no prediction of qualification or aircraft performance.

**Potential future commercial applications:** Reproducible analysis methods and scientific findings may be commercially useful, but ownership, university rules, team contributions and software licenses need independent review before any business use.

## 8. Limitations and disclosure

- No original transonic experiments or validated CFD results are presented.
- This review relies on selected NASA and historical research sources; it is **not yet a systematic literature review**.
- Sources may contain experimental corrections and assumptions not reproduced here.
- No quantified tradeoff or recommendation for an AEQUISON airframe, propulsion system, or variable-sweep mechanism is supported by this review.
- Independent subject-matter review remains pending.
- This report is an educational and research document; it does not authorize flight operations.

## 9. Planned review and publication checklist

- [x] Document identifier, revision and research objective established
- [x] Primary technical sources linked
- [x] Definitions and major physics concepts reviewed
- [x] Initial research gaps and limitations recorded
- [ ] Team technical reviewer assigned
- [ ] Source accuracy and interpretation independently checked
- [ ] Reference metadata and source versions archived internally
- [ ] Review comments resolved
- [ ] Graduate adviser consultation, if applicable
- [ ] Status changed from Draft to Approved

## 10. Revision history

| Revision | Date | Description |
| --- | --- | --- |
| 0.1 | 2026-10-08 | Initial literature synthesis and proposed evidence framework. Not peer approved. |
