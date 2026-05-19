<sub>[← Previous page](../README.md)</sub>

# Machine Learning for Beginners
## Final ML Exam

## General instructions

The exam consists into a presentation of a ML investigation described by the steps below, as well as the submission of the corresponding Python code.

You will submit a Python code (as a jupyter notebook file entitled `Lastname_Firstname_ImmatriculationNumber.ipynb`) addressing the steps described below. Your code should be submitted to albuquerque@uni-bayreuth.de until the deadline:

- To be announced

On the day of the presentation (place/time to be announced), you will make a presentation (12 min +/- 2) clearly addressing the steps described below. After your presentation, some general questions (ca 5 min)


## Step 1: Choose Your Dataset

Select any suitable regression dataset.

Public sources such as Kaggle.com are allowed.

Make sure the dataset has:

- Enough samples
- Clear input features
- At least one continuous target variable


## Step 2: Train–Test Split (Very Important!)

Split your dataset into:

- 80% Training set
- 20% Test set

Do **not** touch the test set until the end.

Do not use it for:

- Model selection
- Hyperparameter tuning
- Cross-validation

The test set must only be used for the final evaluation.


## Step 3: Train and Screen Models

You must test at least the following regression models:

- Random Forest (RF)
- Support Vector Regression (SVR)
- k-Nearest Neighbors (KNN)
- LASSO
- Gaussian Process (GP)

### Model Screening

- Use 5-fold Cross-Validation (CV)
- Perform CV only on the training set
- Optimize hyperparameters if needed


## Step 4: Evaluate Model Performance

During model screening, report:

- MAE (Mean Absolute Error)
- MSE (Mean Squared Error)
- R² (Coefficient of Determination)

Compare all models and select the best one.


## Step 5: Final Test Evaluation

After selecting the best model:

1. Retrain the model using the full training set
2. Evaluate it once on the test set

Show:

- Parity plot (Predicted vs. True values)
- Performance metrics

This is your final result.


## Step 6: Training Performance

Evaluate your best model on the training data.

Show:

- Parity plot
- Performance metrics

This helps analyze overfitting.


## Step 7: Overfitting Analysis

Compare:

- Training error
- Test error

Discuss:

- Is the model overfitting?
- Is it underfitting?
- Why?


## Step 8: Model Variance (Stability)

To evaluate model stability:

- Use the best screened model
- Apply repeated 5-fold cross-validation on the training set only
- Use 10 different random seeds

Report:

- Average MAE
- Standard deviation of MAE

Discuss what these values indicate about model stability and robustness.


## Step 9: Ensemble Model

- Combine the two best individual models
- Build a simple ensemble model (for example, by averaging predictions)

Compare:

- Ensemble performance
- Best individual model performance

Discuss advantages and disadvantages.


## Good Practice

- Keep your work reproducible
- Fix and report random seeds
- Explain your decisions
- Use clear plots and labels
- Practice your presentation timing


## Common Mistakes to Avoid

- Using the test set during model tuning
- Missing preprocessing steps
- Not explaining methods clearly
- Poorly labeled figures
- Exceeding the presentation time limit
