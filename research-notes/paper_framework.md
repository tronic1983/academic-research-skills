# Paper Framework

> **Target Journal**: *Engineering Applications of Artificial Intelligence* (EAAI)
>
> **Paper Title**: *An Auditable Hybrid Decision-Support Framework Decoupling Multi-LLM Knowledge Extraction from Expert-Driven MCDM for Smart Building Retrofitting*

## 1. Introduction

* **Unnumbered Lead-in (1–2 paragraphs)**
  * Contextualise the urgency of decarbonising existing building stock and the widespread adoption of building automation systems (BAS), Internet of Things (IoT) sensors, and smart control algorithms in energy retrofits.
  * Introduce the core tension: substantial capital investments in smart retrofitting frequently underperform in operation because pre-design appraisal neglects legacy building services constraints and operational human factors, while emerging AI-assisted decision workflows often obscure how evaluation criteria are formed and weighted.
  * Transition smoothly into the specific problem dimensions, research gap, objectives, contributions, and paper organisation.

### 1.1 Background: The Pre-Design to Operation Performance Gap in Smart Building Retrofits
* **Upstream Origins of the Performance Gap**: Explain how operational failures in smart retrofits are often predetermined during pre-design alternative selection rather than solely during construction or commissioning.
* **Static Hardware Bias in Conventional Appraisal**: Critique pre-design evaluations that focus on static hardware inventories (e.g., sensor counts, digital twin dashboards, or green certification checklists) while overlooking aged hydraulic/ductwork infrastructure and the operational capabilities of on-site facility staff.
* **Two Target Operational Failure Modes**: Define the specific post-handover failure mechanisms that pre-design appraisal seeks to prevent:
  1. *Overt abandonment*: Facility operators override automated control loops and revert systems to fixed manual schedules due to tenant comfort complaints or interface complexity.
  2. *Covert malfunction*: Automated algorithms calibrated to idealised new-build assumptions interact poorly with degraded legacy plant, inducing equipment short-cycling and excess energy consumption.

