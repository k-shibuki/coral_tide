# CORAL/TIDE Framework Evaluation Dataset

[![DOI](https://zenodo.org/badge/989682983.svg)](https://doi.org/10.5281/zenodo.15505315)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Overview

This repository contains the complete dataset, protocols, and research materials for evaluating the **CORAL (Cell-based Organized Reasoning with Adaptive Linkage)** framework—an approach for structuring individual cognitive processes as AI reasoning processes.

CORAL enables users to structure and verbalize their personal thinking processes, implementing them as AI agent reasoning processes through natural language. This research demonstrates the feasibility and effectiveness of this approach through rigorous quantitative evaluation.

## Research Summary

### The Problem

Current human-AI collaboration approaches treat AI as external tools, failing to reflect users' expertise and cognitive processes in AI reasoning. This structural limitation restricts collaboration to generic interactions.

### The Approach

CORAL proposes structuring individual thinking processes and implementing them as AI reasoning processes through:

- **Cell Architecture**: Dividing complex custom instructions into manageable functional units (Cells) with explicit input-output design
- **TIDE Protocol**: Transition with Inherited Discourse Exchange—a 6-perspective framework for semantic context inheritance between Cells
- **S-OPE Configuration**: A proof-of-concept implementation (Sensemaker-Orchestrator-Planner-Executor)

### Key Findings

The controlled evaluation study (N=36, 4 conditions) demonstrated:

- **Statistical Significance**: S-OPE configuration showed significantly higher scores than all comparison conditions (FDR-adjusted p < 0.001, effect size r > 0.8)
- **Integration Effect**: Combined effect exceeded the sum of individual component effects
- **Qualitative Superiority**: Only the Test condition achieved "Outstanding" (5-point) evaluations

## Repository Structure

```
coral_tide/
├── data/
│   ├── raw/           # Raw experimental data (chat logs, reports)
│   └── src/           # Processed data for statistical analysis
├── docs/
│   ├── protocol/      # Pre-registered evaluation protocols (PDF)
│   └── tasks/         # Task definition files
├── rules/
│   ├── test/          # S-OPE Configuration (Japanese original)
│   ├── control/       # Integrated Custom Instruction (Japanese)
│   ├── a-s/           # Ablation-S: S-OPE without Sensemaker
│   ├── a-h/           # Ablation-H: S-OPE without TIDE context
│   ├── en/            # English translations (for international readers)
│   └── scoring_agents/ # AI scoring agent with rubrics
├── rules_archive/     # Historical versions of custom instructions
├── LICENCE            # CC BY 4.0
└── README.md
```

## Research Protocol

The evaluation protocol was pre-registered before data collection:

- **[Protocol ver.1.1 (2025-08-25)](docs/protocol/protocol_ver.1.1_250825.pdf)** — Current version with task2 discontinuation note
- **[Protocol ver.1.0 (2025-05-24)](docs/protocol/protocol_ver.1.0_250524.pdf)** — Original pre-registered version

## Experimental Conditions

| Condition | Description |
|-----------|-------------|
| **Test** | S-OPE Configuration (Full CORAL implementation) |
| **Control** | Integrated Custom Instruction (CoT + ReAct + Self-reflection) |
| **Ablation-S** | S-OPE without Sensemaker Cell |
| **Ablation-H** | S-OPE without TIDE context inheritance definitions |

## Language Note

All custom instructions were implemented in Japanese, as this is the developer's native language and the medium through which their thinking processes were formed. English translations are provided in `rules/en/` for international readers, though these are machine-translated reference materials.

## Citation

If you use this dataset or materials in your research, please cite:

```bibtex
@dataset{shibuki_coral_tide_2025,
  author       = {Shibuki, Katsuya},
  title        = {{CORAL/TIDE Framework Evaluation Dataset}},
  year         = {2025},
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.15505315},
  url          = {https://doi.org/10.5281/zenodo.15505315}
}
```

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to:
- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material for any purpose, even commercially

Under the following terms:
- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made.

## Author

**Katsuya Shibuki**  
Independent Researcher, Tokyo, Japan  
[![ORCID](https://img.shields.io/badge/ORCID-0000--0003--3570--5038-green)](https://orcid.org/0000-0003-3570-5038)

## Related Resources

- Paper: *CORAL: A Framework for Structuring Individual Cognitive Processes as AI Reasoning Processes* (in preparation)

---

*This study implements Open Science practices by publishing all data, custom instructions, and evaluation processes for transparency and reproducibility.*
