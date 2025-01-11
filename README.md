# YouTube Statistics Analysis: Predicting Channel Type

## Overview
This project analyzes global YouTube statistics to predict the **channel type** based on various engagement metrics, such as views, likes, comments, and regional trends. The project incorporates data cleaning, machine learning models, and Tableau dashboards to uncover insights and make actionable predictions about channel classifications.

---

## Objectives
- Prepare and clean YouTube data using Orange workflows.
- Use machine learning models to predict channel type based on engagement metrics.
- Visualize trends and insights with Tableau dashboards.
- Provide actionable recommendations based on predictions.

---

## Key Features
1. **Data Cleaning and Preparation**:
   - Performed data imputation, normalization, and feature selection using Orange.
   - Exported a clean dataset ready for machine learning and visualization.

2. **Machine Learning Models for Channel Type Prediction**:
   - Built models to predict the type of YouTube channel using:
     - **Random Forest**: To evaluate feature importance and classify channels.
     - **Neural Networks**: For capturing complex, non-linear patterns.
     - **Naive Bayes**: For probabilistic predictions based on engagement metrics.
     - **Logistic Regression**: For binary classification and interpretability.

3. **Visualization with Tableau**:
   - Developed an interactive Tableau dashboard for exploring YouTube engagement patterns and regional trends.
   - Highlighted model predictions with visual storytelling.

---

## Machine Learning Models and Performance

### Target Variable
The target variable is **Channel Type**, which categorizes YouTube channels into specific types (e.g., Entertainment, Education, Music, etc.).

### Model Performance Metrics
The models were evaluated using multiple metrics:
- **Accuracy**: Proportion of correct predictions.
- **Precision**: Proportion of true positives among predicted positives.
- **Recall**: Proportion of true positives among actual positives.
- **F1-Score**: Harmonic mean of precision and recall.
- **AUC (Area Under Curve)**: Measures the ability of the model to distinguish between classes.

| Model               | Accuracy  | Precision | Recall   | F1-Score | AUC    | Log Loss |
|---------------------|-----------|-----------|----------|----------|--------|----------|
| **Logistic Regression** | 0.5142    | 0.5342    | 0.4488   | 0.4894   | 0.5342 | 0.1004   |
| **Random Forest**       | 0.9528    | 0.8630    | 0.8626   | 0.8628   | 0.8630 | 0.7726   |
| **Naive Bayes**         | 0.8984    | 0.7808    | 0.7856   | 0.7950   | 0.7808 | 0.6503   |
| **Neural Network**      | 0.9517    | 0.8904    | 0.8882   | 0.8914   | 0.8904 | 0.8176   |

### Observations
- **Neural Networks**: Achieved the best overall performance with the highest F1-score (0.8914) and AUC (0.8904), indicating its ability to handle complex, non-linear patterns.
- **Random Forest**: Comparable to Neural Networks with high accuracy (0.9528) and F1-score (0.8628), making it the second-best model.
- **Naive Bayes**: Performed well, but slightly lower accuracy and precision compared to Random Forest and Neural Networks.
- **Logistic Regression**: The weakest performer, with lower scores across all metrics, indicating its simplicity was not sufficient for this problem.

---

## Tableau Dashboard

### Dashboard Features
The Tableau dashboard provides:
1. **Engagement Metrics**:
   - Interactive visualizations of likes, dislikes, views, and comments.
2. **Regional Trends**:
   - Insights into video performance across different regions.
3. **Channel Predictions**:
   - Visual representation of machine learning predictions for channel type.

---

## Data Preparation Workflow

### Workflow Overview
Data preparation in Orange included:
1. **Imputation**:
   - Replaced missing values with means or mode where applicable.
2. **Column Selection**:
   - Selected relevant columns such as views, likes, comments, region, and channel type.
3. **Data Splitting**:
   - Split the dataset into training and testing sets for model evaluation.
4. **Visualization**:
   - Explored relationships using scatter plots, feature importance, and correlation matrices.

### Workflow Preview
![Workflow Preview](screenshots/Data_Flow_Screenshot.png)

---

## Key Insights

### 1. Engagement Metrics
- Channels with higher views and likes tend to belong to the Entertainment or Music categories.
- Educational channels have lower overall engagement metrics but higher comment-to-view ratios.

### 2. Regional Trends
- Entertainment channels dominate in North America and Europe.
- Music channels see the most engagement in South America and Asia.

### 3. Channel Type Predictions
- Neural Networks successfully classified channel types with the highest accuracy.
- Random Forest identified **views**, **likes**, and **comment count** as the most critical features for predicting channel type.

---

## How to Use

### Prerequisites
- Install Orange and Tableau.

### Steps
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/YouTube_Statistics_Analysis.git
