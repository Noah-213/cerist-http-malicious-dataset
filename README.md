# CERIST HTTP Malicious Dataset & Processing Pipeline

This repository contains all the scripts, Jupyter notebooks, and intermediate/final datasets developed during the internship project: **"Analysis of Simulated Malicious HTTP Traffic at CERIST"**.

## 📄 Project Overview

This project aimed to:

* Extract, clean, and structure HTTP traffic from PCAP files simulating various web attacks (LFI, SQLi, XSS, SSTI, etc.).
* Build a transparent data pipeline from raw packet capture to a clean, analysis-ready dataset.
* Provide exploratory data analysis (EDA) and visualizations of the generated dataset.

> **Note:**  
> The provided notebooks/scripts reflect the **exact workflow and environment used during the internship**, including Google Colab and Google Drive file paths.  
> **To re-run any code, please adapt all file paths to your own environment (local, Colab, etc.).**  
> These notebooks are shared for transparency and documentation, not for direct out-of-the-box execution.

## 📁 Repository Structure

```
├── data/                                 # All generated intermediate and final datasets (PCAP, JSON, CSV, LOG)
├── figures/                              # Plots and figures generated during EDA
├── INTERNSHIP_REPORT_CERIST.pdf          # Final report: all methodology, results, figures, and discussion
├── README.md                             # This file
├── STEP1_Pcap_To_Json_Pyshark.ipynb      # Extraction of HTTP packets from PCAP (PyShark)
├── STEP2_Cleaning_Flattening_Json.ipynb  # Cleaning and flattening of raw JSON files
├── STEP3_Json_To_CSV.ipynb               # Conversion of JSON to flat CSV
├── STEP4_Combine_CSV.ipynb               # Combining all CSVs into a global dataset
├── STEP5_CSV_to_Apache_log.ipynb         # Generation of Apache-like log files
├── STEP6_Exploratory_Data_Analysis.ipynb  # EDA and data visualizations
├── requirements.txt                      # Key dependencies and Python packages
```


## 🚀 How to Use

- **Browse the notebooks (`.ipynb`):**  
  Each notebook shows the processing steps performed during the internship.  
  > **Paths and file locations correspond to Google Drive (Colab). Adapt as needed to run locally.**

- **Datasets:**  
  The most important artifact is the **final combined/shuffled CSV** (`data/combined_all_shuffled.csv`), ready for downstream use.

- **Dependencies:**   
  See `requirements.txt` for a full list.

## 📊 Dataset Description

* **Sources:** Simulated HTTP attack traffic extracted from PCAP files.
* **Attack types covered:** LFI, SQLi, SSTI, XSS, XML, CMD Injection, etc.
* **Main fields:** HTTP method, URL, headers, body, IPs, ports, timestamps, `attack_tag`.
* **No benign/background traffic included** (see report for limitations and possible extensions).

## 📚 Documentation

For detailed explanations, methodology, and figures, please refer to the final internship report (`INTERNSHIP_REPORT_CERIST.pdf`), or directly explore the notebooks.

## 💡 Citation

If you use this dataset or scripts for academic purposes, please cite:

```
Bennouar, T., & Hani, N. (2025). Analysis of Simulated Malicious HTTP Traffic at CERIST. Internship Report, CERIST.
[GitHub Repository](https://github.com/Noah-213/cerist-http-malicious-dataset)
```

## 📥 Contact

* [Tarek Bennouar](mailto:tarek.tb.pro@gmail.com)
* [Nour El Houda Hani](mailto:nourelhoudahani2002@gmail.com)

---

> **Disclaimer:** This repository is for research and educational purposes only. The generated datasets are synthetic and must not be considered as a direct representation of real-world network traffic.

---
