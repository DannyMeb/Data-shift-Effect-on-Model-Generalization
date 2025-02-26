# ML Model Performance Under Data Shifts

## Project Overview
This repository delves into the performance of various machine learning models in response to data shifts within the hospitality industry. The goal is to identify models that maintain accuracy and robustness when faced with dynamic data distributions.

## Contents
- `Dataset/`: Contains the dataset used for model training and testing.
- `main.ipynb`: Jupyter notebook containing detailed model evaluations and analyses.

## Technical Details of the Project

### Data Collection and Preparation
The dataset consists of over 119,000 booking records from a global hotel chain, spanning from July 2015 to August 2017. It includes features like lead time, booking changes, cancellations, and average daily rates.

### Data Splitting Strategy
- **Training Set**: Data before March 15, 2017. 
- **Seen Test Set**: Data before March 15, 2017, matching the training set distribution.
- **Unseen Test Set**: Data post-March 15, 2017, and from countries/geographic regions not included in the training data.

### Models Evaluated
- **Logistic Regression**
- **Random Forest**
- **Gradient Boosting**
- **Bayesian Neural Network**
- **Deep Neural Network (DNN)**
- **Convolutional Neural Network (CNN)**

### Evaluation Metrics
- **Accuracy**: The percentage of correctly predicted instances.
- **AUC-ROC**: Measures the ability of a classifier to distinguish between classes.
- **Brier Score**: Quantifies the accuracy of probabilistic predictions.
- **Negative Log-Likelihood (NLL)**: Assesses the likelihood of the observed data under the model.

### Methodology
Using a combination of statistical tests and visualization techniques, we quantified the shifts in data distribution:
- **Kolmogorov-Smirnov Test**: Used to detect and measure changes in the distribution of data features between the training and test sets.
- **Visual Analysis**: Employed to further investigate and confirm the presence of data shifts and their impacts on model performance.

### Results and Insights
The analysis revealed a "double descent" phenomenon where model performance initially decreases with increased complexity due to overfitting and then improves as complexity continues to grow. This was particularly evident in models like Bayesian Neural Networks and further complex models like CNNs.

## Running the Analysis
Navigate to the `main.ipynb` notebook and execute the cells to replicate the analysis and view the results.

## Contributions
Contributions are welcome. Please fork the repository, make changes, and submit a pull request.

