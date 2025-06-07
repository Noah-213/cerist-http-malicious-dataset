# CERIST HTTP Malicious Dataset & Processing Pipeline

This repository contains all the scripts, Jupyter notebooks, and intermediate/final datasets developed during the internship project: **"Analysis of Simulated Malicious HTTP Traffic at CERIST"**.

## 📄 Project Overview

This project aims to:

* Extract, clean, and structure HTTP traffic from PCAP files simulating various web attacks (LFI, SQLi, XSS, SSTI, etc.).
* Build a reproducible data pipeline from raw packet capture to a clean, analysis-ready dataset.
* Provide exploratory data analysis (EDA) and visualizations of the generated dataset.
* Enable reproducibility and future extension for research or production use.

## 📁 Repository Structure

```
├── STEP1_Pcap_To_Json_Pyshark.ipynb      # Extraction of HTTP packets from PCAP (PyShark)
├── STEP2_Cleaning_Flattening_Json.ipynb  # Cleaning and flattening of raw JSON files
├── STEP3_Json_To_CSV.ipynb               # Conversion of JSON to flat CSV
├── STEP4_Combine_CSV.ipynb               # Combining all CSVs into a global dataset
├── STEP5_CSV_to_Apache_log.ipynb         # Generation of Apache-like log files
├── STEP6_Exploratory_Data_Analysis.ipynb  # EDA and data visualizations
├── data/                                 # All generated intermediate and final datasets (JSON, CSV, LOG)
├── figures/                              # Plots and figures generated during EDA
├── README.md                             # This file
```

## 🚀 Quick Start

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Noah-213/cerist-http-malicious-dataset.git
   cd cerist-http-malicious-dataset
   ```

2. **Set up the environment:**

   * Recommended: Python 3.9+
   * Install requirements:

     ```bash
     pip install -r requirements.txt
     ```
   * Main libraries: `pyshark`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `jupyter`

3. **Run notebooks in order:**
   Open and execute each notebook (`STEP1_...` to `STEP6_...`) following the comments and instructions.

4. **Explore the results:**

   * See the `data/` folder for generated datasets.
   * See the `figures/` folder for all plots and visuals.

## 📊 Dataset Description

* **Sources:** Simulated HTTP attack traffic extracted from PCAP files.
* **Attack types covered:** LFI, SQLi, SSTI, XSS, XML, CMD Injection, etc.
* **Main fields:** HTTP method, URL, headers, body, IPs, ports, timestamps, attack\_tag.
* **No benign/background traffic included** (see report for limitations and how to extend with other datasets).

## 📚 Documentation

For detailed explanations, methodology, and figures, please refer to the final internship report (`rapport.pdf` if provided) or the notebooks themselves.

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
