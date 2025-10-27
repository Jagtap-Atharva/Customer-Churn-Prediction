# Telco Customer Churn Prediction

A machine learning project that predicts customer churn for a telecommunications company using various classification algorithms. The project analyzes customer data to identify patterns that indicate whether a customer is likely to discontinue their service.

## 📊 Dataset

This project uses the **Telco Customer Churn** dataset, which contains information about:
- Customer demographics
- Services subscribed to
- Account information
- Churn status (target variable)

Dataset: `WA_Fn-UseC_-Telco-Customer-Churn.csv`

## 🎯 Project Overview

The goal is to build and compare multiple machine learning models to accurately predict customer churn, enabling the business to take proactive retention measures.

### Models Implemented:
1. **Logistic Regression** - Baseline linear model
2. **Random Forest** - Ensemble method with 200 trees
3. **XGBoost** - Gradient boosting classifier

## 🛠️ Technologies Used

- **Python 3.x**
- **pandas** - Data manipulation
- **numpy** - Numerical computations
- **matplotlib & seaborn** - Data visualization
- **scikit-learn** - Machine learning models and preprocessing
- **XGBoost** - Advanced gradient boosting

## 📋 Prerequisites

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

Or install from requirements file:

```bash
pip install -r requirements.txt
```

## 🚀 Installation & Usage

1. Clone the repository:
```bash
git clone https://github.com/yourusername/telco-churn-prediction.git
cd telco-churn-prediction
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Place the dataset file `WA_Fn-UseC_-Telco-Customer-Churn.csv` in the project directory

4. Run the script:
```bash
python churn_prediction.py
```

## 📈 Project Workflow

### 1. Data Preprocessing
- Removed `customerID` column (unique identifier)
- Converted `TotalCharges` to numeric format
- Handled missing values using median imputation
- Encoded target variable (`Churn`) as binary (0/1)
- Label encoded all categorical features

### 2. Exploratory Data Analysis (EDA)
- Analyzed churn distribution
- Generated correlation heatmap to identify feature relationships
- Visualized feature importance

### 3. Model Training
- Split data: 80% training, 20% testing (stratified)
- Applied Standard Scaling for feature normalization
- Trained three classification models
- Evaluated using multiple metrics

### 4. Evaluation Metrics
- **Accuracy** - Overall prediction correctness
- **Recall** - Ability to identify churned customers
- **ROC-AUC** - Model's discriminative ability
- **Confusion Matrix** - Detailed prediction breakdown
- **ROC Curve** - Visual performance assessment

## 📊 Results

The script generates:
- Churn distribution plot
- Feature correlation heatmap
- Model evaluation metrics for each classifier
- ROC curves for model comparison
- Feature importance chart (XGBoost)

## 🔍 Key Features

- **Comprehensive preprocessing pipeline** for handling real-world messy data
- **Multiple model comparison** to identify best performer
- **Detailed evaluation metrics** focused on business-relevant measures
- **Feature importance analysis** to understand churn drivers
- **Visualizations** for better interpretability

## 📁 Project Structure

```
telco-churn-prediction/
│
├── churn_prediction.py          # Main script
├── WA_Fn-UseC_-Telco-Customer-Churn.csv  # Dataset
├── requirements.txt             # Dependencies
└── README.md                    # Documentation
```

## 🎯 Future Improvements

- Implement hyperparameter tuning (GridSearchCV/RandomizedSearchCV)
- Add SMOTE or other techniques to handle class imbalance
- Create a web interface for predictions using Flask/Streamlit
- Perform feature engineering for better model performance
- Add cross-validation for more robust evaluation
- Deploy model as an API endpoint

## 📝 Notes

- The project uses stratified train-test split to maintain class distribution
- Standard scaling is applied to normalize features with different ranges
- XGBoost model includes feature importance analysis
- All models are evaluated on the same test set for fair comparison

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

Atharva Jagtap - [@yourhandle](https://github.com/Jagtap-Atharva)

## 🙏 Acknowledgments

- Dataset source: IBM Sample Data Sets
- Scikit-learn documentation
- XGBoost documentation
