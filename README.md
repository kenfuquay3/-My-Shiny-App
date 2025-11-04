install.packages("rsconnect")
library(rsconnect)

---
title: "Tree Volume Estimator Pitch"
author: "Kenzie Fuquay"
output: ioslides_presentation
runtime: shiny
---

## Slide 1: Introduction

This app predicts tree volume based on girth using a simple linear regression.

Built using R's built-in `trees` dataset.

Deployed via RStudio’s shinyapps.io and GitHub.

---

## Slide 2: What the App Does

- Users input a tree’s girth (in inches)
- The app predicts its volume
- Displays:
  - A scatterplot of the dataset
  - A regression line (optional)
  - A predicted volume value

---

## Slide 3: The Data

We're using R’s built-in `trees` dataset:

```{r}
summary(trees)


## How to Use

1. **Choose Girth**: Use the slider to select the tree's girth in inches.
2. **Toggle Regression Line**: Check or uncheck the box to display the regression line.
3. **View Prediction**: The app shows the predicted volume and a visualization.

This app is useful for understanding simple linear regression and making quick volume predictions from field measurements.

## Dataset

The app uses the base R `trees` dataset, which contains measurements of the girth, height, and volume of 31 black cherry trees.
It includes:

Girth (inches)

Height (ft)

Volume (cubic ft)

---

## Slide  4: The Model

Simple linear regression:
model <- lm(Volume ~ Girth, data = trees)
coef(model)

---

## Slide 5: Access the App

Try the app here

See the source code on GitHub



