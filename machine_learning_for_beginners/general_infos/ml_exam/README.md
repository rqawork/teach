<sub>[← Previous page](../README.md)</sub>  

# Machine Learning for Beginners
## Final ML Exam

## General instructions

In order to get ECTS points, you need to pass the final ML exam, which consists into: 

- A presentation of a ML investigation described by the Steps 1-9 below
- The submission of the corresponding Python code + dataset

On the day of the presentation, you will make a presentation (12 min +/- 2) clearly addressing the steps described below. After your presentation, some general questions (ca 5 min) shall be made about your presentation and general ML concepts.

#### Submission/Presentation details

| Item | Details |
|---|---|
| Deadline for files submission | 17 July 2026 at 23:59:59 |
| File 1 format | `FirstName_LastName_ImmatriculationNumber.ipynb` |
| File 2 format | `dataset.zip` |
| Submission method | E-mail to albuquerque@uni-bayreuth.de |
| Presentation place | Room S101, FAN A |
| Presentation date/time | 20 July 2026 from 09:00-12:00 |

#### Important notes

> **NOTE 1**: Your code is supposed to load your dataset from the same folder where the jupyter file is located, without using any long path. For instance, if the dataset is in file "mydataset.csv", your code should open it as e.g. `pd.read_csv('mydataset.csv')` and NOT as e.g. `pd.read_csv('C:\\Users\\Documents\\mydataset.csv')`.

> **NOTE 2**: Late submissions are still accepted but will receive worse grades. 

> **NOTE 3**: If, for any reason, you are unable to obtain ECTS credits, you can still receive a general certificate from the Department of Polymer Engineering, provided that you pass the final exam. However, we strongly recommend that you contact the secretary or coordinator of your study programme to ask whether the ECTS credits from this course can be officially recognized in your programme. In most cases, this recognition is a very simple administrative process (often just a formal approval), but it depends entirely on your individual study programme. Many students have successfully had these ECTS credits recognized in the past.

# Steps for the final ML project  

## Step 1: Choose/Prepare/Present Your Dataset

Select any suitable **regression** dataset (Do not select datasets already discussed in our Machine Learning lectures or exercises: grades will be lower otherwise).

Public sources such as Kaggle.com are allowed. You can also take your own data, but pay attention to the points below.

Make sure the dataset has:

- Enough samples
- Clear input features
- At least one continuous target variable

Be sure to clearly explain your dataset (features and target).

Show any data cleaning used:

- Did you remove outliers? How? 
- Did you apply any encoding? How?

Show histograms of your features and target. In case there are more than 10 features, show the histogram of the first 10 features. If your target has not a gaussian distribution (e.g., exponential distribution), discuss eventual target transformations applied. 


## Step 2: Train–Test Split

Split your dataset into:

- 80% Training set
- 20% Test set

Do **NOT** use the test set for:

- Model selection
- Hyperparameter tuning
- Cross-validation

The test set must only be used for the final evaluations (Steps 5 and 9).

Show on the same plot the histograms of the target property of the training and test sets (use different colors, don't forget to add the legend in the plot).

## Step 3: Train and Screen Models

You must test at least the following regression models:

- Random Forest
- Support Vector Regression
- k-Nearest Neighbors (use k = 1, 3 and 5)
- LASSO
- Gaussian Processes (make sure the kernel parameters are optimized)

#### Model Screening

- Use 5-fold Cross-Validation (CV) only on the training set
- Optimize hyperparameters if needed (show the final hyperparameters and their adopted ranges, if applicable)
- Do not forget to appropriately preprocess your dataset (which scaler did you use and why?)


## Step 4: Evaluate Model Performance

During model screening, report the following metricsi averaged over the validation folds (do not forget the standard deviation):

- MAE (Mean Absolute Error)
- MSE (Mean Squared Error)
- R² (Coefficient of Determination)

Compare all models (show a bar plot comparing the metrics of all investigated models) and select the best one based on the lowest error.

- Compare the individual percentage variations of MAE and R² over all screened ML models (e.g., "The MAE of the best model is 50% lower than that of the worst model, the R² of the best model is ..."): Would R² have been a better metrics (instead of MAE) to help choose the best ML model? Why?


## Step 5: Final Test Evaluation

After selecting the best model:

1. Retrain the model using the full training set
2. Evaluate it once on the test set

Show:

- Parity plot (Predicted vs. True values)
- Performance metrics on the title of the plot
- Bar plot with the feature importances (use e.g. the permutation importance method)


## Step 6: Training Performance

After selecting the best model:

1. Retrain the model using the full training set
2. Evaluate it once on the same training set

Show:

- Parity plot
- Performance metrics on the title of the plot


## Step 7: Overfitting Analysis

Show the parity plots (side-by-side) obtained in Steps 5 and 6 above to compare:

- Training error
- Test error

Discuss:

- Is the model overfitting?
- Is it underfitting?
- Why?


## Step 8: Model Variance

To evaluate model stability:

- Use the best screened model
- Apply repeated 5-fold CV on the training set only
- Use 10 different random seeds

Report for the validation folds:

- Average MAE
- Standard deviation of MAE

Discuss these results in terms of model stability/robustness.


## Step 9: Ensemble Model

- Select the best two or three individual ML models screened in Step 3
- Build a simple ensemble model using the selected ML models (for example, by averaging their predictions)

Compare:

- Ensemble performance evaluated on the test set
- Best individual model performance also evaluated on the test set

Discuss advantages and disadvantages of your ensembling approach. How to improve your ensemble model?


## Grading Criteria

The project and presentation will be assessed on the following:

- Have all project requirements been addressed?
- Is the code well structured and split into the different Steps described above?
- Was the presentation clear and finished on time?
- Were the final Jupyter notebook + dataset files submitted before the deadline?
- Were the questions answered satisfactorily?

> **NOTE**: A second evaluator will be present during the presentations


### Good Practice

- Keep your work reproducible (fix and report random seeds)
- Explain your decisions
- Use clear plots and labels
- Practice your presentation timing


### Common Mistakes to Avoid

- Using the test set during model tuning/training
- Missing preprocessing steps
- Not explaining methods clearly
- Poorly labeled figures
- Not respecting the presentation time limit
- Not addressing the 9 steps described above
