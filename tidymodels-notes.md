# {tidymodels}: Notes
[Jim Tyhurst](https://www.jimtyhurst.com)  
Revised: 2021-09-11

**Contents**

* [Books](#books)
* [Tutorials](#tutorials)
* [Sample Analyses](#sample-analyses)
* [Blog Posts](#blog-posts)
* [Package Documentation](#package-documentation)
* [Tidymodels Packages](#tidymodels-packages)

---

## Books
* Max Kuhn and Julia Silge. 2021-09-08. [Tidy Modeling with R](https://www.tmwr.org/).


## Tutorials
* Julia Silge. [Supervised Machine Learning Case Studies in R](https://supervised-ml-course.netlify.app/): A Free, Interactive Course Using Tidy Tools.
* Tom Mock. 2020-10-24. [Intro to tidymodels with nflfastR](https://cmsac-tidymodels.netlify.app/).
    * [source code](https://github.com/jthomasmock/nfl-workshop)
* Alison Hill. 2020-08-27. [Tidymodels, Virtually](https://tmv.netlify.app/site/).
* Alison Hill. 2020-01-28. [Introduction to Machine Learning with the Tidyverse](https://conf20-intro-ml.netlify.app/).
    * [source code](https://github.com/rstudio-education/tidymodels-virtually).


## Sample Analyses
* Emil Hvitfeldt and Julia Silge. 2021-07-28. [Supervised Machine Learning for Text Analysis in R](https://smltar.com/).
* Emil Hvitfeldt. [ISLR tidymodels Labs](https://emilhvitfeldt.github.io/ISLR-tidymodels-labs/index.html).
    * "This book aims to be a complement to the 2nd version of [An Introduction to Statistical Learning](https://www.statlearning.com/) book with translations of the labs into using the [tidymodels](https://www.tidymodels.org/) set of packages."
    * [source code](https://github.com/EmilHvitfeldt/ISLR-tidymodels-labs), using the [tidyverse style guide](https://style.tidyverse.org/).
    * I love the idea of this book, because [An Introduction to Statistical Learning](https://www.statlearning.com/) is such a great book and so widely quoted, but Hvitfeldt reinterprets the problems with {tidymodels}, providing a great way to get familiar with {tidymodels}.



## Blog Posts
* Julia Silge. 2021-09-01. [Fit and predict with tidymodels for #TidyTuesday bird baths in Australia](https://juliasilge.com/blog/bird-baths/).
* Julia Silge. 2021-08-24. Use tidymodels workflowsets to predict human/computer interactions from Star Trek. [Video](https://www.youtube.com/watch?v=_gVHRqz8GIE). 
* David Robinson. 2021-07-21. [Machine learning in a hurry: what I've learned from the SLICED ML competition](http://varianceexplained.org/r/sliced-ml/).
* Julia Silge. 2020-05-21. [Tune XGBoost with tidymodels and #TidyTuesday beach volleyball](https://juliasilge.com/blog/xgboost-tune-volleyball/)
* Joseph Rickert. 2020-04-21. [The Case for tidymodels](https://rviews.rstudio.com/2020/04/21/the-case-for-tidymodels/).
* Rebecca Barter. 2020-04-14. [Tidymodels: tidy machine learning in R](https://www.rebeccabarter.com/blog/2020-03-25_machine_learning/).
    * Works through an analysis of diabetes in Pima Indians from a [{mlbench}](https://CRAN.R-project.org/package=mlbench) dataset, training a random forest model from the [{ranger}](https://cran.r-project.org/package=ranger) package to predict {pos, neg} from 8 variables.
* Julia Silge. 2020-02-18. Hyperparameter tuning using tidymodels. [Video](https://www.youtube.com/watch?v=muf3-hrahHs).
* Julia Silge. 2020-02-05. [#TidyTuesday and tidymodels](https://juliasilge.com/blog/intro-tidymodels/).
* Edgar Ruiz. 2019-06-19. [A Gentle Introduction to tidymodels](https://rviews.rstudio.com/2019/06/19/a-gentle-intro-to-tidymodels/).


## Package Documentation
* [tidymodels.org](https://www.tidymodels.org/)
* [tidymodels package](https://cran.r-project.org/package=tidymodels) on CRAN.
* [source code](https://github.com/tidymodels)
* [Get started with {tidymodels}](https://www.tidymodels.org/start/)
* [Learn to solve specific problems](https://www.tidymodels.org/learn/)
    * [Perform Statistical Analysis](https://www.tidymodels.org/learn/statistics/)
    * [Create Robust Models](https://www.tidymodels.org/learn/models/)
    * [Tune, Compare, and Work with Your Models](https://www.tidymodels.org/learn/work/)
    * [Develop Custom Modeling Tools](https://www.tidymodels.org/learn/develop/)

## Tidymodels Packages
https://www.tidymodels.org/packages/

* [Core Packages](https://www.tidymodels.org/packages/#core-tidymodels)
    * [tidymodels](https://tidymodels.tidymodels.org/): meta-package for modeling and statistical analysis that share the underlying design philosophy, grammar, and data structures of the tidyverse.
    * [rsample](https://rsample.tidymodels.org/)
    * [parsnip](https://parsnip.tidymodels.org/)
    * [recipes](https://recipes.tidymodels.org/)
    * [workflows](https://workflows.tidymodels.org/)
    * [tune](https://tune.tidymodels.org/)
    * [yardstick](https://yardstick.tidymodels.org/)
    * [broom](https://broom.tidymodels.org/)
    * [dials](https://dials.tidymodels.org/)
* [Specialized Packages](https://www.tidymodels.org/packages/#specialized-packages)
    * Statistical Analysis
        * [infer](https://infer.tidymodels.org/): high-level API for tidyverse-friendly statistical inference.
        * [corrr](https://corrr.tidymodels.org/): tidy interfaces for working with correlation matrices.
    * Robust Models
        * [spatialsample](http://spatialsample.tidymodels.org/)
        * [discrim](https://discrim.tidymodels.org/)
        * [poissonreg](https://poissonreg.tidymodels.org/)
        * [plsmod](https://plsmod.tidymodels.org/)
        * [rules](https://rules.tidymodels.org/)
        * [baguette](https://baguette.tidymodels.org/)
        * [embed](https://embed.tidymodels.org/)
        * [textrecipes](https://textrecipes.tidymodels.org/)
        * [themis](https://themis.tidymodels.org/)
        * [tidypredict](https://tidypredict.tidymodels.org/)
        * [modeldb](https://modeldb.tidymodels.org/)
    * Tune, compare, and work with models
        * [stacks](https://stacks.tidymodels.org/)
        * [usemodels](https://usemodels.tidymodels.org/)
        * [probably](https://probably.tidymodels.org/)
        * [tidyposterior](https://tidyposterior.tidymodels.org/)
        * [butcher](https://butcher.tidymodels.org/)
        * [applicable](https://applicable.tidymodels.org/)
    * Develop custom modeling tools
        * [hardhat](https://hardhat.tidymodels.org/)

