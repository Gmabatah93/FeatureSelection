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

# Feature Selection

## Wrapper Methods
use an external search procedure to choose different subsets of the whole predictor set to evaluate in a model. This approach separates the feature search process from the model fitting process. _(i.e. backwards/stepwise selection and genetic algorithms)_

## Embedded Methods
feature selection procedure occurs naturally course of the model fitting process. Here an example would be a simple decision tree where variables are selected when the model uses them in a split. If a predictor is never used in a split, the prediction equation is functionally independent of this variable and it has been selected out.
