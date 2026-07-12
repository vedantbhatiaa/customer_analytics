# Customer Analytics & Targeting Pipeline
**R | dplyr | K-means | Decision Tree | Random Forest | RFM Analysis**

An end-to-end customer analytics pipeline performing RFM segmentation, 
unsupervised clustering, supervised response modelling, and ROI-optimised 
targeted marketing across 5,000 customer records.


## Overview

This project builds a complete customer targeting framework for an 
e-commerce business, moving from descriptive segmentation through to 
predictive modelling and ROI measurement. The analysis compares three 
targeting approaches — RFM quintile segmentation, K-means clustering, 
and decision tree / random forest classification — evaluating each on 
marketing ROI against a blanket mailing baseline.


## Key Skills Demonstrated

- **EDA & descriptive analytics** — summary statistics, correlation 
  analysis, distribution profiling across RFM variables
- **RFM segmentation** — 125-segment quintile framework using dplyr, 
  with average response rate computed per segment
- **K-means clustering** — elbow method for optimal k, scaled 
  preprocessing, cluster profiling and response rate analysis
- **Supervised learning** — decision tree (rpart) and random forest 
  (ranger) trained on RFM predictors with probability = TRUE
- **Model evaluation** — break-even response rate, ROI comparison 
  across all four targeting strategies
- **Statistical judgment** — interpreting correlation matrices, 
  understanding bias-variance tradeoff, model selection rationale
- **Business recommendations** — structured analytical conclusions 
  translated into actionable targeting decisions


## Methods & Tools

| Task | Package / Method |
|---|---|
| Data wrangling | dplyr, tidyverse |
| Summary statistics | modelsummary, datasummary_skim |
| RFM segmentation | dplyr::ntile(), group_by(), mutate() |
| K-means clustering | stats::kmeans(), factoextra::fviz_nbclust() |
| Decision tree | rpart, rpart.plot |
| Random forest | ranger (num.trees = 2000, probability = TRUE) |
| Model summary | broom::tidy(), modelsummary |


## Results Summary

| Targeting Method | ROI |
|---|---|
| Blanket mailing (baseline) | -21.9% |
| RFM quintile targeting | +39.8% |
| K-means cluster targeting | +22.2% |
| Decision tree targeting | +67.8% |
| Random forest targeting | +49.4% |

The decision tree achieved the highest ROI by directly learning 
response behaviour from training data, outperforming unsupervised 
approaches that cluster on RFM patterns without reference to the 
outcome variable.

## Key Finding

Among all models tested, the supervised decision tree produced the 
strongest ROI (+67.8%) by identifying customers whose predicted 
subscription probability exceeded the break-even threshold of 21.46%. 
This demonstrates that outcome-aware supervised models consistently 
outperform behaviour-based unsupervised segmentation for targeted 
marketing applications.


## Academic Context

Completed as part of MSIN0094 — Marketing Analytics, MSc Business 
Analytics, UCL School of Management, 2024/25.
