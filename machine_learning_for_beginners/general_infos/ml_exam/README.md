<sub>[← Previous page](../README.md)</sub>  

# Machine Learning for Beginners
## Final ML Exam

## General instructions

In order tog et ECTS points, you need to pass in the final ML exam, which consists into: 

- A presentation of a ML investigation described by the steps below
- The submission of the corresponding Python code.

You will submit a Python code (as a jupyter notebook file entitled `Lastname_Firstname_ImmatriculationNumber.ipynb`) addressing the steps described below. Your code should be submitted to **albuquerque@uni-bayreuth.de** until the deadline (to be announced).

On the day of the presentation (place/time to be announced), you will make a presentation (12 min +/- 2) clearly addressing the steps described below. After your presentation, some general questions (ca 5 min) shall be made about your presentation and general ML concepts.


## Step 1: Choose Your Dataset

Select any suitable **regression** dataset.

Public sources such as Kaggle.com are allowed. You can also take your own data.

Make sure the dataset has:

- Enough samples
- Clear input features
- At least one continuous target variable


## Step 2: Train–Test Split

Split your dataset into:

- 80% Training set
- 20% Test set

Do **not** touch the test set until the end.

Do **not** use it for:

- Model selection
- Hyperparameter tuning
- Cross-validation

The test set must only be used for the final evaluations (Step 5).


## Step 3: Train and Screen Models

You must test at least the following regression models:

- Random Forest (RF)
- Support Vector Regression (SVR)
- k-Nearest Neighbors (KNN)
- LASSO
- Gaussian Process (GP)

#### Model Screening

- Use 5-fold Cross-Validation (CV) only on the training set
- Optimize hyperparameters if needed
- Do not forget to appropriately preprocess your dataset


## Step 4: Evaluate Model Performance

During model screening, report:

- MAE (Mean Absolute Error)
- MSE (Mean Squared Error)
- R² (Coefficient of Determination)

Compare all models (show a bar plot comparing the metrics of all investigated models) and select the best one mainly based on the lowest error. Do not forget to preprocess the dataset.


## Step 5: Final Test Evaluation

After selecting the best model:

1. Retrain the model using the full training set
2. Evaluate it once on the test set

Show:

- Parity plot (Predicted vs. True values)
- Performance metrics on the title of the plot


## Step 6: Training Performance

Evaluate your best model on the training data after having trained it on the same training data.

Show:

- Parity plot
- Performance metrics on the title of the plot


## Step 7: Overfitting Analysis

Show side-by-side the parity plots obtained in Steps 5 and 6 above to compare:

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

Discuss these results in terms of model stability/robustness.


## Step 9: Ensemble Model

- Combine the two best individual ML models screened in Step 3
- Build a simple ensemble model (for example, by averaging predictions)

Compare:

- Ensemble performance evaluated on the test set
- Best individual model performance also evaluated on the test set

Discuss advantages and disadvantages of your ensembling approach.


## Good Practice

- Keep your work reproducible (fix and report random seeds)
- Explain your decisions
- Use clear plots and labels
- Practice your presentation timing


## Common Mistakes to Avoid

- Using the test set during model tuning
- Missing preprocessing steps
- Not explaining methods clearly
- Poorly labeled figures
- Exceeding the presentation time limit
