# Sleep Stage Classifier

Machine learning workflow for classifying sleep stages using Apple Watch sensor (motion and heart rate) and polysomnography data.

## What Is In This Repository

- `source/preprocessing/`: Raw data processing and feature generation pipeline.
- `source/`: Shared utilities, constants, and sleep stage definitions.
- `data/`: Input folders for raw files (`heart_rate`, `labels`, `motion`, `steps`).
- `outputs/features/`: Generated feature files used for downstream modeling.
- `Digital_health_project.ipynb`: End-to-end notebook for preprocessing, modeling, and evaluation.
- `Project_report.pdf`: Complete project report.

## Data

Apple Watch data is available from PhysioNet:
- https://alpha.physionet.org/content/sleep-accel/1.0.0/

If your `data/` folder is empty, place downloaded files into these subfolders:
- `data/heart_rate/` (for `*_heartrate.txt`)
- `data/labels/` (for `*_labeled_sleep.txt`)
- `data/motion/` (for `*_acceleration.txt`)
- `data/steps/` (for `*_steps.txt`, if used by your workflow)

## Environment Setup

Use Python 3.12+.

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

## Features

### Data Preprocessing
- Handling missing values
- Feature scaling and encoding
- Dimensionality reduction with PCA
- Outlier detection and management
- Feature engineering

### Machine Learning Models
- Logistic Regression
- Random Forest 
- Gradient Boosting 
- K-Nearest Neighbors 
- Support Vector Machine

### Model Evaluation
- Accuracy, Precision, Recall, and F1-score
- Confusion Matrix
- Multi-class ROC curves and AUC
- Classification Reports

### Model Selection
- Comparison of 11 model variants
- Performance visualization across metrics

### Model Interpretability
- Feature importance analysis (Random Forest)
- SHAP values for model explanation
- SHAP summary and dependence plots

## Notebook Workflow

Open and run `Digital_health_project.ipynb` for a full analysis pipeline:
- loading raw data
- running preprocessing (`run_preprocessing(subject_ids)`)
- feature engineering
- data visualization
- model training/evaluation and testing
- results analysis and explainability analysis

Note:
- Preprocessing can take several minutes depending on machine speed.

## License

This project is licensed under the MIT License - see the [`LICENSE`](LICENSE) file for details.

## Reference

```text
Walch, O., Widmer, Y., Koscec, L., et al. (2019).
Sleep Stage Classification Using Delayed Movement Detection from a Wearable Device.
Sleep, 42(12), zsz180.
https://doi.org/10.1093/sleep/zsz180
```

## Author 
<div align="center">
  
<!-- Team Members -->
<p>
  <a href="https://www.linkedin.com/in/pengcheng-chen-153612317/">
    <img src="https://img.shields.io/badge/Pengcheng_Chen-LinkedIn-%2300a0dc?style=for-the-badge&logo=linkedin&logoColor=white" alt="Pengcheng Chen"/>
  </a>
</p>

</div>
