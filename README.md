# Project: CleanRoom Attribution Modeling Toolkit

## Directory Structure
A multi-layed attribution modeling framework for privacy-safe ad measurement in clean room environment.

## Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [Architecture](#architecture)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Subprojects](#subprojects)
   - [1. Rule-based Attribution](#1-rule-based-attribution)
   - [2. Markov Chain Attribution](#2-markov-chain-attribution)
   - [3. Shapley Value Attribution](#3-shapley-value-attribution)
   - [4. ML-based Attribution (XGBoost + SHAP)](#4-ml-based-attribution-xgboost--shap)
   - [5. Uplift Modeling](#5-uplift-modeling)
   - [6. Hybrid Attribution](#6-hybrid-attribution)
   - [7. AI-Powered Modules](#7-ai-powered-modules)
7. [Configuration](#configuration)
8. [Pipeline](#pipeline)
9. [Contributing](#contributing)
10. [License](#license)
11. [Contact](#contact)


# CleanRoom Attribution Modeling Toolkit

A privacy-conscious open-source toolkit to simulate Clean Room environments and run various marketing attribution models (rule-based, probabilistic, ML-based, and hybrid aggregation & Ai-powered) using anonymized or aggregate data. This project aims to help marketing teams and data scientists build and evaluate attribution strategies without violating user privacy.


## 🌐 Why This Project?
As third-party cookies fade and GDPR/CCPA regulations tighten, marketing teams face challenges in linking touchpoints to conversions. Clean Rooms like Google ADH, Meta AA, and Amazon MC offer a privacy-safe alternative — but often lack open-source modeling frameworks. This project fills that gap.

## 📦 Features
- **Fully SQL-driven modules** for clean room environments (BigQuery / ADH)
- **Python scripts** for advanced modeling and explainability
- **Modular structure**: independent subprojects for each attribution technique
- **AI extensions**: automated feature engineering, LLM insights, anomaly detection
- **Visualization**: visualize results with ready-to-use dashboard templates

## 🔧 Model Types
- **Rule-Based**: Last-touch, First-touch, Linear
- **Probabilistic**: Markov chains, Shapley values
- **ML-Based**: Logistic Regression, Random Forest, XGBoost
- **Hybrid**: Weighted ensemble or conditional logic blending models

## Architecture
```text
Data Sources → Subproject Modules → Attribution Scores → Hybrid Aggregation → AI Insights → Reports

## 🚀 Quick Start
```bash
pip install -r requirements.txt
python simulated_cleanroom/synthetic_data_generator.py
python models/rule_based.py
```

## 📊 Dashboard
Comes with exportable Tableau templates to visualize attribution paths, ROAS impact, and conversion funnels.

## 📁 Case Study (Coming Soon)
- E-commerce campaign with anonymized data
- Meta Ads + Email + Search interaction modeling

## 📜 License
MIT License

## 🤝 Contributing
Pull requests and feature suggestions welcome — let’s build privacy-safe attribution together!
