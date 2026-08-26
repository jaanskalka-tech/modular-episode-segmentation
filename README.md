# Segmentation-based Episodic Representation Framework

Reproducibility repository for the manuscript **A Segmentation-based Episodic Representation Framework for Cross-Design Comparison in Multi-Mode Industrial Time Series**.

## Repository structure

```text
.
└── notebooks/
    ├── Episodic_framework_case_study.ipynb
    ├── HAI_Functional_evaluation.ipynb
    └── data.zip
```

## Contents

The repository contains two complementary Jupyter notebooks used in the empirical evaluation of the framework.

`Episodic_framework_case_study.ipynb` contains the main structural case study based on CNC production data. It demonstrates the complete SERF workflow, including shared state construction, alternative segmentation designs, episodic standardization, boundary stabilization, meta-mode alignment, and cross-design structural evaluation.

`HAI_Functional_evaluation.ipynb` contains the complementary functional evaluation on the HAI 21.03 industrial-control dataset. It examines how alternative SERF-derived operating-context representations affect the assessment of the same process responses under fixed empirical reference and multichannel-extremeness rules.

The CNC input data are provided in `data.zip` in the `notebooks/` folder. The HAI 21.03 data are obtained separately from the original public dataset source.

## Usage

### CNC structural case study

1. Open `Episodic_framework_case_study.ipynb` in the `notebooks/` folder.
2. Make sure that `data.zip` is present in the same folder as the notebook.
3. Run the notebook cells in sequence from top to bottom.

### HAI functional evaluation

1. Download the HAI 21.03 dataset from the original HAI repository.
2. Place the following files directly in the same working directory as `HAI_Functional_evaluation.ipynb`:

```text
train1.csv
test1.csv
test2.csv
test3.csv
test4.csv
test5.csv
```

3. Open `HAI_Functional_evaluation.ipynb`.
4. Run the notebook cells in sequence from top to bottom.

The HAI notebook creates all derived files under its local `outputs/` directory. No precomputed intermediate files or machine-specific paths are required.

## Data notes

### CNC production data

The structural case study uses the open **Series production data set for 5-axis CNC milling** published on Zenodo by Engelmann and Schmitt (2024). In this repository, the required data archive is stored directly in the `notebooks/` folder in zipped format.

**Original data source:**

Engelmann, B., & Schmitt, A.-M. (2024). *Series production data set for 5-axis CNC milling*. Zenodo.
https://doi.org/10.5281/zenodo.10853254

### HAI 21.03 industrial-control data

The functional evaluation uses **HAI 21.03**, a publicly available Hardware-In-the-Loop based industrial control-system security dataset. The dataset contains multivariate process and control measurements collected from a coupled industrial-control testbed during normal operation and experimentally introduced attacks.

The complete HAI 21.03 release contains three normal training files and five labeled attack-test files. The functional evaluation in this repository deliberately uses only `train1.csv` for all data-dependent development and reference estimation. The five files `test1.csv`–`test5.csv` are treated as held-out evaluation runs.

All preprocessing parameters, segmentation models, retained state definitions, boundary-stabilization settings, meta-mode mappings, and empirical response-reference intervals are derived from `train1.csv` before the test runs are processed. Attack annotations are excluded from these stages and are introduced only after label-independent multichannel-extremeness sequences have been constructed, for external functional validation.

This protocol allows the notebook to compare the functional consequences of alternative operating-context representations while holding the development data, response variables, and extremeness procedure fixed.

**Original HAI data source:**

HAI Security Dataset repository:
https://github.com/icsdataset/hai

**Reference for HAI 21.03:**

Shin, H.-K., Lee, W., Yun, J.-H., & Min, B.-G. (2021). *Two ICS Security Datasets and Anomaly Detection Contest on the HIL-Based Augmented ICS Testbed*. Cyber Security Experimentation and Test Workshop (CSET '21), 36–40.
https://doi.org/10.1145/3474718.3474719

## Original framework source

in pub-process
