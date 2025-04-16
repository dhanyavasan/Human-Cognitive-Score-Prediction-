# Human-Cognitive-Score-Prediction

## Overview
The objective of this study is to examine the extent to which behavioral, lifestyle, and demographic factors contribute to variations in human cognitive performance. By leveraging a large-scale dataset, this analysis aims to uncover meaningful patterns and relationships within the data and to construct a data-driven model capable of estimating cognitive scores.

## Dataset
This dataset is sourced from [Kaggle](https://www.kaggle.com/datasets/samxsam/human-cognitive-performance-analysis/data). The dataset containing 80,000 samples is explored with the objective of predicting human cognitive scores based on a variety of lifestyle, demographic, and behavioral features. The dataset includes attributes such as age, sleep duration, stress level, diet type, screen time, exercise frequency, caffeine intake, memory test score and more—each potentially influencing cognitive performance. 

Please find the EDA in this [link](https://github.com/dhanyavasan/Human-Cognitive-Score-Prediction-/blob/main/Capstone_phase_I.ipynb) to Jupyter Notebook: 


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

1. Removed: User_ID and AI_Prediction_Score (irrelevant for cognitive score prediction).
2. Normalized - Applied to numerical features (Age, Caffeine_Intake, Reaction_Time, Memory_Test_Score) as these features showed uniform distribution.
3. Ordinal Encoding - Applied to Stress_Level and Exercise_Frequency as they have an inherent order.
4. Nominal Encoding - Applied to Gender and Diet_Type (non-ordinal categories).
5. Joint Encoding - Applied to Sleep_Duration and Daily_Screen_Time (related features in hours).


## Model Building & Prediction

A basic Linear Regression model was created to predict cognitive scores based on the cleaned data. While the initial model provides decent results, more advanced algorithms can be explored and be compared with each other to find the best model to suit the usecase.

## Conclusion: 
The model shows potential in identifying how various factors influence cognitive performance. By comparing more advanced models and fine-tuning the current approach, this work can be enhanced and applied in real-world scenarios, such as mental wellness tracking and personalized lifestyle recommendations.
