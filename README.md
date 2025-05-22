# Resilient_Predictive_Maintenance
Official repository of the paper "Toward Resilient Predictive Maintenance" presented at BOSON workshop for AINA 2025 conference

# Toward Resilient Predictive Maintenance in Complex Industrial Processes

[![DOI](https://img.shields.io/badge/DOI-10.1007%2F978--3--031--87781--0__2-blue)](https://doi.org/10.1007/978-3-031-87781-0_2)  
[![Open in Colab]([https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1LmY0QvsebPMth4cCeg-pn6Pk_Tob4UfK7](https://colab.research.google.com/drive/1LmY0QvsebPMth4cCeg-pn6Pk_Tob4UfK?usp=sharing))

This repository accompanies the following publication:

> **Moccardi, A., Cirillo, E., Del Prete, A., Mashaallah, Z. (2025)**  
> *Toward Resilient Predictive Maintenance in Complex Industrial Processes*  
> In: Barolli, L. (ed) **Advanced Information Networking and Applications (AINA 2025)**  
> Lecture Notes on Data Engineering and Communications Technologies, vol 251. Springer, Cham.  
> [https://doi.org/10.1007/978-3-031-87781-0_2](https://doi.org/10.1007/978-3-031-87781-0_2)

---

## Overview

This repository presents the official implementation of a Resilient Predictive Maintenance (ResPdM) framework designed to address reliability in industrial processes under uncertain, noisy, and non-stationary conditions. By leveraging a diagnostic-based approach, survival models, and anomaly-aware adjustments, we propose a robust system for Remaining Useful Life (RUL) forecasting using the **N-CMAPSS dataset**.

---

## Key Contributions

- **Multivariate anomaly detection** using DBSCAN clustering
- **Kaplan-Meier survival modeling** with dynamic RUL clipping
- **Diagnostic-aware degradation modeling**
- **Robust BiLSTM RUL forecasting**
- **Custom evaluation metric (S-score)** emphasizing failure proximity penalties
- **Simulation of adversarial and drift conditions**

---

## Getting Started

### Requirements

- Python ≥ 3.8
- TensorFlow ≥ 2.x or PyTorch
- NumPy, Pandas, Scikit-learn
- Matplotlib, Seaborn



Dataset: N-CMAPSS
This study uses the second dataset in the NASA N-CMAPSS suite to simulate real-world turbofan engine degradation under multi-operational conditions.

Download from: https://www.nasa.gov/content/prognostics-center-of-excellence-data-set-repository

Unzip and place files under: ./data/


Google Colab
You can explore and execute the full pipeline via Google Colab:


Results
Model	MSE	MAE	RMSE	R²	S-score
BiLSTM	348.9	13.9	18.7	0.83	99,164
LSTM	393.2	15.4	19.8	0.81	116,150
GRU + Attn	412.8	15.3	20.3	0.80	108,551
TCN	380.8	14.4	19.5	0.81	136,669

Highlights:

+3% improvement in R²

-17.5% reduction in S-score (early failure penalty)

Robust detection of drift and operational anomalies

Citation
If you find this repository useful in your research, please cite:
```
@inproceedings{moccardi2025resilient,
  title={Toward Resilient Predictive Maintenance in Complex Industrial Processes},
  author={Moccardi, Alberto and Cirillo, Egidia and Del Prete, Alessandro and Mashaallah, Zahida},
  booktitle={Advanced Information Networking and Applications (AINA)},
  series={Lecture Notes on Data Engineering and Communications Technologies},
  volume={251},
  year={2025},
  publisher={Springer},
  doi={10.1007/978-3-031-87781-0_2}
}
```
License
This code is licensed under the MIT License. See the LICENSE file for full details.

Acknowledgements
This research was supported by PNRR MUR Project PE0000013-FAIR, an initiative committed to promoting ethical, sustainable, and advanced AI systems for industrial applications.
