# Step away from the notebook!
## Use an R package to organize your project
[Jim Tyhurst](https://www.jimtyhurst.com)<br>
2020-07-15

I will give an overview of the advantages of using the R package structure for a data science project, even when you will never publish the package for reuse by others. I have a few discussion points about how package structure improves the development lifecycle. There is also a list of references with more details.

Topics that are only mentioned here, but really deserve their own full length discussion as good practices for software development of any type, including data science projects:

* Use source control.
* Write unit tests (and other types of tests).
* Automate a build process.

For now, we are just considering the advantages of using an R package to organize a project.

---

**Contents**

* [Advantages to using an R package for your project files](#advantages-to-using-an-r-package-for-your-project-files)
* [Disadvantages](#disadvantages)
* [Choosing whether to use a package structure](#choosing-whether-to-use-a-package-structure)
* [References: Use the R package structure to organize your projects](#references-use-the-r-package-structure-to-organize-your-projects)
* [References: R package structure](#references-r-package-structure)
* [References: workflow for R development and reproducibility](#references-workflow-for-r-development-and-reproducibility)

---

## Advantages to using an R package for your project files
* Access to automated tools
    * building
        * command line: `R CMD build`
        * RStudio: `Build > Install and Restart`
    * documenting
        * function documentation built during "build".
    * testing
        * unit testing while coding (`devtools::test()`).
        * automated Continuous Integration (CI) testing
            * CI build will run the unit tests.
    * checking (`devtools::check()`)
* A standard for where to store files.
    * R code (functions) in the `R/` directory.
    * R Markdown in the `vignettes/` directory.
        * Note: Some people put exploratory data analysis scripts or other R Markdown scripts in a top-level directory called `analysis/` or `research/`.
            * However, the package structure does not specify those other directories, so `devtools::check()` will give a `NOTE`: "Non-standard file/directory found at top level".
            * You can avoid the `NOTE` by adding the extra directory to the `.Rbuildignore` file.
            * So it is possible to override the standard form of the package structure, but you should have a good reason for doing so.
    * Metadata, data about your project:
        * A `README.md` displays by default on the home page of the project if you use one of the Git repository providers to store your project. e.g. [GitHub](https://github.com/), [GitLab](https://gitlab.com/), [BitBucket](https://bitbucket.org/), [Framagit](https://framagit.org/), etc.
            * Note: All of the Git repository providers allow you to have private repositories if you do not want to expose your work publicly.
        * Dependencies in the `DESCRIPTION` file.
        * A license should be specified in the `DESCRIPTION` file.
            * Depending on the license, you may also want a `LICENSE` file.
    * Data: It depends! See section [12. External data](https://r-pkgs.org/data.html) of [R Packages, 2nd edition](https://r-pkgs.org/):
        * `data/` directory is for binary data to be exposed as part of the package, such as the output of `save` or `saveRDS`. See `usethis::use_data()`.
        * `data-raw/` directory is for reproducibility. It includes original data and the scripts you used to transform it into the clean data that you expose in the `data/` directory. See `usethis::use_raw_data()`.
        * `inst/extdata/` for raw data, e.g. CSV files, used in vignettes.
        * `tests/testthat/` for small data files used for unit testing.
* Easy to share your code and analyses with others.
    * You write within a standardized structure, i.e. the package structure, so people know where to look for details, such as dependencies, the license, the reusable code, documentation of the code, the tests, and code with sample usage.
* Easier to track down integration errors when dependencies are upgraded.
    * While any code can have associated tests, the package structure makes it easy to set up automated unit testing. By focusing on small units of code, i.e. functions, with associated unit tests that are run automatically at certain steps in the development lifecycle, it is easier to track down errors that get introduced when dependencies are upgraded with breaking changes.
* Easier to use your own code! Rather than making sure you source files in the correct order, functions will be defined and usable within your environment when the package is loaded.
* Easy to deploy your code.
    * While any code can be deployed to a different machine, it is especially easy to use a package in a Docker image to deploy an application to a server.

## Disadvantages
* It takes some time and effort to learn package structure ... but automated tools make it easy to get started:
    * The {[usethis](https://usethis.r-lib.org/index.html)} package is very helpful.
    * The [R Packages, 2nd edition](https://r-pkgs.org/) book provides clear explanations. It is a great reference for getting started, as well as getting deeper into package structure.
* It takes some time to set up each new package. Even with the automated tools, you still need to enter your custom information. However, I am convinced that the benefit of package structure for improving developer workflow is much greater than this small cost of set-up.
* With a very large code base and corresponding tests, it may take some time to build the entire package. Although it makes for a simple workflow to rebuild with each code change, in practice that can become tedious when you are writing a very iterative sequence of changes.

## Choosing whether to use a package structure
Given some of the disadvantages, especially the overhead of creating a package and running frequent builds during development, what type of project is best suited to using a package structure?

For a simple analysis, e.g. doing exploratory data analysis, it might not be worth the effort to create a package for such a small project. However for projects with any of the following characteristics, the benefits will likely outweigh the costs:

* You are going to use the code in production, e.g. as a machine learning model for classification or prediction.
* You write some functions that are reused within different parts of your analysis or they will be reused by others.
    * Remember, if you copied and pasted a block of code 2 or 3 times, you really should be using a function with that code in one place instead of copying and pasting.
* Even if code blocks are not reused, it is often helpful to extract a code block into a function, which makes the code easier to read and maintain by yourself and others, because functions can be:
    * documented with standard documentation formatting; and
    * tested thoroughly with unit tests.
* You need to maintain the code over a period of time. Writing code in small functions with associated tests is easier to maintain. Also, if you write sufficient unit tests, this will help you to identify breaking changes when you upgrade a library on which you depend.
* More than one person is writing or maintaining the code. Extracting code blocks into functions accompanied by comprehensive unit tests makes it easier to enhance and maintain the code by multiple people while avoiding unintended side effects of code changes.

## References: Use the R package structure to organize your projects
* Ben Marwick, Carl Boettiger, Lincoln Mullen. 2018-03-20. [Packaging data analytical work reproducibly
using R (and friends)](https://peerj.com/preprints/3192/). [PDF](https://peerj.com/preprints/3192.pdf).
    * "The purpose of this paper is to show how the R package can be a suitable template for organising files into a research compendium to enhance the reproducibility of research."
* Denis Gontcharov. 2020-02-28. [Put your Data Analysis in an R Package — Even if You Don’t Publish it](https://towardsdatascience.com/put-your-data-analysis-in-an-r-package-even-if-you-dont-publish-it-64f2bb8fd791): How to leverage R's package development environment to organize, document and test your work.
    * Working on our analysis inside an R package offers four benefits:
        1. R packages provide a standardized folder structure to organize your files
        2. R packages provide functionality to document data and functions
        3. R packages provide a framework to test your code
        4. putting effort into points 1–3 enables you to reuse and share your code
* Emily Riederer. 2019-05-04. [RMarkdown Driven Development (RmdDD)](https://emilyriederer.netlify.app/post/rmarkdown-driven-development/). She explains how to convert from a single RMarkdown file to a project and then to a package.
* Emily Riederer. 2020-02-01. [RMarkdown Driven Development: the Technical Appendix](https://emilyriederer.netlify.app/post/rmddd-tech-appendix/). Discussion of tools for the technical implementation of each step for converting from a single RMarkdown file to a package.
* Anna Krystalli. March-April 2020. [Reproducible Research Data & Project Management in R](https://annakrystalli.me/rrresearchACCE20/). See especially the [Paths and Project structure](https://annakrystalli.me/rrresearchACCE20/path-proj-str.html) section.
    * An earlier workshop provides lots of good details too: Anna Krystalli. 2018-10-31. [Manage functionality as a package](https://annakrystalli.me/rrtools-repro-research/package.html). This is part 3 of a 4 part workshop: [Reproducible Research in R with `rrtools`](https://annakrystalli.me/rrtools-repro-research/index.html).
* Karl Broman. 2020-03-20. [R package primer](https://kbroman.org/pkg_primer/): a minimal tutorial. See especially the [Why write an R package?](https://kbroman.org/pkg_primer/pages/why.html) section.
* Edwin Thoen. 2020. [Agile Data Science with R: A workflow](https://edwinth.github.io/ADSwR/index.html). See [6.1 Using the R Package Structure](https://edwinth.github.io/ADSwR/code-organisation.html)
    * Highlights presented by Edwin Thoen at: Invited Speakers Session 1.  2020-06-17. "Building Agile data products leveraging the R package structure". [eRum 2020](https://2020.erum.io/). Individual talks have not been published separately yet, but this talk appears at 1:54:10 - 2:12:00 of the complete [Day 1 recording](https://www.youtube.com/watch?v=yHJ7RSv6nio).
* Colin Fay, et al. 2020-07-07. [Engineering Production-Grade Shiny Apps](https://engineering-shiny.org/). See [3.1 Shiny App as a Package](https://engineering-shiny.org/structure.html).


## References: R package structure
* Hadley Wickham. 2015. [R Packages](http://r-pkgs.had.co.nz/).
* Hadley Wickham, Jenny Bryan. in process. [R Packages, 2nd edition](https://r-pkgs.org/).
* Scott Chamberlain. 2018-10-01. [R package development workshop](https://portlandrusergroup.github.io/pkgdev/). Presented at [Portland R User Group](https://www.meetup.com/portland-r-user-group/events/253797396/) Meetup on 2018-09-27.
* Maëlle Salmon. 2020-04-29. [Workflow automation tools for package developers](https://blog.r-hub.io/2020/04/29/maintenance/).
* Maëlle Salmon. 2020. [How to improve your R package: Automatically, and not](https://maelle.github.io/erum2020/index.html#1). Presented at [e-Rum 2020](http://2020.erum.io/) Invited Speakers Session 3. 2020-06-19. Individual talks have not been published separately yet, but this talk appears at 5:39:22 - 5:53:20 of the complete [Day 3 recording](https://www.youtube.com/watch?v=ZRGxTHRY_hs).
* [rOpenSci](https://ropensci.org/) software review editorial team. 2020-07-13. [rOpenSci Packages: Development, Maintenance, and Peer Review](https://devguide.ropensci.org/). See especially [Chapter 1. Packaging Guide](https://devguide.ropensci.org/building.html).


## References: workflow for R development and reproducibility
* Hilary Parker. 2017-08-30. [Opinionated analysis development](https://peerj.com/preprints/3210/). [PeerJ Preprints 5:e3210v1](https://doi.org/10.7287/peerj.preprints.3210v1). [PDF](https://peerj.com/preprints/3210v1.pdf).
* Edwin Thoen. 2020. [Agile Data Science with R: A workflow](https://edwinth.github.io/ADSwR/index.html).
* Riccardo Porreca, Peter Schmid, Andrea Melloncelli. 2020-06-20. Bring your R Application Safely to Production: Collaborate, Deploy, Automate. Workshop at [e-Rum 2020](https://2020.erum.io/program/workshops/).
    * [MLflow Documentation](https://mlflow.org/docs/latest/index.html).
* Anna Krystalli. 2020-07-10. [Computational Reproducibility: from theory to practice](https://www.youtube.com/watch?v=KHMW8fV2NXo). Keynote lecture at useR! 2020.
* [Research Compendia](https://research-compendium.science/) web site has a "Resources" section with papers and talks that touch on templates and workflows for reproducible research.
* The Turing Way. [Guide for Reproducible Research](https://the-turing-way.netlify.app/reproducible-research/reproducible-research.html). See especially the [Reproducible environments](https://the-turing-way.netlify.app/reproducible-research/renv.html) section for useful principles, although examples are for Python, not R.
