# Sampled Subsets for Malicious Traffic Detection under Noisy Labels

This repository contains the sampled subsets of the **DoHBrw-2020** and **CICIoT2023** datasets used in our research paper: *"Robust Label: A Robust Learning Framework for Malicious Traffic Detection under Noisy Conditions"*.

## 1. Overview
Due to the massive scale of the original datasets (exceeding 600GB in total), training deep learning models on the full sets is computationally prohibitive for multi-round noise-injection experiments. These subsets were constructed using **stratified random sampling** to:
- Maintain computational feasibility.
- Mitigate extreme class imbalance found in the original traffic.
- Ensure fair evaluation of the **Robust Label** framework.

## 2. Dataset Descriptions

### 2.1 DoHBrw-2020 (DNS-over-HTTPS)
- **Original Source:** [DoHBrw-2020 Dataset (UNB)](https://www.unb.ca/cic/datasets/dohbrw-2020.html)
- **Scenario Used:** `MaliciousDoH`
- **Sample Count:** 38,000
- **Characteristics:** This subset focuses on distinguishing between benign DoH traffic and malicious DoH activities (such as tunneling and data exfiltration) embedded within HTTPS-encrypted tunnels.

### 2.2 CICIoT2023 (IoT Intrusion Detection)
- **Original Source:** [CICIoT2023 Dataset (UNB)](https://www.unb.ca/cic/datasets/iotdataset-2023.html)
- **Sample Count:** 70,000
- **Characteristics:** The subset covers 34 traffic categories (33 types of attacks and 1 benign class) from modern IoT environments, including DoS/DDoS, port scanning, and device hijacking. Stratified sampling was applied to ensure each attack type is adequately represented.

## 3. Research Purpose
These datasets are specifically curated to evaluate the performance and robustness of the **Robust Label** framework. By introducing controlled label noise (ranging from 0.1 to 0.9), these subsets allow researchers to:
- Test the effectiveness of sample selection and label correction strategies.
- Verify the stability of noise injection methods like **S-IDN**.
- Facilitate the reproducibility of the experimental results presented in our paper.

## 4. File Structure
The data is provided in CSV format with pre-processed features (after normalization and encoding).
- `dohbrw_sampled_38k.csv`: Sampled DoHBrw-2020 dataset.
- `ciciot2023_sampled_70k.csv`: Sampled CICIoT2023 dataset.

## 5. Citation
If you use these subsets in your research, please cite our paper:
```bibtex
@article{yourcitation2025,
  title={Robust Label: A Robust Learning Framework for Malicious Traffic Detection under Noisy Conditions},
  author={Your Name, et al.},
  journal={The Computer Journal},
  year={2025}
}
6. LicenseThese subsets are derived from the original datasets provided by the Canadian Institute for Cybersecurity (CIC). Users should comply with the original licensing terms of the DoHBrw-2020 and CICIoT2023 datasets.
