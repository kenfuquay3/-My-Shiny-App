# -My-Shiny-App
 My Shiny App
 rmarkdown::render("pitch.Rmd")
 
 file.rename("pitch.html", "index.html")

slidify("index.Rmd")

 git checkout --orphan gh-pages
git rm -rf .

library(slidify)
library(slidifyLibraries)
publish('gh-pages')

touch .nojekyll

git checkout --orphan gh-pages
git rm -rf .
touch .nojekyll
git add index.html
git commit -m "Deploy ioslides presentation"
git push origin gh-pages
---
title: "Pitch: My Shiny App"
author: "Kenzie Fuquay"
date: "`r Sys.Date()`"
output: ioslides_presentation
---

## Slide 1: Introduction

Welcome to my pitch!  
This Shiny app helps users interactively explore data using R.

---

## Slide 2: The Problem

Many users struggle to visualize trends in real-time data.  
Our app provides an intuitive interface for exploring datasets with live feedback.

---

## Slide 3: The App

The app takes user input via a slider and plots a histogram of eruption waiting times from the `faithful` dataset.  
Here's a sample of what the output looks like:

```{r, echo=FALSE}
hist(faithful$waiting, col = 'skyblue', main = "Histogram of Waiting Times")
sidebarPanel(
  sliderInput("bins", "Number of bins:", min = 1, max = 50, value = 30)
)
output$distPlot <- renderPlot({
  x <- faithful[, 2]
  bins <- seq(min(x), max(x), length.out = input$bins + 1)
  hist(x, breaks = bins, col = 'gray', border = 'white')
})


