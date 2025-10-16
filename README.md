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


