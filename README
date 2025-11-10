# Project Title: Dating App Behavior Analysis

## Abstract
The objective of this project is to explore the different characteristics that can affect decision-making in the dating app industry. By analyzing user profile attributes, app-specific features, user behavior, and broader social and psychological factors, we aim to understand the dynamics of online dating and the decision-making processes involved.

## Industry Overview
The dating app industry has grown rapidly over the past decade, driven by increased smartphone usage, shifting social norms, and advancements in matching algorithms. Major players like Tinder, Bumble, and Hinge dominate the market, with revenue generated through subscription models, in-app purchases, and advertising. Platforms are focusing on user safety, AI-driven matchmaking, and expanding into international markets to sustain growth.

## Dataset Overview
This dataset provides a synthetic representation of user behavior on a fictional dating app. It contains 50,000 records with 19 features capturing demographic details, app usage patterns, swipe tendencies, and match outcomes.

- **Source**: [Kaggle Dataset](https://www.kaggle.com/datasets/keyushnisar/dating-app-behavior-dataset/data)
- **Key Features**:
  - Gender, sexual orientation, location type, income bracket, education level
  - App usage time, swipe ratios, likes received, mutual matches
  - Match outcomes (e.g., "Mutual Match," "Ghosted," "Catfished")

## Hypotheses
1. **H1**: Higher activity leads to more matches.
2. **H2**: More complete profiles achieve greater success.
3. **H3**: There are differences based on gender/orientation.
4. **H4**: Urban users are more successful.

## Variables
- **gender**: User’s gender identity
- **sexual_orientation**: User’s sexual orientation
- **location_type**: Type of user’s location
- **income_bracket**: User’s income level
- **education_level**: Highest education attained
- **app_usage_time_min**: Daily app usage time in minutes
- **swipe_right_ratio**: Ratio of right swipes to total swipes
- **likes_received**: Number of likes received
- **mutual_matches**: Number of total successful matches
- **profile_pics_count**: Number of profile pictures
- **bio_length**: Number of characters in bio
- **match_outcome**: Categorical description of the match outcome

## Exploratory Data Analysis (EDA)
1. **Dataset Overview**: Examined rows, columns, and data types.
2. **Summary Statistics**: Analyzed numerical and categorical variables.
3. **Missing Values**: Addressed nulls and duplicates.
4. **New Variables**: Created metrics for app usage, activity score, and profile completeness.
5. **Correlation Analysis**: Explored relationships between key variables.

## Hypotheses Testing
- **H1**: Supported. Higher activity correlates with more matches.
- **H2**: Supported. More complete profiles lead to greater success.
- **H3**: Partially supported. Gender/orientation differences exist for specific groups.
- **H4**: Not supported for the general population, but urban users show higher success for non-binary individuals.

## Machine Learning Pipeline
### 1. Data Preparation
- Selected relevant features based on hypotheses.
- Encoded categorical variables.
- Split data into training (80%) and testing (20%) sets.
- **Target Variable**: The variable chosen for prediction was `success`, which indicates whether a user achieved a "Mutual Match" or "Date Happened".

### 2. Model Selection
- Used LazyClassifier to identify top-performing models.
- Selected LightGBM and XGBoost for deeper evaluation.

### 3. Hyperparameter Optimization
- Tuned LightGBM hyperparameters using GridSearchCV.
- Best parameters: `{'learning_rate': 0.05, 'max_depth': -1, 'n_estimators': 200, 'num_leaves': 50}`.

### 4. Final Model
- **Optimized LightGBM** achieved:
  - Cross-Validation Accuracy: 97.16%
  - Test Accuracy: 97.18%
- Selected for its high accuracy, efficiency, and robustness.

## Conclusion
This project demonstrates the potential of data-driven insights in the dating app industry. By analyzing user behavior and profile attributes, we identified key factors influencing match success. The final LightGBM model provides a reliable tool for predicting user success, offering valuable implications for app design and user engagement strategies.