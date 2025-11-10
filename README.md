# Project Title: Dating App Behavior Analysis

## Abstract
This project explores the factors influencing decision-making in the dating app industry. By analyzing user profiles, app features, behaviors, and societal factors, we aim to understand the dynamics of online dating and predict user success.

---

## Project Structure
The project is organized as follows:

1. **Dataset**: Synthetic dataset with 50,000 records and 19 features.
2. **Exploratory Data Analysis (EDA)**: Data cleaning, feature engineering, and hypothesis testing.
3. **Machine Learning Pipeline**: Predictive modeling using LightGBM and XGBoost.
4. **Results and Conclusion**: Insights and final model evaluation.

---

## Dataset Overview
- **Source**: [Kaggle Dataset](https://www.kaggle.com/datasets/keyushnisar/dating-app-behavior-dataset/data)
- **Key Features**:
  - Demographics: Gender, sexual orientation, location type, income, education.
  - Behavior: App usage time, swipe ratios, likes received, mutual matches.
  - Outcome: Match outcomes (e.g., "Mutual Match," "Ghosted," "Catfished").

---

## Data Transformation
### 1. **Data Cleaning**
- Removed missing values and duplicates.
- Normalized column names for consistency.

### 2. **Feature Engineering**
- **New Variables**:
  - `app_usage_time_label`: Categorized app usage into Low, Moderate, and Extreme.
  - `success`: Binary target variable (1 = "Mutual Match" or "Date Happened").
  - `activity_score`: Composite metric combining app usage, messages sent, and swipe ratio.
  - `profile_completeness`: Composite metric combining profile pictures and bio length.

### 3. **EDA Highlights**
- Correlation analysis revealed:
  - Strong positive correlation between `activity_score` and `mutual_matches`.
  - Moderate correlation between `profile_completeness` and success metrics.
- Addressed anomalies (e.g., negative values in `likes_received`).

---

## Hypotheses Testing
1. **H1**: Higher activity leads to more matches → Supported.
2. **H2**: More complete profiles achieve greater success → Supported.
3. **H3**: Differences based on gender/orientation → Partially supported.
4. **H4**: Urban users are more successful → Not supported for the general population.

---

## Machine Learning Pipeline
### 1. **Data Preparation**
- Selected relevant features based on hypotheses.
- Encoded categorical variables.
- Split data into training (80%) and testing (20%) sets.
- **Target Variable**: `success` (1 = "Mutual Match" or "Date Happened").

### 2. **Model Selection**
- Used LazyClassifier to identify top-performing models.
- Selected LightGBM and XGBoost for deeper evaluation.

### 3. **Hyperparameter Optimization**
- Tuned LightGBM hyperparameters using GridSearchCV.
- Best parameters: `{'learning_rate': 0.05, 'max_depth': -1, 'n_estimators': 200, 'num_leaves': 50}`.

### 4. **Final Model**
- **Optimized LightGBM** achieved:
  - Cross-Validation Accuracy: 97.16%
  - Test Accuracy: 97.18%
- Selected for its high accuracy, efficiency, and robustness.

---

## Results and Conclusion
### Key Findings:
- **Activity**: Users with higher activity levels achieve more matches.
- **Profile Completeness**: Longer bios and more profile pictures lead to greater success.
- **Gender/Orientation**: Differences exist for specific groups.
- **Location**: Urban users show higher success for non-binary individuals.

### Final Model:
- The optimized LightGBM model provides a reliable tool for predicting user success.
- It demonstrates strong generalization and efficiency, making it suitable for production use.

### Implications:
- Platforms can enhance user engagement by encouraging activity and profile completeness.
- Insights can guide app design and targeted user strategies.

---

## References
- Dataset: [Kaggle](https://www.kaggle.com/datasets/keyushnisar/dating-app-behavior-dataset/data)
- Libraries: Pandas, NumPy, Scikit-learn, LightGBM, XGBoost, Seaborn, Matplotlib