# Pro Tic Tac - Semiconductor AI & Machine Learning Toolbox 🚀

[![Platform](https://img.shields.io/badge/Platform-Pro_Tic_Tac-06b6d4?style=for-the-badge)](https://protictac.com)
[![Framework](https://img.shields.io/badge/Framework-Laravel_11-ff2d20?style=for-the-badge&logo=laravel)](https://laravel.com)
[![Engine](https://img.shields.io/badge/ML_Engine-XGBoost_%7C_SVM_%7C_KNN-38bdf8?style=for-the-badge&logo=python)](https://github.com/scikit-learn/scikit-learn)
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
[ Module 1: XGBoost ]          [ Module 2: SVM Classifier ]    [ Module 3: KNN Classifier ]
Yield Anomaly & SHAP           Linear Hyperplane Weights       Permutation Importance
           |                              |                              |
           +------------------------------+------------------------------+
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

📦 Module 2: SVM Classifier Yield Diagnostics (Active)
The Support Vector Machine (SVM) Classifier utilizes standardized feature scaling (StandardScaler) and linear margin hyperplanes to determine clear-cut decision boundaries between functional passing dies and parametric yield anomalies.

🌟 Key Performance Metrics
Dataset Volume: 3,000 samples (Hold-out test verification set)

Optimization Pipeline: Scikit-Learn Pipeline + GridSearchCV (C=1, kernel='linear')

Test ROC-AUC: 0.9895 (Exceptional separation confidence)

Test Accuracy: 93.17%

Top Hyperplane Weight: vt_p (Feature Weight = 3.6483, ~3.7x higher impact than vt_n)

📦 Module 3: KNN Classifier Yield Diagnostics (Active - Released 2026.09)
The K-Nearest Neighbors (KNN) Classifier employs StandardScaler feature normalization paired with distance-weighted local space evaluation to partition parametric yield clusters and isolate anomaly boundaries in high-dimensional feature spaces.

🌟 Key Performance Metrics
Dataset Volume: 3,000 samples (28nm FEOL verification set)

Optimization Pipeline: Scikit-Learn Pipeline + GridSearchCV (n_neighbors=11, metric='manhattan', weights='distance')

Test ROC-AUC: 0.9654 (High statistical trustability and sharp spatial boundary)

Test Accuracy: 92.83%

Feature Importance Evaluation: Permutation Importance (scoring='roc_auc')

Top Attributed Driver: vt_n (ROC-AUC Impact = 0.0978) and vt_p (ROC-AUC Impact = 0.0971), confirming threshold voltage instability as the primary failure root cause.

🖼️ User Interface & Diagnostic Showcase 1. KNN English Mode Showcase
English KNN Dashboard & SelectionFeature Permutation Importance Table

Automated AI Diagnostic Summary (English Excerpt)
Sample LLM Output Excerpt:

"Permutation importance confirms that yield loss is almost exclusively driven by threshold voltage instability across both NMOS and PMOS devices: vt_n (ROC-AUC Impact: 0.0978) and vt_p (ROC-AUC Impact: 0.0971). Physical process deviations point to Front-End-of-Line (FEOL) common-mode process excursions, specifically Gate Dielectric Thickness / EOT Variance and Channel/Halo Implant Drift."

2. KNN Traditional Chinese Mode Showcase (繁體中文)
繁中良率診斷 UI 選單與 DashboardTop 5 KNN 關鍵影響參數與 AI 報告

🛣️ Future Roadmap & Upcoming ML Tools
The Pro Tic Tac platform is continuously expanding to include more statistical and machine learning tools for fab yield enhancement:

[x] Module 1: XGBoost & SHAP Automated Diagnostics (Released & Active)

[x] Module 2: Support Vector Machine (SVM) Classifier (Released & Active)

[x] Module 3: K-Nearest Neighbors (KNN) Classifier (Released & Active)

[ ] Module 4: Decision Trees & Random Forest Classifiers (Coming Soon)

[ ] Module 5: Statistical Process Control (SPC) & Trend Plotter (Coming Soon)

[ ] Module 6: Wafer Map Heatmap Generator (Planned)

🔒 Security & Privacy Notice
All dataset processing on protictac.com is non-persistent and memory-isolated.

Sensitive semiconductor process parameter headers are anonymized and processed with strict zero-leak protocols.

© 2026 Pro Tic Tac Platform. Built by Bruce Chen.
