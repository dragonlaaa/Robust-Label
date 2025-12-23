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
- **Characteristics:** The subset  including DoS/DDoS, MITM, and ReconHostDiscovery. Stratified sampling was applied to ensure each attack type is adequately represented.

6. LicenseThese subsets are derived from the original datasets provided by the Canadian Institute for Cybersecurity (CIC). Users should comply with the original licensing terms of the DoHBrw-2020 and CICIoT2023 datasets.
