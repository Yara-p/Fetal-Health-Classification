# Fetal Health Classification

## Overview
This project aims to classify fetal health using features extracted from Cardiotocogram (CTG) data. It categorizes fetal health status into three classes: Normal, Suspect, and Pathological. The goal is to enhance the accuracy and reliability of fetal health assessments, providing healthcare professionals with an effective tool for early diagnosis.

## Objectives
- **Problem Objective**: Monitor fetal health using CTG data.
- **Research Questions**:
  1. Can we accurately classify fetal health using CTG data?
  2. Which machine learning algorithms are most effective for this classification task?
  3. What are the most important features for predicting fetal health?

## Data
- **Source**: The dataset is publicly available on Kaggle: [Fetal Health Classification](https://www.kaggle.com/datasets/andrewmvd/fetal-health-classification).
- **Description**: The dataset contains 2,126 records with features derived from CTG exams, which were then categorized into three classes by expert obstetricians: Normal, Suspect, and Pathological.
- **Features**: 
  - FHR baseline, accelerations, fetal movement, uterine contractions, light decelerations, severe decelerations, prolonged decelerations, abnormal short-term variability, histogram metrics, and others.
- **Target**: **'fetal_health'** - Classified as 1 (Normal), 2 (Suspect), and 3 (Pathological).

## Data Preparation
- **Preprocessing**: The dataset did not contain missing values. Standardization was applied to ensure consistency in feature scales.
- **Class Imbalance Handling**: Applied SMOTE (Synthetic Minority Over-sampling Technique) to address class imbalance, thereby enhancing the performance of models in predicting minority classes.

## Exploratory Data Analysis (EDA)
- **Visualization**:
  - **Histograms and Box Plots**: Used to understand feature distributions and identify significant outliers.
  - **Correlation Matrix**: Visualized using a heatmap to understand feature relationships. Highly correlated features were dropped to avoid redundancy.
- **Key Insights**: Features like prolonged decelerations and abnormal short-term variability were found to be positively correlated with fetal health issues.

## Machine Learning Models
- **Algorithms Implemented**:
  - K-Nearest Neighbors (KNN)
  - Gaussian Naive Bayes
  - Random Forest
  - Gradient Boosting
  - Logistic Regression
  - Linear Discriminant Analysis (LDA)
  - Neural Network (MLP)
  - Support Vector Machine (SVM)
- **Best Performing Models**:
  - **Random Forest**: Achieved an accuracy of 94%, excelling across all classes.
  - **Gradient Boosting**: Demonstrated strong performance, particularly in distinguishing between classes.
  - **Neural Networks**: Provided balanced precision and recall, suitable for capturing complex non-linear relationships.

## Results
- **Random Forest** emerged as the top-performing model, with high accuracy and reliability in classifying all three fetal health categories.
- **Performance Metrics**: Classification reports and confusion matrices highlighted the strong performance of Random Forest and Gradient Boosting, especially in identifying "normal" and "pathological" cases.
- **Feature Importance**: Features like accelerations, prolonged decelerations, and variability measures played crucial roles in prediction.

## Future Work
- **Deep Learning**: Explore more advanced deep learning models for automated feature extraction.
- **Data Generalization**: Validate the model on data collected from different populations and settings.
- **Model Interpretability**: Enhance interpretability to provide actionable insights for healthcare professionals.

## Usage
To run the project:
1. Clone the repository:
    ```bash
    git clone https://github.com/YOUR_USERNAME/Fetal-Health-Classification.git
    ```
2. Navigate to the directory:
    ```bash
    cd Fetal-Health-Classification
    ```
3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4. Run the Jupyter notebook for analysis:
    ```bash
    jupyter notebook Fetal_Health.ipynb
    ```

## Conclusion
This project successfully demonstrated the application of machine learning models to classify fetal health using CTG data. The **Random Forest** and **Gradient Boosting** models provided the most reliable predictions, showing significant promise in assisting healthcare professionals in early diagnosis and decision-making.

