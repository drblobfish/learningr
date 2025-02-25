
<!-- README.md is generated from README.Rmd. Please edit that file -->

# learningr

<!-- badges: start -->

[![binder](https://github.com/mahendra-mariadassou/learningr/workflows/binder/badge.svg)](https://mybinder.org/v2/gh/mahendra-mariadassou/learningr/master)
<!-- badges: end -->

The goal of learningr is to provide interactive tutorials for the
statistics classes given by Tristan for UE 2.3. The tutorial are
shamelessly taken from
[rstudio-education](https://rstudio.cloud/learn/primers) for the basics
of R and the tidyverse. Tutorials are packaged so you can install them
on you computer and do the exercices without access to an internet
connection.

## Installation

### Local installation

You only need to perform each of the following steps **once**:

  - installing **R**
  - installing **Rstudio**
  - installing **R** packages `remotes` and `learnr`

However each of them may take some time.

#### Installing R

Go to the CRAN [webpage](https://cran.r-project.org/), select your OS
and follow the instructions.

  - On Windows, you should just download and execute an .exe file.
  - On MacOS, you should just download and execute a .pkg file.
  - On Linux, you can get install R from the command line using
    something like

<!-- end list -->

``` bash
## If you're on Ubuntu
sudo apt-get install r-base
```

#### Installing RStudio Desktop

Go to the
[download](https://rstudio.com/products/rstudio/download/#download)
page. Select, download and install the file corresponding to your OS.

#### Installing R packages

Launch Rstudio (by clicking on the corresponding icon) and execute the
following commands in the console

``` r
install.packages("remotes") 
install.packages("learnr") 
```

On **Windows**: you may need **Rtools** and **git**

  - **Rtools**: visit the dedicated
    [page](https://cran.r-project.org/bin/windows/Rtools/), download the
    suggested exe and install it on your computer
  - **git**: visit the dedicated
    [page](https://git-scm.com/download/win), download the suggested exe
    and install it on your computer

On **MacOS**: you may need **XCode**

  - **XCode**: visit the dedicated
    [page](https://mac.r-project.org/tools/), download the **Mandatory
    tools** and install them on your computer

#### Installation (II)

You need to install the tutorials **every time** there is an update
(hopefully not too often)

### Installing the tutorials

You can install the tutorials from [GitHub](https://github.com/) by
launching Rstudio and typing the following command in the console:

``` r
remotes::install_github("mahendra-mariadassou/learningr")
```

Alternatively, you can use a remote R session to complete the tutorial
by launching binder:
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/mahendra-mariadassou/learningr/master?urlpath=rstudio)

You only need a web browser, no account or anything and the tutorials
will always be up to date. The main drawbacks of this solution (compared
to the previous one) are that (i) you lose your progress each time you
launch a new session and (ii) the binder image may take some time to
launch (usually a few minutes).

## Starting a tutorial

This package is intended for use with `learnr`:

``` r
library(learnr)
```

You should only launch **one** tutorial at the time. Before launching a
new tutorial, **restart R**.

### Basics of programmings

``` r
## Launch only one tutorial at the time!!
learnr::run_tutorial("01_programming_basics", package = "learningr")
learnr::run_tutorial("03_visualisation_basics", package = "learningr")
```

### R and stats

``` r
learnr::run_tutorial("02.1_random_variables", package = "learningr")
learnr::run_tutorial("02.2_classical_distributions", package = "learningr")
learnr::run_tutorial("02.3_bivariate_statistics", package = "learningr")
```

### Data visualization

``` r
learnr::run_tutorial("04.1_exploratory_data_analysis", package = "learningr")
learnr::run_tutorial("04.2_barcharts", package = "learningr")
learnr::run_tutorial("04.3_histograms", package = "learningr")
learnr::run_tutorial("04.4_boxplots", package = "learningr")
learnr::run_tutorial("04.5_scatterplots", package = "learningr")
learnr::run_tutorial("04.6_linegraphs", package = "learningr")
```

## Data manipulation

``` r
learnr::run_tutorial("05.1_tibbles", package = "learningr")
learnr::run_tutorial("05.2_isolating_data", package = "learningr")
learnr::run_tutorial("05.3_summaries", package = "learningr")
```

### Estimation and confidence intervals

``` r
learnr::run_tutorial("06.1_sampling", package = "learningr")
learnr::run_tutorial("06.2_testing", package = "learningr")
```

## Tidy data

``` r
learnr::run_tutorial("07.1_reshape_data", package = "learningr")
learnr::run_tutorial("07.2_separate_columns", package = "learningr")
learnr::run_tutorial("07.3_join_datasets", package = "learningr")
```

## Troubleshooting

If you have an error when launching a vignette (it may happen on Windows
with R 4.0.0), try this syntax (illustrated on the first vignette):

``` r
rmarkdown::run(file = NULL, 
               dir = learnr:::get_tutorial_path("01_programming_basics",  
                                                package = "learningr"), 
               shiny_args = list(launch.browser = 1))
```
