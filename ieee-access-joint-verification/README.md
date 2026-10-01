# Question-Driven Joint Verification of Privacy and Utility — reproducibility artifact

The archive `artifact.zip` in this folder accompanies the IEEE Access submission "Question-Driven Joint Verification of Privacy and Utility" by S. Yang, P. Rivière and T. Aoki (JAIST). It contains every model, script and result the manuscript reports.

| Folder | What it reproduces |
|---|---|
| `icfem_scaling/` | Running example: the twelve-record Alloy model and Table "counterexamples per policy"; the coordinate-space pruning table |
| `alloy_experiments/` | Synthetic Small/Medium/Large Alloy sweeps (archived results and the 2026-10-01 rerun), sanity checks, every Small timing run, the record-count probe (including the 512-record heap test), and the Adult-128/256 Alloy sweeps |
| `scale/` | Full UCI Adult experiments with the direct evaluator: nested questions, record sweep, policy-space growth (2,430–87,480 policies), extended quasi-identifier, data-dependent questions, seeded defects (evaluator side) and metric optima |
| `validation/` | Bounded Alloy checks of the structural results, seeded-defect specifications with Alloy counterexamples, randomized Alloy–evaluator differential testing |
| `symbolic_utility.als`, `CheckIllustration.java` | Symbolic utility module and its checks |

## Requirements
- Alloy 6.1.0 (`org.alloytools.alloy.dist.jar`, https://alloytools.org). Set `ALLOY_JAR` to its path.
- Java 11 or later.
- Python 3.9 or later with numpy and pandas.

## Data
The UCI Adult training file `adult.data` (https://archive.ics.uci.edu/dataset/2/adult, CC BY 4.0) is not redistributed here. Download it. The copy used for the manuscript has SHA-256 `df25a4e32ed6f1bd4b3910d21a7bd661a09061eced7cb45555a519d9667cc87b`; the UCI download may differ from it only by trailing blank lines, which do not change any result. Rows with missing values are dropped, leaving 30,162 records.

Download `artifact.zip` and unzip it. Each subfolder's README lists its exact commands.

SHA-256 of `artifact.zip`: 7920a99df05a248801b4a6f51e3f65a638bc32b0c58027576dab6dfc854889f1
