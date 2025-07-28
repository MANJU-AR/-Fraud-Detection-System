# Credit Card Fraud Detection

A machine learning project for detecting fraudulent credit card transactions using Random Forest classifier with balanced class weights to handle imbalanced datasets.

## 📊 Overview

This project implements a fraud detection system that can identify potentially fraudulent credit card transactions. The model achieves excellent performance with an AUC-ROC score of 0.958, demonstrating high accuracy in distinguishing between legitimate and fraudulent transactions.

## 🎯 Key Results

- **Accuracy**: 99.95%
- **AUC-ROC Score**: 0.958
- **Precision (Fraud)**: 96%
- **Recall (Fraud)**: 76%
- **F1-Score (Fraud)**: 85%

## 📁 Project Structure

```
fraud-detection/
│
├── Fraud detection.ipynb    # Main notebook with complete analysis
├── creditcard.csv          # Dataset (not included - see data section)
├── README.md              # Project documentation
└── requirements.txt       # Dependencies
```

## 🔧 Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/fraud-detection.git
cd fraud-detection
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

## 📊 Dataset

This project uses the Credit Card Fraud Detection dataset. The dataset contains:
- **284,807** total transactions
- **492** fraudulent transactions (0.17%)
- **284,315** legitimate transactions (99.83%)

### Features:
- **V1-V28**: Anonymized features (result of PCA transformation)
- **Time**: Time elapsed between transactions
- **Amount**: Transaction amount
- **Class**: Target variable (0 = legitimate, 1 = fraud)

**Note**: Due to size constraints, the dataset is not included in this repository. You can download it from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud).

## 🚀 Usage

1. Download the dataset and place `creditcard.csv` in the project directory
2. Open and run the Jupyter notebook:
```bash
jupyter notebook "Fraud detection.ipynb"
```



## 🧠 Model Architecture

### Algorithm: Random Forest Classifier
- **Why Random Forest?**
  - Handles imbalanced datasets well
  - Robust to outliers
  - Provides feature importance insights
  - Good generalization performance

### Key Preprocessing Steps:
1. **Feature Scaling**: StandardScaler normalization
2. **Class Balancing**: Balanced class weights to handle imbalanced data
3. **Feature Selection**: Removed 'Time' column, kept PCA-transformed features

### Hyperparameters:
- `class_weight='balanced'`: Automatically adjusts weights for imbalanced classes
- `random_state=42`: For reproducible results

## 📈 Performance Metrics

| Metric | Value |
|--------|-------|
| Accuracy | 99.95% |
| Precision (Class 0) | 100% |
| Precision (Class 1) | 96% |
| Recall (Class 0) | 100% |
| Recall (Class 1) | 76% |
| F1-Score (Class 0) | 100% |
| F1-Score (Class 1) | 85% |
| AUC-ROC | 0.958 |

### Confusion Matrix:
```
                Predicted
Actual    0        1
   0   56861      3
   1      24     74
```

## 🔍 Key Features

- **Imbalanced Data Handling**: Uses balanced class weights to address the 99.83% vs 0.17% class distribution
- **Feature Engineering**: Leverages PCA-transformed features for privacy and dimensionality reduction
- **Comprehensive Evaluation**: Multiple metrics including confusion matrix, classification report, and ROC curve
- **Visualization**: ROC curve plotting for model performance assessment

## 🛠️ Dependencies

```
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
jupyter>=1.0.0
```

## 📊 Visualizations

The project includes:
- ROC Curve with AUC score
- Performance metrics visualization
- Class distribution analysis


## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Dataset provided by Kaggle and the Machine Learning Group of ULB
- Scikit-learn library for machine learning tools
- The data science community for methodological insights


---

**Note**: This model is for educational and research purposes. For production use in financial systems, additional validation, testing, and regulatory compliance would be required.
