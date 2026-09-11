# Pro Tic Tac - Semiconductor AI & Machine Learning Toolbox 🚀

[![Platform](https://img.shields.io/badge/Platform-Pro_Tic_Tac-06b6d4?style=for-the-badge)](https://protictac.com)
[![Framework](https://img.shields.io/badge/Framework-Laravel_11-ff2d20?style=for-the-badge&logo=laravel)](https://laravel.com)
[![Engine](https://img.shields.io/badge/ML_Engine-XGBoost_%7C_SHAP-38bdf8?style=for-the-badge&logo=python)](https://github.com/dmlc/xgboost)
[![LLM Agent](https://img.shields.io/badge/AI_Agent-Gemini_3.6_Flash-8e44ad?style=for-the-badge&logo=google)](https://ai.google.dev)
[![Status](https://img.shields.io/badge/Status-Live-emerald?style=for-the-badge)](https://protictac.com/yield/upload)

> **Pro Tic Tac** is an industrial-grade cloud analytics platform built for semiconductor engineers, yield enhancement (YE) teams, and fab process controllers. It seamlessly combines advanced machine learning algorithms with automated generative AI diagnostics to accelerate yield anomaly attribution and root cause analysis (RCA).

🔗 **Live Production System:** [https://protictac.com](https://protictac.com)  
🧪 **Interactive Live Demo:** [https://protictac.com/yield/upload](https://protictac.com/yield/upload)

---

## 🛠️ Machine Learning Toolbox Architecture

The toolbox is structured into modular machine learning suites designed to handle wafer acceptance test (WAT) metrics, circuit probe (CP) parameters, and inline process metrology:

```text
[ Wafer / WAT / CP Dataset (.xlsx, .csv) ]
                                          |
                                          v
                          +-------------------------------+
                          |   Laravel 11 Cloud Pipeline   |
                          +-------------------------------+
                                          |
                                          v
                          +-------------------------------+
                          |    Python 3.12 ML Subprocess  |
                          +-------------------------------+
                                          |
           +------------------------------+------------------------------+
           |                              |                              |
           v                              v                              v
[ Module 1: XGBoost ]          [ Module 2: SVM / RF ]          [ Module 3: SPC / Trend ]
Yield Anomaly Classifier           (Under Development)              (Under Development)
|
v
[ SHAP Feature Importance ]
|
v
[ Gemini 3.6 Flash Agent ]
|
v
[ Interactive Dashboard ]

📦 Module 1: XGBoost & SHAP Yield Diagnostics (Active)
The XGBoost Yield Classifier analyzes multi-dimensional wafer fabrication parameters to predict functional yield failure (OK vs NG) and leverages SHAP (SHapley Additive exPlanations) to pinpoint exact physical process root causes.

🌟 Key Performance Metrics
Dataset Volume: 3,000 samples (28nm FEOL WAT/CP model)

Optimization Method: Automated Scikit-Learn GridSearchCV

Test ROC-AUC: 0.9861 (Exceptional discrimination capability)

Test Accuracy: 93.67%

Top Defect Driver Identified: vt_p (PMOS Threshold Voltage, Mean |SHAP| = 1.8618)

🖼️ User Interface & Diagnostic Dashboard
The system provides fully automated, real-time diagnostic reporting supported in both English and Traditional Chinese (i18n).

1. English Mode ShowcaseDiagnostic Dashboard & MetricsSHAP Anomaly Parameters
Automated AI Diagnostic Summary (English)
Sample LLM Output Excerpt:
"SHAP feature attributions clearly identify vt_p (PMOS Threshold Voltage) as the primary root cause of yield loss, displaying a dominant Mean |SHAP| value of 1.8618—more than double the secondary driver, vt_n (0.8062). Physical process deviations point to PMOS Channel/Halo Implant Drift and High-k Metal Gate (HKMG) thickness non-uniformity."

2. Traditional Chinese Mode Showcase (繁體中文)繁中良率診斷 DashboardTop 5 SHAP 關鍵異常參數
Gemini AI 良率診斷報告 (繁體中文)
🛣️ Future Roadmap & Upcoming ML Tools
The Pro Tic Tac platform is continuously expanding to include more statistical and machine learning tools for fab yield enhancement:

[x] XGBoost & SHAP Automated Diagnostics (Released & Active)

[ ] SVM Classifier (Support Vector Machines) (Module 2 - Coming Soon)

[ ] Random Forest & KNN Classifiers (Module 3 - Coming Soon)

[ ] Statistical Process Control (SPC) & Trend Plotter (Module 4 - Coming Soon)

[ ] Wafer Map Heatmap Generator (Module 5 - Planned)

🔒 Security & Privacy Notice
All dataset processing on protictac.com is non-persistent and memory-isolated.

Sensitive semiconductor process parameter headers are anonymized and processed with strict zero-leak protocols.

© 2026 Pro Tic Tac Platform. Built by Bruce Chen.