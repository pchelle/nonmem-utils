# nonmem-utils

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)

A toolbox of shiny apps to preview, investigate and report output files exported by Nonmem.

> [!CAUTION]
> This repository is currently under development

> [!IMPORTANT]
> The Shiny Apps below require the following packages to be installed on RStudio

```r
install.packages(c("tidyverse", "GGally", "DT", "shiny", "miniUI", "shinyWidgets", "bslib", "shinydashboard", "plotly", "mrgsolve", "pmplots"))
```

Exporting word reports uses the following packages that may also need to be installed

```r
install.packages(c("flextable", "officedown", "ragg"))
```

## Usage

This repo is a toolbox shiny app helping you out with Nonmem modeling and reporting:

```r
shiny::runGitHub(repo = "nonmem-utils", username = "pchelle", ref = "main")
```

### Check Input PK dataset

The app requires you to load a csv dataset that uses a Nonmem format and a csv dictionary that maps and labels the variables of the dataset.

```r
shiny::runGitHub(repo = "nonmem-utils", subdir = "dataset-analysis", username = "pchelle", ref = "main")
```

> [!TIP]
> A template of the csv dictionary is available [here](dataset-analysis/www/template_mapping.csv).
> You can also download the template from within the app.

### Compare Model Runs

The app requires you to indicate a directory on which all the `.res` files will be parsed and summarized.

### Model Fit

The app requires you to load a `.tab` file exported from Nonmem and a csv dictionary that maps and labels the variables of the dataset.

```r
shiny::runGitHub(repo = "nonmem-utils", subdir = "model-fit", username = "pchelle", ref = "main")
```

### Check Model Parameters

The app requires you to load a table file exported from Nonmem and 
a csv metadata file that maps the variables of the dataset.

### Check Optimization Profile

The app requires you to load an `.ext` file exported from Nonmem.

```r
shiny::runGitHub(repo = "nonmem-utils", subdir = "optimization-profile", username = "pchelle", ref = "main")
```

### Visual Predictive Check

The app requires you to load a `.tab` file exported from Nonmem and 
a csv metadata file that maps the variables of the dataset.
The first step of this app creates a `.csv` that you can re-use to speed up the processing of the VPC output file.

### Bootstrap Analysis

TODO
