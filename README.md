# Predicting_KC_Housing_Prices
Creating a prediction model for home prices in Kings County, WA
**Author**: Eric Roberts

## Overview

A one-paragraph overview of the project, including the business problem, data, methods, results and recommendations.

## Business Problem

Create a prediction model for the sale price of homes in Kings County, Washington.

***
Questions to consider:
* What are the business's pain points related to this project?
* How did you pick the data analysis question(s) that you did?
* Why are these questions important from a business perspective?
***

## Data

Data for this analysis is of home sales in Kings County, Washington over the past decade. The target variable is the sale price. Continuous features  included in the data set include the square footage of the living area, the lot, the basement and the above ground living area, as well as the mean square footage of the living area and lot of the nearest 15 neighbors.  The year the home was built and the year of renovation is included. Geographic information includes the latitue, the longitude and the zip code.  Categorical features of the home include the number of bedrooms, bathrooms and floors, whether the home is on the waterfront, and qualitative ratings of the home's amentities including the quality of the view, the condition of the home and the archetectural grade.

## Methods

Descriptive statistics and histograms were created for continuous variables to assess the distribution and evaluate measures of central tendency and dispersion.  Value counts were calculated for all categorical variables.  Scatterplots or box plots (as appropriate) were assessed between the sale price, and continuous and categorical features to visualize associations to determine cutpoints for the creation of categorical variables and to determine whether linear transformations of continuous variables were necessary. Bivariable tests of association (ANOVA and Pearon's Correlation Coefficient) were calculated to aid in this process.

A series of linear regressions were estimated on an 80:20 train-test split to assess model fit through a stepwise process.  A baseline conceptually derived model based on EDA was constructed and iterations including engineered features consisting of logarithmic transformations polynomials, and interactions.  Overfitting was assessed by comparing the RMSE of the model on the training and testing data.  Model prediction was assessed by comparing the adjusted R-sqaure and the RMSE of the test set model between models.

As a sensitivity analysis we constructed a model using a purely data driven approach.  To complete this we contructed all dummy variables for all possible categorical values, and constructed all second order polynomials and interactions possible given the variables using the PolynomialFeatures class in sklearn.preprocessing.  We selected the 110 best variables using the SelectKBest class in sklearn.feature_selection using the F-test as our criteria.  One hundred ten was chosen follwing the rule of thumb to avoid the curse of dimensionality - the square root of the training split rounded down to 110.

## Results

Present your key results. For Phase 1, this will be findings from your descriptive analysis.

***
Questions to consider:
* How do you interpret the results?
* How confident are you that your results would generalize beyond the data you have?
***

Here is an example of how to embed images from your sub-folder:

### Visual 1
![Figure 1](https://https://github.com/etr359/Predicting_KC_Housing_Prices/price by bedrooms boxplot.png)

## Conclusions

Provide your conclusions about the work you've done, including any limitations or next steps.

***
Questions to consider:
* What would you recommend the business do as a result of this work?
* What are some reasons why your analysis might not fully solve the business problem?
* What else could you do in the future to improve this project?
***

## For More Information

Please review our full analysis in [our Jupyter Notebook](./dsc-phase1-project-template.ipynb) or our [presentation](./DS_Project_Presentation.pdf).

For any additional questions, please contact **name & email, name & email**

## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── README.md                           <- The top-level README for reviewers of this project
├── dsc-phase1-project-template.ipynb   <- Narrative documentation of analysis in Jupyter notebook
├── DS_Project_Presentation.pdf         <- PDF version of project presentation
├── data                                <- Both sourced externally and generated from code
└── images                              <- Both sourced externally and generated from code
```
