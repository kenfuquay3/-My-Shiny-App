# Tree Volume Estimator Pitch

This repository contains an interactive ioslides presentation (R Markdown) that demonstrates a simple linear regression to predict tree volume from girth using R's built-in `trees` dataset.

Live demo
- If deployed: (add your shinyapps.io URL here)

Source
- Presentation source: presentation.Rmd

How to run locally
1. Install required packages:
   ```r
   install.packages(c("rmarkdown", "shiny", "rsconnect"))
   ```
2. In RStudio, open `presentation.Rmd` and click "Run Document" to view locally (or use rmarkdown::run()).
3. To deploy to shinyapps.io, use rsconnect::deployApp() or the RStudio Publish button.

Notes
- The presentation is an R Markdown (ioslides) document with runtime: shiny. For deployment as an interactive app, keep it as `.Rmd` and deploy that file (not the README).
