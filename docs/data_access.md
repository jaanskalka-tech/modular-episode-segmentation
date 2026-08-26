## Data access

The empirical evaluation uses two publicly available industrial datasets for complementary purposes: CNC production data for the structural cross-design case study and HAI 21.03 industrial-control data for the functional evaluation of alternative operating-context representations.

### CNC production data

The structural case study is based on the open *Series production data set for 5-axis CNC milling* published on Zenodo by Engelmann and Schmitt (2024) and described in the associated data paper by Schmitt and Engelmann (2024). The data were recorded on a HERMLE C600 U five-axis milling machine with a HEIDENHAIN iTNC 530 control system and cover thirteen real production series from a contract-manufacturing environment. Each series includes the setup changeover period and the subsequent production run and is stored as a separate CSV file.

**Original source:**

Engelmann, B., & Schmitt, A.-M. (2024). *Series production data set for 5-axis CNC milling*. Zenodo.
https://doi.org/10.5281/zenodo.10853254

For reproducibility, the downloaded CNC data are provided in this repository as `data.zip` in the `notebooks/` directory.

### HAI 21.03 industrial-control data

The functional evaluation uses the publicly available HAI 21.03 industrial-control security dataset. The experiment uses `train1.csv` as the sole normal-development run and `test1.csv`–`test5.csv` as held-out evaluation runs. All preprocessing parameters, segmentation models, SERF mappings, and empirical reference intervals are derived from `train1.csv`. Attack annotations from the test files are used only in the final external validation stage.

The HAI data are not redistributed in this repository. Download HAI 21.03 from the original dataset source and place the following files directly in the `notebooks/` directory, alongside `HAI_Functional_evaluation.ipynb`:

```text
train1.csv
test1.csv
test2.csv
test3.csv
test4.csv
test5.csv
```

**Original source:**

HAI Security Dataset repository:
https://github.com/icsdataset/hai

Shin, H.-K., Lee, W., Yun, J.-H., & Min, B.-G. (2021). *Two ICS Security Datasets and Anomaly Detection Contest on the HIL-Based Augmented ICS Testbed*. CSET '21, 36–40.
https://doi.org/10.1145/3474718.3474719
