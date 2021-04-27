<img src="Images/FittingProcess.PNG" width="600">

## Exploratory Visualizations
- Scatter Plots
- Pairwise Correlations
- Projection into a lower Dimension
- 1st Level Regression and Classification Trees
- Heatmap or Mosaic Plot for examining associations among Categorical Variables

_(Post model building, visual tools can be used to assess model lack-of-fit and to evaluate the potential effectiveness of new predictors that were not in the original model)_

### Numeric Data
**Histograms & BoxPlots**



# Feature Engineering
> process of creating representations of data that increase the effectiveness of a model

**Overfitting**: model fits very well to the current data but fails when predicting new samples
-  risk of this type of overfitting is especially dangerous when the number of data points (n), is small and the number of potential predictors (p) is very large

**No Free Lunch**: without any specific knowledge of the problem or data at hand, no one predictive model can be said to be the best.



**Model Bias and Variance**:

<img src="Images/Bias.PNG" width="300">

- Variance: describes the degree in which the values can fluctuate
- Bias: ability of a model to conform to the underlying theoretical structure of the data.
  + Low Bias: one that can be highly flexible and has the capacity to fit a variety of different shapes and patterns
  + High Bias: would be unable to estimate values close to their true theoretical counterparts

## Encoding Categorical Predictors
<img src="Images/Dummy.PNG" width="600">

- Create an "Other" category for rarely occuring predictors
- Feature Hashing: encoding predictors with many categories
- **Supervised Encoding Methods**
  + Effect / Likelihood Encoding: Mean of a certain category

## Engineering Numeric Predictors
- **Potential Problems**
  + Different scales
  + Skewed Distributions
  + Small number of extreme values
  + Complex relationship with the response and is truly predictive but cannot be adequately represented with a simple function or extracted by sophisticated models.
  + Contain relevant and overly redundant information. That is, the information collected could be more effectively and efficiently represented with a smaller, consolidated number of new predictors while still preserving or enhancing the new predictors’ relationship with the response.

### 1:1 Transformations
**BoxCox** _Can only be applied to data that is strictly positive_

<img src="Images/BoxCox.PNG" width="200">

**YeoJohnson**: can be used on any numeric data

**Log Transformation**

**Centering and Scaling**

### 1:Many Transformations
**Basis Expansion**:

<img src="Images/Basis.PNG" width="200">

**Splines**:

**Discretizing**:
- Potential Problems
  + extremely unlikely that the underlying trend is consistent with the new model.
  + when a real trend exists, discretizing the data is most likely making it harder for the model to do an effective job since all of the nuance in the data has been removed.
  + there is probably no objective rationale for a specific cut-point.
  + when there is no relationship between the outcome and the predictor, there is a substantial increase in the probability that an erroneous trend will be “discovered”

### Many:Many Transformations
**Principal Component Analysis**

**Independent Component Analysis**
It creates new components that are linear combinations of the original variables but does so in a way that the components are as statistically independent from one another as possible.
- no unique ordering of the components.

**Non-negative Matrix Factorization**

**Partial Least Squares**
 find linear functions (called latent variables) of the predictors that have optimal covariance with the response. This means that the response guides the dimension reduction such that the scores have the highest possible correlation with the response in the training data.

 **Spatial Sign**
 
 <img src="Images/SpatialSign.PNG" width="200">

# Feature Selection

## Wrapper Methods
use an external search procedure to choose different subsets of the whole predictor set to evaluate in a model. This approach separates the feature search process from the model fitting process. _(i.e. backwards/stepwise selection and genetic algorithms)_

## Embedded Methods
feature selection procedure occurs naturally course of the model fitting process. Here an example would be a simple decision tree where variables are selected when the model uses them in a split. If a predictor is never used in a split, the prediction equation is functionally independent of this variable and it has been selected out.
