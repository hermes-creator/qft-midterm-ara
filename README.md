# QFT Midterm Agent-Native Research Artifact (`ara/`)

This repository contains the complete research, analytical derivations, calculations, and traceability ledgers for the **QFT Midterm Project** on real scalar $\phi^4$ theory renormalization and critical phenomena (covering Parts 1 & 2), structured in accordance with the Agent-Native Research Artifact (ARA) framework.

---

## Repository Structure & File Guide

The project is organized under the `ara/` directory into distinct layers separating problem requirements, physical claims, experimental execution records, exploration traces, equation anchors, and computational evidence:

```text
ara/
├── README.md                          # This user guide
├── source/
│   └── assignment-requirements.md     # Mapping of every requirement from FeynCalc_Midterm_Project.pdf
├── logic/
│   ├── claims.md                      # Detailed mathematical and physical derivations for 1.1–2.3
│   └── experiments.md                 # Execution logs, methods, and results for all subparts
├── src/
│   └── environment.md                 # Verified software environment details (Mathematica, FeynCalc, etc.)
├── trace/
│   └── exploration_tree.yaml          # Chronological workflow trace, decisions, and corrections
├── anchor/
│   └── equation-map.md                # Global equation anchor mapping (A-01 to A-23) to Fields Notes & workbook
└── evidence/
    └── <subsection>/                  # Subsection output logs, generated figures, and tables
        ├── outputs/
        ├── figures/
        └── tables/
```

---

## How to Read and Use This Repository

1. **Start with the Requirements (`ara/source/assignment-requirements.md`):**
   - Read this file to see how every mathematical question from the detailed brief (`FeynCalc_Midterm_Project.pdf`) maps to specific subtasks, notebook sections, and verification statuses.

2. **Explore the Physics Derivations (`ara/logic/claims.md`):**
   - This ledger provides the complete step-by-step mathematical derivations, conventions (Euclidean signature, $d = 4-\epsilon$, $g = \frac{\lambda}{16\pi^2}$), intermediate algebra, and final closed-form results for subsections **1.1 through 2.3**.

3. **Check the Experiments and Code Execution (`ara/logic/experiments.md`):**
   - Reviews the computational methods, FeynArts/FeynCalc topologies, convolution formulas, and analytic cross-checks. All subparts are marked `EXECUTED`.

4. **Verify Equation Sources (`ara/anchor/equation-map.md`):**
   - Maps every key equation in the project (`A-01` to `A-23`) to its corresponding chapter, section, equation number, and page in the assigned *Fields Notes* text and the anchor Excel workbook.

5. **Trace the Research Workflow (`ara/trace/exploration_tree.yaml`):**
   - Tracks the chronological decisions, corrections (such as resolving Mathematica `Solve` product syntax), symmetry factor displays, and water critical-isotherm scaling formula expansions (`(P - P_c)/P_c \sim A \, \text{sgn}(\Delta\rho) |\Delta\rho/\rho_c|^\delta`).

---

