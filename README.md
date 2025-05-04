# CleanRoom Attribution Modeling Toolkit

A privacy-conscious open-source toolkit to simulate Clean Room environments and run various marketing attribution models (rule-based, probabilistic, ML-based, hybrid aggregation & AI-powered) using anonymized or aggregated data. This project helps marketing teams and data scientists build and evaluate attribution strategies without violating user privacy.


## Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Architecture](#architecture)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Subprojects](#subprojects)

   * [1. Rule-based Attribution](#1-rule-based-attribution)
   * [2. Markov Chain Attribution](#2-markov-chain-attribution)
   * [3. Shapley Value Attribution](#3-shapley-value-attribution)
   * [4. ML-based Attribution (XGBoost + SHAP)](#4-ml-based-attribution-xgboost--shap)
   * [5. Uplift Modeling](#5-uplift-modeling)
   * [6. Hybrid Attribution](#6-hybrid-attribution)
   * [7. AI-Powered Modules](#7-ai-powered-modules)
7. [Configuration](#configuration)
8. [Pipeline](#pipeline)
9. [Contributing](#contributing)
10. [License](#license)
11. [Contact](#contact)

---

## Overview

As third-party cookies fade and GDPR/CCPA regulations tighten, marketing teams face challenges linking touchpoints to conversions. Clean Rooms like Google ADH, Meta AA, and Amazon MC offer a privacy-safe alternative — but often lack open-source modeling frameworks. This project fills that gap.

---

## Features

* **Fully SQL-driven modules** for clean room environments (BigQuery / ADH)
* **Python scripts** for advanced modeling and explainability
* **Modular structure**: independent subprojects for each attribution technique
* **AI extensions**: automated feature engineering, LLM insights, anomaly detection
* **Visualization**: exportable dashboard templates for quick insights

---

## Architecture

```text
Data Sources → Subproject Modules → Attribution Scores → Hybrid Aggregation → AI Insights → Reports
```

---

## Installation

```bash
git clone https://github.com/your_org/adh_attribution_project.git
cd adh_attribution_project
pip install -r requirements.txt
export GCP_PROJECT=your-project
export OPENAI_API_KEY=your_key
```

---

## Usage

```bash
# Generate synthetic data
python synthetic_data_generator.py --output data/events.csv

# Run rule-based attribution
bq query --use_legacy_sql=false < subproject_1_rule_based/sql/first_touch.sql

# Run ML-based attribution
python subproject_4_ml_based/python/xgboost_attribution.py --config config.yaml
```

---

## Subprojects

### 1. Rule-based Attribution

📂 `subproject_1_rule_based/`

* **Scripts**: `first_touch.sql`, `last_touch.sql`, `linear_touch.sql`
* **Description**: Last-touch, First-touch, and Linear models via SQL queries.

### 2. Markov Chain Attribution

📂 `subproject_2_markov/`

* **Scripts**: `transition_matrix.sql`, `removal_effect.sql`
* **Demo**: `notebooks/markov_demo.ipynb` for visualization.

### 3. Shapley Value Attribution

📂 `subproject_3_shapley/`

* **Script**: `shapley_estimator.py`
* **Notebook**: `notebooks/shapley_analysis.ipynb`

### 4. ML-based Attribution (XGBoost + SHAP)

📂 `subproject_4_ml_based/`

* **Scripts**: `xgboost_attribution.py`, `shap_explainer.py`

### 5. Uplift Modeling

📂 `subproject_5_uplift/`

* **Scripts**: `uplift_data_prep.py`, `uplift_xlearner.py`

### 6. Hybrid Attribution

📂 `subproject_6_hybrid/`

* **Script**: `hybrid_combine.py`

### 7. AI-Powered Modules

📂 `subproject_7_ai_powered/`

* **Scripts**: `llm_insight_generator.py`, `auto_feature_engineer.py`, `anomaly_detector.py`

---

## Configuration

```yaml
project: your-gcp-project
dataset: cleanroom_dataset
model:
  xgboost:
    max_depth: 6
    learning_rate: 0.1
```

---

## Pipeline

```bash
python run_all.py --steps rule_based,markov,ml,hybrid,ai
```

---

## Contributing

Pull requests and feature suggestions welcome!

1. Fork the repository
2. Create a feature branch
3. Commit and push
4. Open a Pull Request

---


## Contact

* **Yin Xu** (Fien) — [yinfienxuwork@gmail.com](mailto:yinfienxuwork@gmail.com)
* GitHub: [your\_org/adh\_attribution\_project](https://github.com/your_org/adh_attribution_project)
* LinkedIn: [linkedin.com/in/yinfienxu](https://linkedin.com/in/yinfienxu)
