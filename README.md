```markdown
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