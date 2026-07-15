# Decision Trees and Random Forest Project

## 📌 Overview
This project applies **Decision Trees and Random Forest** algorithms to predict whether a borrower will fully repay a loan using LendingClub data (2007-2010). The model aims to assist investors in making informed lending decisions based on borrower profiles. The dataset contains loan-related features that influence repayment behavior, and this project explores how machine learning models can classify loan repayment risk.

## 📂 Project Structure
```
├── data/                  # Dataset used for training and testing
├── notebooks/             # Jupyter notebooks with step-by-step implementations
├── src/                   # Python scripts for model training and evaluation
├── results/               # Outputs, plots, and model performance metrics
├── visualizations/        # Visual representations of results
├── README.md              # Project documentation
└── requirements.txt       # Dependencies required to run the project
```

## 📊 Dataset
The dataset used in this project is **LendingClub loan data (2007-2010)**, obtained from [LendingClub](https://www.lendingclub.com/info/download-data.action). It contains details about loans and borrowers, including:
- `credit.policy`: Whether the borrower meets LendingClub's credit criteria.
- `purpose`: Loan purpose category.
- `int.rate`: Interest rate of the loan.
- `installment`: Monthly installment amount.
- `fico`: FICO credit score.
- `revol.util`: Revolving line utilization rate.
- `not.fully.paid`: Target variable (1 if the loan was not fully paid back).

🔗 **GitHub Repository:** [Project Link](https://github.com/ranjansinghds/decision-trees-and-random-forest-project)

## 🔍 Methodology

### 1. **Exploratory Data Analysis (EDA)**
- **Distribution of Loan Repayment Status**: Visualized the proportion of fully paid vs. not fully paid loans.
- **FICO Score vs Loan Repayment**: Analyzed trends between credit scores and repayment behavior.
- **Correlation Analysis**: Identified relationships between numerical variables.
- **Boxplots and Histograms**: Explored distributions of `int.rate`, `installment`, and `revol.util` among different loan statuses.

### 2. **Data Preprocessing**
- **Handling Missing Values**: Checked for missing values and handled them using imputation techniques where necessary.
- **Encoding Categorical Variables**: Converted the `purpose` column into dummy variables using one-hot encoding.
- **Feature Scaling**: Standardized numerical features such as `int.rate` and `installment` for better model performance.
- **Train-Test Split**: Divided the dataset into 80% training and 20% testing data.

### 3. **Model Training**
- **Decision Tree Classifier**: Built an initial decision tree model to understand feature splits.
- **Random Forest Classifier**: Implemented an ensemble of decision trees to improve accuracy and reduce overfitting.
- **Hyperparameter Tuning**: Used `GridSearchCV` to find optimal depth and number of estimators.

### 4. **Model Evaluation**
- **Classification Metrics**: Evaluated models using accuracy, precision, recall, and F1-score.
- **Confusion Matrix**: Assessed false positives and false negatives in predictions.
- **Feature Importance Analysis**: Identified top contributing factors to loan repayment predictions.

## 📊 Visualizations
All generated plots and graphs are stored in the `visualizations/` folder. These include:
- **Histogram of two FICO distributions on top of each other, one for each credit.policy outcome.**
  ![credit.policy outcome](https://github.com/ranjansinghds/decision-trees-and-random-forest-project/blob/main/Decision%20trees%20and%20Random%20forest%20png/Histogram%20of%20two%20fico%20for%20each%20credit.policy.png)
- **Histogram of two FICO distributions on top of each other the not.fully.paid column.**
  ![not.fully.paid column](https://github.com/ranjansinghds/decision-trees-and-random-forest-project/blob/main/Decision%20trees%20and%20Random%20forest%20png/Histogram%20for%20two%20fico%20for%20not.fully.paid.png)
- **Countplot using seaborn showing the counts of loans by purpose, with the color hue defined by not.fully.paid.**
  ![loans by purpose, with the color hue defined by not.fully.paid](https://github.com/ranjansinghds/decision-trees-and-random-forest-project/blob/main/Decision%20trees%20and%20Random%20forest%20png/countplot%20for%20counts%20of%20loan%20by%20purpose%2C%20with%20hue%20defined%20by%20not.fully.paid.png)
- **The trend between FICO score and interest rate. Recreate the following jointplot.**
  ![The trend between FICO score and interest rate](https://github.com/ranjansinghds/decision-trees-and-random-forest-project/blob/main/Decision%20trees%20and%20Random%20forest%20png/jointplot%20for%20fico%20rate%20and%20interest%20rate.png)
- **The trend differed between not.fully.paid and credit.policy.**
  ![The trend differed between not.fully.paid and credit.policy](https://github.com/ranjansinghds/decision-trees-and-random-forest-project/blob/main/Decision%20trees%20and%20Random%20forest%20png/lmplots%20for%20not.fully.paid%20and%20credit.policy.png)


## 🛠️ Technologies Used
- **Python**
- **Scikit-learn**
- **Pandas & NumPy**
- **Matplotlib & Seaborn**
- **Jupyter Notebook**

## 📌 Future Improvements
- **Advanced Hyperparameter Tuning**: Use RandomizedSearchCV for faster optimization.
- **Feature Engineering**: Create new features based on financial ratios for better predictions.
- **Comparison with Other Models**: Implement SVM, XGBoost, and Neural Networks for benchmarking.
- **Deployment**: Convert the model into a Flask API for real-world usability.