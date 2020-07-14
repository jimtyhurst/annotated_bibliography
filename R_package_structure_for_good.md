# Step away from the notebook!
[Jim Tyhurst](https://www.jimtyhurst.com)<br>
2020-07-13

## References: Use the R package structure to organize your projects
* Ben Marwick, Carl Boettiger, Lincoln Mullen. 2018-03-20. [Packaging data analytical work reproducibly
using R (and friends)](https://peerj.com/preprints/3192/). [PDF](https://peerj.com/preprints/3192.pdf).
    * "The purpose of this paper is to show how the R package can be a suitable template for organising files into a research compendium to enhance the reproducibility of research."
* Anna Krystalli. 2018-10-31. [Manage functionality as a package](https://annakrystalli.me/rrtools-repro-research/package.html). This is part 3 of a 4 part workshop: [Reproducible Research in R with `rrtools`](https://annakrystalli.me/rrtools-repro-research/index.html).
    * Note: She gives bad advice about putting your data files in the `data/` directory. The convention for package structure is to put your raw data in the ['inst/extdata' directory](http://r-pkgs.had.co.nz/data.html). Only `*.Rda` files go in the `data/` directory.
* Denis Gontcharov. 2020-02-28. [Put your Data Analysis in an R Package — Even if You Don’t Publish it](https://towardsdatascience.com/put-your-data-analysis-in-an-r-package-even-if-you-dont-publish-it-64f2bb8fd791): How to leverage R's package development environment to organize, document and test your work.
    * Working on our analysis inside an R package offers four benefits:
        1. R packages provide a standardized folder structure to organize your files
        2. R packages provide functionality to document data and functions
        3. R packages provide a framework to test your code
        4. putting effort into points 1–3 enables you to reuse and share your code
* Edwin Thoen. 2020. [Agile Data Science with R: A workflow](https://edwinth.github.io/ADSwR/index.html). See [6.1 Using the R Package Structure](https://edwinth.github.io/ADSwR/code-organisation.html)
    * Highlights presented by Edwin Thoen at: Invited Speakers Session 1.  2020-06-17. "Building Agile data products leveraging the R package structure". [eRum 2020](https://2020.erum.io/). Individual talks have not been published separately yet, but this talk appears at 1:54:10 - 2:12:00 of the complete [Day 1 recording](https://www.youtube.com/watch?v=yHJ7RSv6nio).
* Colin Fay, et al. 2020-07-07. [Engineering Production-Grade Shiny Apps](https://engineering-shiny.org/). See [3.1 Shiny App as a Package](https://engineering-shiny.org/structure.html).

## References: R package structure
* Hadley Wickham. 2015. [R Packages](http://r-pkgs.had.co.nz/).
* Hadley Wickham, Jenny Bryan. in process. [R Packages, 2nd edition](https://r-pkgs.org/).
* Scott Chamberlain. 2018-10-01. [R package development workshop](https://portlandrusergroup.github.io/pkgdev/). Presented at [PDX RLang Meetup](https://www.meetup.com/portland-r-user-group/events/253797396/) on 2018-09-27.
* Maëlle Salmon. 2020-04-29. [Workflow automation tools for package developers](https://blog.r-hub.io/2020/04/29/maintenance/).
* Maëlle Salmon. 2020. [How to improve your R package: Automatically, and not](https://maelle.github.io/erum2020/index.html#1). Presented at [e-Rum 2020](http://2020.erum.io/) Invited Speakers Session 3. 2020-06-19. Individual talks have not been published separately yet, but this talk appears at 5:39:22 - 5:53:20 of the complete [Day 3 recording](https://www.youtube.com/watch?v=ZRGxTHRY_hs).
* [rOpenSci](https://ropensci.org/) software review editorial team. 2020-07-13. [rOpenSci Packages: Development, Maintenance, and Peer Review](https://devguide.ropensci.org/). See especially [Chapter 1. Packaging Guide](https://devguide.ropensci.org/building.html).

## References: workflow for R development and reproducibility
* Hilary Parker. 2017-08-30. [Opinionated analysis development](https://peerj.com/preprints/3210/). [PeerJ Preprints 5:e3210v1](https://doi.org/10.7287/peerj.preprints.3210v1). [PDF](https://peerj.com/preprints/3210v1.pdf).
* Edwin Thoen. 2020. [Agile Data Science with R: A workflow](https://edwinth.github.io/ADSwR/index.html).
* Riccardo Porreca, Peter Schmid, Andrea Melloncelli. 2020-06-20. Bring your R Application Safely to Production: Collaborate, Deploy, Automate. Workshop at [e-Rum 2020](https://2020.erum.io/program/workshops/).
    * [MLflow Documentation](https://mlflow.org/docs/latest/index.html).
* [Research Compendia](https://research-compendium.science/) web site has a "Resources" section with papers and talks that touch on templates and workflows for reproducible research.
