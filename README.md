# Geology Forecast Challenge (Kaggle)

# Introduction

This project explored a real-world dataset from a Kaggle competition called the Geology Forecast Challenge. The goal was to predict a specific target value related to geological data using machine learning models.

We started by understanding and cleaning the data, followed by trying different models to see which performed best. Our approach included using k-Nearest Neighbors (kNN), tree-based models like Random Forest, and linear models like Ridge Regression. We also focused on tuning these models to improve performance.

To gain deeper insights, we experimented with clustering to explore hidden patterns in the data. Along the way, we carefully handled feature selection, checked for data leakage, and evaluated our models using cross-validation. We tracked our Kaggle scores over time to see how our changes affected the results.

This notebook outlines the full machine learning workflow, including:
- Data loading and preprocessing
- Exploratory data analysis (EDA)
- Baseline and advanced modeling (starting with k-Nearest Neighbors)
- Feature analysis and selection
- Evaluation using cross-validation
- Submission of predictions to Kaggle

This project allows us to apply the techniques we’ve learned in class from exploratory data analysis to model evaluation, on a challenging, real-world dataset. It also gives us the chance to engage with the Kaggle community and benchmark our solutions against peers through a leaderboard. Ultimately, the project isn’t just about building accurate models, but also about understanding the data deeply, making thoughtful design choices, and learning from each step of the process.

Overall, this project helped us practice the end-to-end process of a data science workflow from data exploration and preprocessing to modeling and interpretation.

#### Problem Statement
Develop a machine learning model to predict the probability distribution of rock types from geological drilling sensor data. This is a classification problem where the output should match the submission format (probabilities per class), and the evaluation metric is log loss.

## List the key steps you took to perform EDA
1. Dataset Overview
2. Missing Value Analysis
3. Statistical Summary
4. Correlation Check
5. Distribution Plots
6. Feature Relationships
7. Boxplots and Outliers
8. Clustering analysis

## List and describe your kNN methodological design you used for experimental testing, benchmarking against a baseline, tuning, ensuring data leakage was not ocurring and how you effectively summarised and communicated all your results
In this project, we applied a well-structured and rigorous methodological design to develop and evaluate a k-Nearest Neighbors (kNN) model. The design covered all critical stages as below.
1. Experimental Testing
   - Train-Test Split
   - Feature Scaling
   - Baseline Comparison
2. Benchmarking
   - Training kNN models with varying k values and both uniform and distance weighting schemes
   - For each configuration, we used 5-fold cross-validation and computed Root Mean Squared Error (RMSE) as the primary metric
   - This approach allowed us to visualize model behavior over a range of hyperparameter values and identify performance trends
3. Hyperparameter Tuning
   - We performed a grid search over
   - Used cross_val_score() from scikit-learn with a custom RMSE scorer
   - Visualized the RMSE scores using line plots
4. Data Leakage Prevention
   - Scaling and preprocessing were performed only on training data
   - The cross-validation folds used in benchmarking and tuning were isolated from the test set
   - At no point was test data (X_test) used for training or tuning model parameters
5. Result Communication and Interpretation
   - I created a table and line plots showing RMSE scores for each combination
   - Clearly annotated the best-performing configuration
   - Presented the final model’s predictions on the test set alongside actual values
   - Plotted the Kaggle submission score history to show the progression and improvements made through iterations
   - All results were described in plain language and supported by visuals for better interpretation

## List all the predictive algorithms you used for the classification modelling component where you had the freedom to explore alternative methods. List here also your best Kaggle score and your position on the Kaggle leaderboard
1. Ridge
2. Support Vector Machine (SVM)
3. Random Forest Classifier

## Analysis: list here all the remaining test design strategies you used, like k-fold CV, hyperparameter tuning, feature selection and feature engineering, discussion of your submission score results over time with resepct to model refinements and their effects
1. K-Fold Cross-Validation (CV)
2. Hyperparameter Tuning
3. Feature Selection and Engineering
4. Data Preprocessing to Prevent Data Leakage

### Executive Summary
This project focused on the Kaggle Geology Forecast Challenge, a supervised classification task aiming to predict geological formations based on spatial and sensor data.

After thorough data cleaning, exploratory data analysis, and feature engineering, several models were developed and evaluated, including k-Nearest Neighbors, Ridge, Random Forest, Support Vector Machine. Stratified k-fold cross-validation and grid search were used for hyperparameter tuning, and clustering analysis using KMeans with PCA provided insights into feature separability.

To improve on our baseline, we explored additional machine learning algorithms such as Ridge Regression, Random Forests, and Gradient Boosting. We compared these models using accuracy, log loss, and precision/recall metrics, and evaluated their runtime and interpretability. We also investigated feature importance and tried different feature selection strategies to enhance model performance.

Throughout the project, we carefully tracked each experiment and submitted our best-performing k-NN model to Kaggle. Our leaderboard score and ranking were documented, and all findings were compiled into this notebook, offering a clear and reproducible workflow.

This challenge helped us connect theory with practice, experiment with multiple modeling strategies, and build a stronger understanding of how machine learning applies in real-world industrial settings.
