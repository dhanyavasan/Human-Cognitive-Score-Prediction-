# Human-Cognitive-Score-Prediction

**Dhanya Srinivasan**

## Introduction
In today’s fast-paced, distraction-heavy world, declining attention spans and rising cognitive health issues like ADHD have become increasingly common. Lifestyle, behavioral, and demographic factors play a critical role in shaping cognitive performance, yet these influences are often overlooked. This study aims to investigate how such factors contribute to variations in cognitive ability and to build a predictive model that estimates cognitive scores. The resulting tool can support cognitive health monitoring for individuals, assist clinicians in assessment, and serve as a foundation for further research in educational and wellness domains.

## Dataset
This dataset is sourced from [Kaggle](https://www.kaggle.com/datasets/samxsam/human-cognitive-performance-analysis/data). The dataset containing 80,000 samples is explored with the objective of predicting human cognitive scores based on a variety of lifestyle, demographic, and behavioral features. The dataset includes attributes such as age, sleep duration, stress level, diet type, screen time, exercise frequency, caffeine intake, memory test score and more—each potentially influencing cognitive performance. 

Please find the analysis & the model in this [......] to Jupyter Notebook.

## Overview of Predictive Modeling Process
Given that the dataset is structured in tabular form and the objective is to predict a continuous cognitive score, a supervised learning approach was employed using both linear and non-linear regression algorithms, including Linear Regression, Lasso Regression, Random Forest, and XGBoost. The models were evaluated based on residual plots, learning curves with increasing training size, and Root Mean Squared Error (RMSE) to identify the best performer.

##  Exploratory Data Analysis (EDA) Insights
1. **Sleep Duration**:  
   Analysis of sleep hours reveals that only about **17%** of the sample population gets the recommended **7-8 hours of sleep**. Additionally, **longer sleep durations** are positively correlated with **higher cognitive scores**, emphasizing the importance of adequate sleep for cognitive health.

2. **Screen Time**:  
   The analysis indicates that **increased screen time** is linked to **lower cognitive scores**, suggesting that excessive screen exposure may have a negative impact on cognitive performance.

3. **Caffeine Consumption**:  
   Contrary to the common belief that caffeine boosts alertness, a **negative correlation** between **caffeine intake** and **cognitive score** is observed, implying that higher caffeine consumption may be associated with lower cognitive performance.

4. **Stress and Exercise**:  
   A **negative correlation** between **stress level** and **cognitive score** suggests that higher stress is linked to lower cognitive performance. However, **exercise frequency** appears to mitigate this effect, enhancing cognitive performance despite high stress levels.

5. **Reaction Time**:  
   **Slower reaction times** are found to be associated with **lower cognitive scores**, indicating that individuals who take longer to respond may have diminished cognitive performance.
   

## Data Preprocessing

1. **Feature Selection:**
Removed: Dropped irrelevant features, namely User_ID and AI_Prediction_Score, as they do not contribute to predicting cognitive scores.

2. **Normalization:**
Applied to Numerical Features: Features like Age, Caffeine_Intake, Reaction_Time, Memory_Test_Score, Sleep_Duration, and Daily_Screen_Time were normalized since these features exhibited a uniform distribution. This ensures that all numerical data is on a comparable scale.

3. **Data Splitting:**
Train-Test Split: The dataset was divided into training (80%) and test (20%) sets to train the model and evaluate its performance on unseen data.

4. **Encoding:**
      - **Ordinal Encoding:** Applied to Stress_Level and Exercise_Frequency, as these features have a natural order (e.g., low, medium, high).
      - **Nominal Encoding:** Applied to Gender and Diet_Type, which are non-ordinal categorical variables. One-hot encoding was used to represent these features, creating binary columns for each category.




## Modeling
To predict cognitive scores, both linear and non-linear regression models were implemented and compared. Each model underwent appropriate hyperparameter tuning to optimize its performance.

- **Linear Regression:** A simple linear model used as a baseline to predict the cognitive score and capture relationships between features and the target.

- **Lasso Regression:** A regularized linear model that helps reduce overfitting by applying L1 regularization, improving model generalization.

- **Random Forest Regressor (Bagging):** A non-linear ensemble model that uses bagging, training multiple decision trees on bootstrapped samples to capture complex relationships.

- **XGBoost Regressor (Boosting):** A non-linear ensemble model that uses boosting to sequentially correct errors from previous trees, effectively capturing intricate, non-linear patterns in the data.

## Model Evaluation



## Conclusion
The predictive model identified reaction time and memory performance as the most significant factors influencing cognitive scores. This highlights the importance of engaging in activities that strengthen mental function, such as cognitive training and memory-enhancing exercises. Furthermore, adopting healthier lifestyle habits—including regular physical activity, effective stress management, adequate sleep, limited screen time, and moderate caffeine consumption—can contribute positively to overall cognitive well-being.

## Next Steps & Recommendations
- Expand the dataset with more diverse samples to improve model generalization.
- Incorporate additional features like genetic features, cognitive history for deeper insights.
- Explore advanced modeling techniques and hyperparameter tuning to enhance prediction accuracy.
- Validate the model periodically with real-world data to ensure practical relevance and reliability.