### 1.2 Research Gap
* **Gap 1 — Omission of Operational-Feedforward Logic and Deliverable Verification**: Examine how existing retrofit assessment frameworks lack systematic mechanisms to feed post-handover operational failure risks forward into pre-design criteria, leaving appraisals vulnerable to superficial compliance (Goodhart's Law) via unverifiable paper promises.
* **Gap 2 — Opaque Upstream Criteria Formation and Unbounded LLM Use in MCDM**: Focus on upstream decision-structure transparency—specifically criteria provenance, selection logic, evidence-to-criterion transformation, and contextual validity. Critique the growing tendency in engineering MCDM studies to deploy Large Language Models (LLMs) as unverified virtual experts or end-to-end scorers, which introduces hallucination, correlated errors from overlapping pre-training corpora, circular reasoning, and non-auditable judgements. (Frame the "criteria-formation black box" strictly as a descriptive metaphor for opaque criteria provenance rather than a formal theory or method name.)

### 1.3 Research Objectives
* **Epistemological Scope Statement**: Define the study as developing a normative pre-design decision-support framework focused on internal content validity, weight consistency, and algorithmic robustness, explicitly refraining from claiming longitudinal post-occupancy predictive validity.
* **Specific Research Objectives (RO1–RO3)**:
  * **RO1 (Auditable Evidence Acquisition and Extraction)**: Establish a transparent protocol combining dual-track PRISMA searching (academic literature and building standards), parallel multi-LLM screening with verbatim evidence binding, stratified manual error auditing, and LLM-assisted inductive grounded coding.
  * **RO2 (Operational-Feedforward Evaluation Index System Construction)**: Formulate an Evaluation Index System (EIS) and bundled Strategic Design Pathways (SDPs) anchored to verifiable pre-design technical deliverables.
  * **RO3 (Decoupled Expert-Driven MCDM Appraisal and Validation)**: Operationalise two-round Fuzzy Delphi Method (FDM) screening, Full Consistency Method (FUCOM) weighting, and Combined Compromise Solution (CoCoSo) pathway prioritisation across separate, non-overlapping expert panels, followed by weight perturbation and cross-method robustness verification.

### 1.4 Main Contributions
* **Bounded Contributions Aligned with Actual Evidence**:
  1. *Transparent Upstream Decision-Structure Formation*: Demonstrate an auditable human–AI role separation in which multiple LLMs extract and structure candidate constructs with verbatim source traceability, while stratified manual auditing and rule-based arbitration quantify and control correlated extraction errors.
  2. *Operational-Feedforward Retrofit Evaluation Structure*: Establish an EIS whose operational definitions are anchored to verifiable pre-design technical deliverables, capturing legacy plant compatibility and facility-management usability while curbing superficial compliance.
  3. *Independent Multi-Panel Hybrid Appraisal*: Separate knowledge elicitation, consensus screening, criteria weighting, and pathway performance scoring across four distinct expert panels to prevent cross-stage anchoring and circularity, supported by systematic sensitivity and cross-model ranking checks.
  4. *Pre-Design Baseline Profiling for Retrofit Governance*: Provide a structured, traceable pre-design assessment record capable of serving as an auditable baseline for staged post-occupancy verification schemes.

### 1.5 Paper Organization
* Provide a concise, direct roadmap outlining the content and structure of `Section 2` (Literature Review), `Section 3` (Proposed Framework and Methodology), `Section 4` (Empirical Case Study), `Section 5` (Research Results), `Section 6` (Validation and Implication), and `Section 7` (Conclusion and Limitations).

---

## 2. Literature Review

* **Unnumbered Lead-in (1–2 paragraphs)**
  * State the critical review objective: examining the empirical and methodological claims underlying operational-feedforward smart retrofit appraisal, LLM-assisted knowledge extraction, and multi-criteria decision-making (MCDM) without imposing the study's final taxonomy onto existing scholarship.

### 2.1 Operational-Feedforward Perspectives in Smart Building Retrofitting
* **Performance Gap and Handover Literature**: Critically review empirical studies on the discrepancy between predicted and measured energy performance in retrofitted buildings, focusing on handover discontinuities and Soft Landings principles.
* **Legacy Physical Constraints and Operational Human Factors**: Synthesise findings on how aged mechanical/hydraulic systems, limited plantroom accessibility, tenant sub-metering contracts, and operator workload drive overt abandonment and covert malfunction.
* **Feedforward Integration in Pre-Design Appraisal**: Examine conceptual equivalents and adjacent frameworks that translate operational feedback into early-stage design constraints.

### 2.2 Large Language Models in Knowledge Extraction and Engineering Decision Support
* **LLMs in Structured Evidence Extraction and Qualitative Coding**: Review applications of LLMs in PRISMA screening, building code parsing, concept extraction, and inductive grounded theory coding, clarifying their utility as candidate knowledge organisers rather than autonomous decision-makers.
* **Hallucination, Correlated Errors, and Human-Centred AI Oversight**: Examine evidence on LLM failure modes—including omission, over-generalisation, context loss, output instability, and correlated errors across models sharing training data—alongside human-in-the-loop and human-centred AI governance principles.

### 2.3 Multi-Criteria Decision-Making (MCDM) in Building Retrofit Evaluation
* **Trade-Offs and Criteria Formation Transparency in Retrofit MCDM**: Review how MCDM frameworks structure conflicting technical, economic, and operational trade-offs in building retrofits, scrutinising how evaluation criteria are sourced, selected, and justified prior to weighting.
* **Consensus Screening and Expert Independence**: Examine the role of Fuzzy Delphi Method (FDM) screening in refining candidate constructs and compare single-panel versus independent multi-panel governance in mitigating anchoring bias and Goodhart-type superficial compliance.

### 2.4 Full Consistency Method
* **Comparative Judgement Structure and Consistency Control**: Focus directly on how FUCOM structures subjective criteria weighting through ordinal ranking and $n-1$ adjacent pairwise ratios under multiplicative transitivity constraints (contrasted structurally with the $n(n-1)/2$ comparisons in AHP and $2n-3$ comparisons in BWM), rather than recounting method history.
* **Hierarchical Weighting in Engineering Appraisal**: Review how FUCOM derives local and global weights across multi-level criteria hierarchies while quantifying deviation from full consistency ($\chi$).

### 2.5 CoCoSo
* **Compromise Aggregation Mechanics**: Focus directly on how CoCoSo integrates weighted sum and weighted product comparability sequences via three compromise appraisal score strategies to balance arithmetic and relative utility without distortion from extreme single-criterion values.
* **Comparative Prioritisation and Multi-Method Benchmarking**: Review how CoCoSo supports comparative prioritisation of non-mutually-exclusive design alternatives alongside sensitivity testing and rank-correlation benchmarking.

### 2.6 Summary
* Synthesise the critical conclusions across `2.1` to `2.5` (identifying which premises are supported, conditionally supported, or unresolved in existing literature) and establish the evidential justification for the proposed research tasks, concluding without forward section previews.

---

## 3. Proposed Framework and Methodology: The Auditable Decoupled Decision-Support System

### 3.1 Overview of the Research Framework
* **Architectural Logic and Role Boundaries**: Explain how the framework separates automated candidate knowledge elicitation from human evaluative authority across four sequential phases encompassing ten operational steps:
  * *Phase 1 — AI-Augmented Knowledge Elicitation and Inductive Coding*: Dual-track PRISMA 2020 searching (academic literature and building standards), parallel screening and verbatim evidence extraction by three heterogeneous LLMs (GPT, Gemini, and Claude), stratified manual error auditing, relevance arbitration, and LLM-assisted inductive grounded coding of documentary records and field interviews to construct an initial candidate hierarchy (main criteria, sub-criteria, and bundled strategic design pathways). Models assign no weights, performance scores, or rankings.
  * *Phase 2 — Expert-in-the-Loop Consensus Screening*: Independent multi-disciplinary panellists audit wording, anchor operational definitions to verifiable pre-design deliverables, and screen candidate items through a two-round single-TFN Fuzzy Delphi Method (FDM) to establish the validated Evaluation Index System (EIS).
  * *Phase 3 — Computational Strategic Appraisal*: A separate independent expert panel derives main-criterion and global sub-criterion weights via FUCOM, after which another independent panel—blinded to criterion weights—evaluates bundled Strategic Design Pathways (SDPs) on a crisp scale for comparative prioritisation via CoCoSo.
  * *Phase 4 — Robustness and Comparative Validation*: One-at-a-time weight perturbation sensitivity analysis and cross-method rank comparison (against MARCOS, TOPSIS, and VIKOR using Spearman's rank correlation $\rho$ and Kendall's $\tau$) verify ranking stability, accompanied by complete evidence-traceability logs.
* **Governance Principle**: Enforce strict operational separation between generative LLMs and human evaluators, alongside strict sample independence across four separately recruited expert panels ($\text{Panel A} \cap \text{Panel B} \cap \text{Panel C} \cap \text{Panel D} = \emptyset$).
* **Table 1**: *Sequential Methodological Architecture of the Auditable Decoupled Decision-Support System* (Columns: `Framework Phase`, `Methodological Engine`, `Primary Epistemic Function`, `Decision Agent & Role Boundary`; no Note).
* **Fig. 1**: *Overall research process and operational role boundaries* (no Note).

### 3.2 Two-Round Single-TFN Fuzzy Delphi Method (FDM) Protocol
* **Fuzzy Representation and Parameter Definitions**: Ground single-TFN elicitation in fuzzy set theory [1–3], defining each individual triangular fuzzy number $\tilde{A}_{ij} = (l_{ij}, m_{ij}, u_{ij})$ under $0 \le l_{ij} \le m_{ij} \le u_{ij} \le 1$, and compiling all mathematical symbols in **Table 2** (*Mathematical notation and parameter definitions for the single-TFN FDM protocol*; no Note).
* **Step 1 — Prespecified linguistic scale and fuzzy mapping**: Define the five-level linguistic scale (`Very Low` to `Very High`) and corresponding predefined TFNs on $[0, 1]$ (**Table 3**; no Note).
* **Step 2 — Component-wise group aggregation and operator rationale**: Compute group TFNs $\tilde{A}_j = (l_j, m_j, u_j)$ via component-wise arithmetic mean, explaining why geometric aggregation is unsuitable due to the zero-product property triggered by zero lower/modal vertices in `Very Low` $(0.00, 0.00, 0.25)$.
* **Step 3 — Vertex-distance consensus testing mechanics and threshold interpretation**: Compute Euclidean vertex distance $d(\tilde{A}_{ij}, \tilde{A}_j)$ [4], applying proximity threshold $d \le 0.20$ and item-level consensus rate $CR_j \ge 0.75$, while requiring disclosure of full five-category response distributions to avoid masking polarised ratings.
* **Step 4 — Weighted defuzzification and scale transformation**: Compute crisp importance $S_j = (l_j + 4m_j + u_j)/6$ and linear 0–10 score $A_j = 10S_j$, applying the a priori importance threshold $S_j \ge 0.70$ ($A_j \ge 7.00$).
* **Step 5 — Dual-threshold decision rules, stopping protocol, and subgroup consensus retention**: Formalise Round 1 retention ($CR_j \ge 0.75$ and $S_j \ge 0.70$), immediate elimination ($S_j < 0.70$), and Round 2 re-evaluation ($S_j \ge 0.70$ and $CR_j < 0.75$), plus subgroup consensus retention for field-emergent operational indicators that achieve consensus within the facility-operations expert subgroup despite borderline overall consensus. Define the two-round stopping rule under which unresolved items after Round 2 are excluded.
* **Step 6 — Audit logging, controlled feedback, and interpretation boundaries**: Specify structured revision logging, the six-element anonymised Round 2 controlled feedback package, non-pooling of Round 1 and Round 2 ratings, and the interpretation of retained outputs strictly as an expert-screened decision set.

### 3.3 Full Consistency Method (FUCOM)
* **Parsimonious Elicitation Structure**: Specify FUCOM [5] for deriving subjective weights across hierarchical criterion groups using $n-1$ adjacent comparisons after ordinal ranking, explaining its consistency control relative to full pairwise matrices [6, 7].
* **Step 1 — Criterion ordering**: Rank criteria within each group from highest to lowest stated importance ($C_{j(1)} \succeq C_{j(2)} \succeq \dots \succeq C_{j(n)}$).
* **Step 2 — Comparative priority elicitation**: Elicit finite positive adjacent importance ratios $\varphi_{k/(k+1)} \ge 1$.
* **Step 3 — Weight estimation and deviation minimisation**: Formulate the constrained non-linear optimisation model minimising maximum absolute deviation $\chi$ subject to adjacent ratio reproduction, multiplicative transitivity ($w_{j(k)}/w_{j(k+2)} = \varphi_{k/(k+1)} \otimes \varphi_{(k+1)/(k+2)}$), unit-sum, and strict positivity constraints; clarify that $\chi = 0$ establishes algebraic agreement with elicited ratios rather than substantive validity.
* **Step 4 — Group aggregation**: Combine individual expert weight vectors via normalised geometric mean to preserve multiplicative ratio-scale invariance [8, 9].
* **Step 5 — Hierarchical weight aggregation**: Multiply each main-criterion group weight by its subordinate sub-criterion local weight to obtain global weights summing to unity, applying only global sub-criterion weights in pathway appraisal to prevent double counting.

### 3.4 Combined Compromise Solution (CoCoSo)
* **Compromise Prioritisation Logic**: Specify CoCoSo [10] for comparative prioritisation of bundled SDPs under blinded performance ratings, integrating weighted comparability sum ($S_i$) and power-weighted comparability sum ($P_i$) without LLM involvement.
* **Step 1 — Initial decision matrix construction**: Construct the $m \times n$ performance matrix $X = [x_{ij}]_{m \times n}$ across $m$ bundled SDPs and $n$ final sub-criteria.
* **Step 2 — Compromise normalisation**: Normalise benefit and cost criteria onto $[0, 1]$ using linear min–max scaling to obtain $R = [r_{ij}]_{m \times n}$.
* **Step 3 — Weighted comparability sequences ($S_i$ and $P_i$)**: Inject FUCOM global weights $w_j^{\text{global}}$ to compute $S_i = \sum_{j=1}^n w_j^{\text{global}} r_{ij}$ and $P_i = \sum_{j=1}^n (r_{ij})^{w_j^{\text{global}}}$.
* **Step 4 — Appraisal score aggregation and strategy prioritisation**: Compute arithmetic-mean ($k_{ia}$), relative-ratio ($k_{ib}$), and balanced-compromise ($k_{ic}$, with $\lambda = 0.5$) appraisal scores, synthesising the final compromise utility index $k_i = (k_{ia} k_{ib} k_{ic})^{1/3} + \frac{1}{3}(k_{ia} + k_{ib} + k_{ic})$ for descending comparative prioritisation.

### 3.5 Evidence Verification, Multi-LLM Auditability, and Knowledge Traceability
* **Human-Centred Governance and Verbatim Source Binding**: Ground role boundaries in human-centred AI principles [11]; require every extracted candidate construct to carry a unique source identifier and verbatim supporting text span, rejecting fluent wording or inter-model agreement alone as evidential proof [12].
* **Stratified Manual Error Auditing and Arbitration Protocol**: Mandate stratified random manual verification across all four multi-LLM voting strata (unanimous inclusion, majority inclusion, majority exclusion, unanimous exclusion) to quantify correlated false-positive and false-negative rates, paired with backward/forward snowballing and rule-based arbitration logging.
* **Inductive Coding Audit and Deliverable-Anchored Definitions**: Require codebook verification, inter-coder agreement testing (Cohen's $\kappa > 0.75$), and participant member checking for field interviews; require all EIS operational definitions to anchor to verifiable pre-design technical deliverables rather than aspirational promises.
* **Disposition Logging and Upstream Scope Disclosure**: Maintain a structured disposition log (`Accepted`, `Rejected`, `Revised`, `Merged`, `Added`) linking every item from raw extraction to final EIS inclusion, while explicitly disclosing that corpus selection and prompt design bound candidate coverage without claiming exhaustiveness.

---

## 4. Empirical Case Study

* **Unnumbered Lead-in (Structure & Panel Recruitment)**
  * *Empirical Context*: Introduce the application of the proposed decision-support framework to appraise strategic design pathways for smart energy retrofitting of existing commercial office buildings in China.
  * *Transition to Expert Qualifications*: Explain why evaluating operational-feedforward criteria and bundled retrofit pathways requires integrated expertise spanning building services engineering, front-line commercial property operation, decision science, and retrofit policy governance.
  * *Concrete Eligibility & Exclusion Rules (**Table 4**)*: Require at least ten consecutive years of relevant professional experience and fulfilment of at least two of four concrete domain qualifications (C1 Building MEP and smart control engineering practice; C2 Commercial building facility operations and energy management; C3 Academic expertise in sustainable building design or MCDM; C4 Building energy codes, green building standards, or urban renewal governance), directly specifying concrete requirements without vague placeholders. Exclude individuals limited to pure sales, administration, or new-build projects without retrofit or operational engagement.
  * *Independent Multi-Panel Allocation (**Table 5**)*: Detail the separate, independent recruitment of the Principal Arbitrator ($N = 1$), Panel A (field interview panellists), Panel B (two-round FDM panellists, $N = 20$), Panel C (FUCOM weighting panellists, $N = 10$), and Panel D (CoCoSo pathway appraisal panellists, $N = 10$), verifying zero overlap ($\text{Panel A} \cap \text{Panel B} \cap \text{Panel C} \cap \text{Panel D} = \emptyset$) and zero replacement across FDM rounds.
  * *Subsection Roadmap*: Briefly introduce the sequence of `4.1` through `4.5`.

### 4.1 AI-Augmented Knowledge Elicitation and Candidate Corpus Formation
* **Stage 1 — Dual-track searching and deduplication**: Report parallel systematic searches following PRISMA 2020 [13, 14] across **Track 1** (Web of Science Core Collection streams A1–A3 covering retrofit performance gaps, smart BAS/HVAC control retrofitting, and handover/facility operations) and **Track 2** (building retrofit and smart-readiness standards across five jurisdictions: China, the European Union, the United States, Singapore, and Taiwan), described with equal procedural detail, search coverage periods, and deduplication counts (**Table 6**, **Table 7**; no specific collection calendar dates).
* **Stage 2 — Multi-model relevance scoring and verbatim extraction**: Report isolated parallel screening by three heterogeneous LLMs using a shared five-point relevance rubric (**Table 8**) and verbatim evidence-span extraction, summarising model-level rating distributions and agreement splits (**Table 9**).
* **Stage 3 — Stratified manual audit, relevance arbitration, and final candidate corpus**: Report correlated false-positive and false-negative rates from stratified random manual auditing across all four voting strata, backward/forward snowballing additions, Principal Arbitrator rulings on score-range divergences ($\Delta \ge 3$), and final corpus reconciliation (**Table 10**).

### 4.2 Inductive Grounded Theory Coding Protocol and Theoretical Saturation Analysis
* **Stage 1 — Cross-source inductive coding and inter-coder audit**: Report open, axial, and selective coding [15] conducted with Claude assistance across the retained Track 1 literature, Track 2 standards, and Panel A semi-structured facility-management interview transcripts (strictly in English with zero non-English illustrative text), alongside inter-coder agreement (Cohen's $\kappa > 0.75$) and Panel A member checking.
* **Stage 2 — Code accumulation and theoretical saturation analysis**: Report code accumulation across 300 random corpus orderings and split-half comparisons to examine code saturation, explicitly distinguishing code saturation from meaning saturation [16].
* **Stage 3 — Candidate taxonomy, source traceability, and initial strategic design pathways**: Present the candidate main categories, sub-criteria, and source-traceability counts across WoS literature, five-jurisdiction standards, and Panel A interviews (**Table 11**), together with initial candidate strategic design pathways linked to open codes (**Table 12**).

### 4.3 Two-Round Normalised Fuzzy Delphi Method (FDM)
* **Stage 1 — Round 1 evaluation results and operational-subgroup retention**: Report Round 1 consensus rates ($CR_j \ge 0.75$) and defuzzified importance scores ($S_j \ge 0.70$, $A_j \ge 7.00$) from Panel B ($N = 20$) across all candidate main criteria (**Table 13**) and sub-criteria (**Table 14**; clear `Round 1` / `Round 2` grouped headers, no `Mean Score` column), detailing how subgroup consensus retention preserved critical field-emergent operational indicators for Round 2 reassessment.
* **Stage 2 — Round 2 consensus re-evaluation and deliverable-anchored refinement**: Report Round 2 standalone calculations and wording clarifications anchored to verifiable pre-design technical deliverables (**Table 15**), clearly separating statistical screening outcomes from editorial scope refinements and excluding unresolved Round 2 items without mentioning any third round.
* **Stage 3 — Strategic alternatives screening and pathway bundling**: Report two-round screening of candidate pathways (**Table 16**, **Table 17**), explaining how the majority of experts identified load-offset and hydraulic-control interdependencies and consolidated complementary interventions into bundled Strategic Design Pathways (SDPs).
* **Stage 4 — Final operational-feedforward Evaluation Index System**: Directly state the final counts of main criteria, sub-criteria, and bundled SDPs, introducing **Table 18** and **Table 19** with standalone, self-contained operational definitions (never defining one code via another code) and the `Literature Saturation` column.

### 4.4 Deriving Criteria Weights Using FUCOM
* **Independent Elicitation and Consistency Verification**: Report Panel C ($N = 10$) ordinal rankings and adjacent comparison ratios across main and sub-criterion groups (**Table 20**), individual optimisation solutions verifying $\text{DFC } (\chi^*) = 0.0000$ (**Table 21**), and geometric-mean group main weights, local weights, and global weights (**Table 22**).

### 4.5 Appraising Strategic Design Pathways Using CoCoSo
* **Blinded Appraisal and Compromise Utility Computation**: Report Panel D ($N = 10$, blinded to FUCOM weights) 1–9 performance ratings forming the initial decision matrix $X$ (**Table 23**), compromise normalised matrix $N$ (**Table 24**), weighted comparability sequences $S_i$ and $P_i$ (**Table 25**), and the three appraisal score components $k_{ia}$, $k_{ib}$, and $k_{ic}$ (**Table 26**).

---

## 5. Research Results

### 5.1 The FUCOM Model
* **Main-Criterion Group Weights (`Fig. 2`)**: Present the ranking of main-criterion group weights derived from Panel C, highlighting the relative weight concentration in operational-feedforward and legacy-system compatibility domains compared with static hardware metrics.
* **Sub-Criterion Global Weights (`Fig. 3`)**: Present the complete global weight ranking across all final sub-criteria, detailing the top-ranked operational-feedforward indicators and the descending weight gradient across the remaining criteria.

### 5.2 The CoCoSo Model
* **Final Compromise Utility Values and Strategy Ranking (`Table 27`, `Fig. 4`)**: Present the aggregated utility values and final CoCoSo compromise utility index $k_i$ for all bundled SDPs (**Table 27**) and plot their comparative prioritisation from highest to lowest (**Fig. 4**), interpreting the engineering rationale behind top-ranked integrated pathways versus lower-ranked standalone digital modules.

---

## 6. Validation and Implication

### 6.1 Sensitivity Analysis of Criteria Weights
* **One-at-a-Time Perturbation Design (54 Scenarios)**: Vary each of the three highest-weighted sub-criteria independently from $-90\%$ to $+90\%$ in $10\%$ increments (18 scenarios per target criterion; 54 scenarios total plus baseline), proportionally recalculating all remaining sub-criterion weights to preserve unit sum (**Table 28**).
* **Utility Trajectories and Rank Stability (`Tables 29–31`, `Figs. 5–7`)**: Report perturbed CoCoSo utility values (**Tables 29–31**) and rank trajectories (**Figs. 5–7**), evaluating rank stability against the baseline via Spearman's rank correlation coefficient ($\rho$).

### 6.2 Comparative Analysis with Other MCDM Methods
* **Cross-Model Rank Comparison (`Fig. 8`)**: Evaluate the identical FUCOM weights and Panel D performance matrix using MARCOS, TOPSIS, and VIKOR, comparing pathway rankings across all four methods (**Fig. 8**) and quantifying pairwise agreement via Spearman's $\rho$ and Kendall's $\tau$ (strictly excluding Pearson correlation).

### 6.3 Implications for Research
* **Methodological Implications**: Discuss how dual-track multi-LLM extraction, stratified manual error auditing, and independent multi-panel separation improve upstream criteria-formation transparency and prevent circularity in engineering MCDM studies.
* **Domain Theoretical Implications**: Discuss how the empirical weight distribution and pathway rankings challenge hardware-centric smart retrofit appraisal by demonstrating the primacy of legacy plant compatibility and operational human factors.

### 6.4 Implications for Management
* **Pre-Design Deliverable Gatekeeping (Architects & Design Teams)**: Recommend requiring verifiable pre-design diagnostic and control-architecture deliverables (e.g., measured hydraulic balancing reports and manual bypass schematics) during design-scheme selection to eliminate paper-only compliance.
* **Phased Investment Sequencing (Building Owners & Facility Managers)**: Recommend prioritising foundational hydraulic/plant rectification bundled with operator-friendly adaptive controls before layering advanced AI optimisation modules.
* **Retrofit Governance and Staged Subsidies (Policy Makers)**: Recommend archiving pre-design EIS scores as traceable structured baseline profiles paired with staged subsidy disbursements (retaining 30–40% of incentives until one-year post-handover verification of automated-mode retention, equipment cycling stability, and weather-normalised energy savings) and independent commissioning.

---

## 7. Conclusion and Limitations

* **Unnumbered Six-Paragraph Synthesis (No Subsections)**
  * *Paragraph 1*: Summarise the complete execution of the auditable decoupled framework across dual-track multi-LLM PRISMA screening, grounded coding, and four independent expert panels (Panel A interviews, Panel B two-round FDM, Panel C FUCOM weighting, and Panel D blinded CoCoSo appraisal).
  * *Paragraph 2*: Summarise the hierarchical weight concentration across main criteria and global sub-criteria.
  * *Paragraph 3*: Summarise the CoCoSo comparative prioritisation of bundled SDPs, emphasising that rankings represent conditional relative priorities rather than universal optimality or grounds to discard lower-ranked modules when integrated into broader packages.
  * *Paragraph 4*: Summarise the 54-scenario weight sensitivity analysis and cross-method rank agreement across CoCoSo, MARCOS, TOPSIS, and VIKOR within the tested bounds.
  * *Paragraph 5*: State five key limitations: (1) upstream corpus dependence on WoS and five selected jurisdictions; (2) inductive coding assisted by a single LLM without cross-model coding sensitivity comparisons; (3) purposively assembled Chinese commercial retrofit expert panels reflecting regional institutional contexts; (4) one-at-a-time weight perturbation holding performance ratings fixed, alongside unmodelled construction-phase execution gaps; and (5) focus on pre-design internal validity without post-occupancy longitudinal operational measurements.
  * *Paragraph 6*: Outline future research directions: cross-regional and cross-sector replication with multi-model coding comparisons, simultaneous Monte Carlo parameter perturbation, and longitudinal pairing of pre-design EIS baseline profiles with one-year post-handover operational proxy metrics.