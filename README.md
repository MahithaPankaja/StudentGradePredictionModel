# StudentGradePredictionModel
This repository provides end-to-end TensorFlow/Keras models to predict university students' average semester grades using survey and academic features, with full preprocessing, training, evaluation, and visualizations for the neural networks.

# Dataset
The dataset dataSet.csv contains survey responses with academic and lifestyle information:

Year of Study, Attendance Rate, Subject Grades, GPA

Study hours per week, Assignment completion frequency

Part-time job status, Extracurricular involvement

Preprocessing includes handling missing fields, encoding categorical variables, and normalizing GPA and features.

# Preprocessing Workflow
Filtering out incomplete rows or missing grades

Encoding categorical data (attendance, study hours, assignment frequency, job, extracurriculars)

Mapping grades to numeric values (A+=4.0, A=4.0, ..., E=0)

Normalizing GPA and creating the target: average grade of main subjects

Output is saved as preprocessed_model_data.csv for modeling.

# Models
Two core architectures are included:

# Shallow Model (StuGrdPrdShallowModel.ipynb)
Multi-layer perceptron (MLP) with 3 hidden layers (32, 16, 8 units)

Input features: Encoded attendance, study hours, assignment completion, job, extracurriculars, normalized GPA

Output: Average grade (numeric and letter grade)

Loss: Mean Squared Error (mse); Metric: Mean Absolute Error (mae)

Visualizations: Scatter plot true vs. predicted grades

# Deeper Model (StuGrdPrdDeeperModel.ipynb)
Deeper MLP with more layers for improved prediction (128, 64, 32, 16, 8, 4, 2 units)

Same feature pipeline and output as above

Shows improved learning and lower error on validation

# Evaluation
Both models use 85% training / 15% test split

Performance metrics: MSE, MAE, comparison of actual vs. predicted grades (numeric and converted to letter)

The README includes utility code for mapping numeric grades back to standard letter grades for easy interpretation (A, B+, etc.)

# Usage
Place dataSet.csv in the working directory

Run either notebook (StuGrdPrdShallowModel.ipynb or StuGrdPrdDeeperModel.ipynb)

View preprocessing, training, evaluation, and plots

For manual predictions, run the interactive cell in the notebook to enter new student feature inputs and get grade predictions

# Features
Clean, reproducible preprocessing pipeline (pandas/numpy)

Keras deep learning models for regression

Ready-to-run notebooks for new data and custom predictions

Utility for letter grade mapping and scatter plots for model validation

# Visualizations
Scatterplots of predicted vs. actual grades enable quick assessment of model performance

Numerical and categorical accuracy metrics for regression output

# Requirements
Python 3.x

TensorFlow/Keras

scikit-learn

pandas, numpy, matplotlib

Feel free to use, adapt, and extend to your university dataset and prediction tasks. For details, follow code comments and markdown explanations in provided notebooks.