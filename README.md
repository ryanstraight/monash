
<!-- README.md is generated from README.Rmd. Please edit that file -->

# uarizona

<!-- badges: start -->
<!-- badges: end -->

The `uarizona` R-package is a utility package with consolidated tools and
templates for staffs at uarizona University. The package contains three
primary themes:

-   **workflow**: automating repetitive tasks, particularly teaching
    related activities;
-   **template**: uarizona branded R Markdown templates for teaching,
    presentation, etc; and
-   **data**: easy access to relevant information (may require access
    privileges).

## Installation

You can install `uarizona` R-package as below:

``` r
# install.packages("remotes")
remotes::install_github("numbats/uarizona")
```

## Get uarizona logo

You can get a copy of the logo into the directory you wish with below.

``` r
# default logo
uarizona::logo_get(path = "man/figures")
#> ✔ The 'uarizona-stacked-blue-rgb.png' is now in 'man/figures/'
#> man/figures/uarizona-stacked-blue-rgb.png
# black and white & one-line version of the logo
uarizona::logo_get(path = "man/figures", color = "black", stack = FALSE, filename = "uarizona-logo-black.png")
#> ✔ The 'uarizona-logo-black.png' is now in 'man/figures/'
#> man/figures/uarizona-logo-black.png
```

And then you can reference the logo file that you copied.

![](man/figures/uarizona-stacked-blue-rgb.png)
![](man/figures/uarizona-logo-black.png)

## Get uarizona brand colors

These are handy commands to quickly see uarizona brand colors and be able
to copy-and-paste the hex color codes.

``` r
uarizona::color_show()
```

<img src="man/figures/README-unnamed-chunk-2-1.png" width="100%" />

    #>      blue     black     white    gray80    gray50    gray10      blue    purple 
    #> "#006DAE" "#000000" "#FFFFFF" "#5A5A5A" "#969696" "#E6E6E6" "#027EB6" "#746FB2" 
    #>   fuchsia      ruby      pink       red    orange     umber     olive     green 
    #> "#9651A0" "#C8008F" "#ee64a4" "#EE0220" "#D93F00" "#795549" "#6F7C4D" "#008A25"

## Settings

(WIP) The uarizona package makes use of some values, listed below, from
your R profile. You can modify this by using `usethis::edit_r_profile()`
and adding below with values modified to your own values.

    options(uarizona.full_name = "Emi Tanaka",
            uarizona.email = "emi.tanaka@uarizona.edu",
            uarizona.orgunit = "Department of Econometrics and Business Statistics",
            uarizona.teaching_dir = "~/teaching/uarizona/",
            uarizona.workshop_dir = "~/workshop/")

## Teaching

(WIP) `create_teaching_directory("ETCXXXX")` would create a skeleton
directory with folder and file structure below for development of
teaching material. What is the advantage of this structure? It’s
designed to be synced with a private github repository and the materials
in the `release` folder are *automatically* pushed using Github
Repository to the public github repository for public release. The
website associated with it will be also be built automatically as well.
The website format will closely resemble [ETC5512: Wild-Caught
Data](https://wcd.numbat.space/).

(WIP) `release_tutorial(1)` moves `tutorial-01.html` (and .Rmd) to the
appropriate place in the `release` folder.

(WIP) Tutorial, slides and other templates for teaching.

    ├── ETCXXXX.Rproj
    ├── .git
    ├── data
    │   └── data01.csv
    ├── lectures
    │   ├── assets
    │   │   ├── uarizona-brand.css
    │   │   └── uarizona-font.css  
    │   ├── images
    │   │   ├── lecture-01-image01.png
    │   │   └── lecture-02-image01.png  
    │   ├── lecture-01.Rmd
    │   ├── lecture-02.Rmd
    │   └── lecture-03.Rmd
    ├── tutorials
    │   ├── images
    │   │   ├── tutorial-01-image01.png
    │   │   └── tutorial-02-image01.png 
    │   ├── tutorial-01.Rmd
    ├── assessments
    │   ├── assignment-01.Rmd
    │   └── quiz-01.Rmd
    ├── release # for public release
    │   ├── site
    │   │   └── _site.yml
    │   ├── data
    │   ├── lectures
    │   ├── tutorials
