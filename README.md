# XAI-IDS-Architecture

**XAI-IDS-Architecture** is an Explainable Artificial Intelligence (XAI) framework for Intrusion Detection Systems (IDS). This project focuses on enhancing the transparency, interpretability, and usability of machine learning-based IDS, making them actionable and trustworthy for cybersecurity analysts without compromising accuracy.

## 🚀 Motivation

Traditional IDS solutions, while effective in detecting cyber threats, often lack interpretability, making them less practical in high-stakes environments. Analysts need clear and actionable explanations for flagged threats to ensure trust and effective response. This project bridges the gap between detection and explainability by integrating XAI techniques into IDS.

## 🔍 Problem Statement

Modern IDS systems face challenges such as:

- **Opacity in Machine Learning Models**: Lack of interpretability in black-box models like deep learning.
- **False Positives and Negatives**: Misclassification of legitimate activities or missed threats.
- **Trust and Usability Issues**: Security analysts require explainable insights for validation.
- **Scalability and Adaptability**: Limited performance under high traffic and evolving threats.

## 🎯 Objectives

- Build an XAI-based IDS architecture that enhances transparency while maintaining high detection accuracy.
- Integrate explainability techniques such as SHAP (SHapley Additive ExPlanations) and LIME (Local Interpretable Model-Agnostic Explanations).
- Validate the architecture using benchmark datasets such as NSL-KDD and CICIDS-2017.
- Support analysts in mitigating threats with understandable, actionable insights.

## 🛠️ Features

- **Explainable AI Integration**: Use SHAP and LIME to make predictions interpretable.
- **Support for Multiple Attack Types**: Includes DoS, phishing, SQL injection, and zero-day attacks.
- **Evaluation Metrics**: Assesses accuracy, interpretability, scalability, and adaptability.
- **Scalability for Distributed Networks**: Efficient handling of real-time traffic.

## 🗂️ Project Structure

```plaintext
├── 1_Pre-Modeling-Phase
│   ├── Data Preprocessing and Feature Engineering
├── 2_Modeling-Phase
│   ├── Model Training and Evaluation
│   ├── Random Forest, XGBoost, and Explainability Models
├── 3_Post-Modeling-Phase
│   ├── Interpretability Analysis using SHAP and LIME
│   ├── Comparative Analysis with Traditional IDS
├── Datasets
│   ├── NSL-KDD and CICIDS-2017 Benchmark Data
├── README.md
```
## 📊 Datasets

The project utilizes the following benchmark datasets:

1. **NSL-KDD**: A well-known dataset for network intrusion detection research.
1. **CICIDS-2017**: Represents realistic modern cyberattack scenarios.

---

## 🛠️ Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/mo-abdulai/XAI-IDS-Architecture.git
   ```

2. Navigate to the project directory:

    ```bash
    cd XAI-IDS-Architecture
    ```

3. Install the required Python packages:

    ```bash
    pip install -r requirements.txt 
    ```


## 🧪 Usage

1. Preprocess the datasets:

    ```python 1_Pre-Modeling-Phase/data_preprocessing.py```

2. Train models and evaluate performance:

    ```python 2_Modeling-Phase/train_model.py```

3. Perform explainability analysis:

    ```python 3_Post-Modeling-Phase/xai_analysis.py```

## 📈 Evaluation Metrics

- Accuracy: Measures correct predictions.
- F1-Score: Evaluates precision and recall balance.
- Transparency: Provided by SHAP and LIME explanations.
- Scalability: Tested on real-time simulated traffic.

## 🧩 Future Work

- Extend support for encrypted traffic analysis.
- Improve scalability for large-scale distributed networks.
- Integrate real-time monitoring and alerting.

## 📝 References

- S. Mane and D. Rao, "Explaining Network Intrusion Detection System Using Explainable AI Framework," Persistent Systems Limited, India, 2020.
- F. Wei, H. Li, Z. Zhao, and H. Hu, "xNIDS: Explaining Deep Learning-based Network Intrusion Detection Systems for Active Intrusion Responses," Proceedings of the 32nd USENIX Security Symposium, Anaheim, CA, 2023.
- C. Molnar, Interpretable Machine Learning: A Guide for Making Black Box Models Explainable, 2020. 