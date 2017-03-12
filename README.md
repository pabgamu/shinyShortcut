
<!-- README.md is generated from README.Rmd. Please edit that file -->
shinyShortcut
=============

[![Travis Build Status](https://travis-ci.org/Ewan-Keith/shinyShortcut.svg?branch=master)](https://travis-ci.org/Ewan-Keith/shinyShortcut) [![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/Ewan-Keith/shinyShortcut?branch=master&svg=true)](https://ci.appveyor.com/project/Ewan-Keith/shinyShortcut) [![codecov](https://codecov.io/gh/Ewan-Keith/shinyShortcut/branch/master/graph/badge.svg)](https://codecov.io/gh/Ewan-Keith/shinyShortcut)

[![Travis Build Status](https://travis-ci.org/Ewan-Keith/shinyShortcut.svg?branch=master)](https://travis-ci.org/Ewan-Keith/shinyShortcut)
[![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/Ewan-Keith/shinyShortcut?branch=master&svg=true)](https://ci.appveyor.com/project/Ewan-Keith/shinyShortcut)
[![codecov](https://codecov.io/gh/Ewan-Keith/shinyShortcut/branch/master/graph/badge.svg)](https://codecov.io/gh/Ewan-Keith/shinyShortcut)

Overview
--------

This package allows users to create a shortcut for their shiny app that, when ran, will launch the app directly in the default browser. No need to navigate to the correct working directory in R (or even to open R at all!). Simply run the shortcut and the app will fire up. Tested for both windows and unix OS'.

Package wholly inspired by [this blog post](http://www.mango-solutions.com/wp/2017/03/shiny-based-tablet-or-desktop-app/) by Mark Sellors at Mango Solutions.

Installation
------------

``` r
# Package not yet on CRAN, needs installed from Github:
# install.packages("devtools")
devtools::install_github("ewan-keith/shinyShortcut")
```

Usage
-----

The package loads just a single function, also named `shinyShortcut()`. It takes three arguments:

-   `shinyDirectory`: The home directory of your shiny app (that contains your `server.r`, `ui.r`, or `app.r` files).
-   `OS`: The operating system for the app to be ran on, must be `"windows"` or `"unix`.
-   `gitIgnore`: Whether to update the `.gitignore` file to prevent the shortcut files being uploaded to github when pushing new commits.

When the `shinyDirectory` is the current working directory then the default options should run fine.

``` r
library(shinyShortcut)

shinyShortcut()
```