# Resources for PS200E - `R` review

Caleb Ziolkowski
9/25/2019

Here I've gathered a few things together for our `R` review session. Please have a look through this document to make sure you're ready and we can avoid spending most of our time on installation issues. 

## Installing `R`/`RStudio`

The first order of business is to make sure you have `R` and `RStudio` up and running. If you do not have these set up, do the following, in order.
1. Install `R`.
2. Install `RStudio`.

### Install `R`

**For Windows:** 
1. Download the binary setup file for `R` [here](https://cran.r-project.org/bin/windows/base/).
2. Open the downloaded `.exe` file and Install `R`.

**For Mac:** 
1. Download the appropriate version of `.pkg` file [here](https://cran.r-project.org/bin/macosx/).
2. Open the downloaded `.pkg` file and Install `R`.

**For Linux:**
1. For a complete `R` system installation, try [this](https://cran.r-project.org/bin/linux/ubuntu/README).
2. For Ubuntu with Apt-get installed, execute _sudo apt-get install r-base_ in terminal.

### Install `RStudio`

Go [here](https://rstudio.com/products/rstudio/download/) and get the right installer for your platform. Run the downloaded installer, following the instructions. Open `RStudio` and make sure everything seems kosher. In the `Console` type something like 

```
rnorm(5)
```

to confirm that things are probably as they should be. 

## Install some packages

There are a few different packages that will show up in the review session. I suggest you install them ahead of time. Priority should be given to `tidyverse`.

```
install.packages('tidyverse')
```

You may also need to install `haven`. In addition, I will go over `pivot_wider()`, which is in the development version of `tidyr`. If you'd like to try this updated version of `spread()` tomorrow, install the development version using the code below.

```
install.packages('haven')
install.packages("remotes")
remotes::install_github("tidyverse/tidyr") 
```

We will briefly use `estimatr` tomorrow. We will use this package a lot in the future. I found that the behavior of the latest version was ideal, which can be installed with the following code. 

```
install.packages("estimatr", dependencies = TRUE,
                 repos = c("http://r.declaredesign.org", 
                           "https://cloud.r-project.org"))
```

Likewise, all the following packages will make an appearance.

```
install.packages('gapminder')
install.packages('broom')
install.packages('magrittr')
```
## Using Projects

Lastly, we're going to use `Projects` in `RStudio`. Have a look at [this](https://r4ds.had.co.nz/workflow-projects.html) to get an idea for what `Projects` do and how to use them. Tomorrow, when we start, we will open a new project with its own directory--you will need to pay attention to where exactly you put this directory. I will have a `.Rmd` that you can then move into the project directory. From there, it will be smooth sailing. :fingers_crossed:
