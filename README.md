
<!-- README.md is generated from README.Rmd. Please edit that file -->

# OpenCaseStudies

<!-- badges: start -->

[![Build
Status](https://travis-ci.org/opencasestudies/ocs-police-shootings-firearm-legislation.svg?branch=master)](https://travis-ci.org/opencasestudies/ocs-police-shootings-firearm-legislation)
<!-- badges: end -->

### License

This case study is part of the [OpenCaseStudies]() project. This work is
licensed under the Creative Commons Attribution-NonCommercial 3.0 ([CC
BY-NC 3.0](https://creativecommons.org/licenses/by-nc/3.0/us/)) United
States License.

### Citation

To cite this case study:

Stephens, Alexandra and Jager, Leah and Taub, Margaret and Hicks,
Stephanie. (2019, February 14).
opencasestudies/ocs-police-shootings-firearm-legislation: Firearm
Legislation and Fatal Police Shootings in the United States (Version
v1.0.0). Zenodo.
<http://doi.org/10.5281/zenodo.2565249>

[![DOI](https://zenodo.org/badge/151612152.svg)](https://zenodo.org/badge/latestdoi/151612152)

### Title

Firearm Legislation and Fatal Police Shootings in the United States (A
recreation of the study found at
<https://ajph.aphapublications.org/doi/suppl/10.2105/AJPH.2017.303770>).

### Motivating question

Is stricter firearm legislation associated with rates of fatal police
shootings?

### Data

All data is grouped at the state level. The following are the main
variable for the analysis:

  - The Brady Center state-level firearm legislation
    [“scorecard”](http://crimadvisor.com/data/Brady-State-Scorecard-2015.pdf)
    for 2015.
  - [The
    Counted](https://www.theguardian.com/us-news/ng-interactive/2015/jun/01/about-the-counted)
    is a project by The Guardian dedicated to counting the number of
    people in the United Stated killed by police or other law
    enforcement in 2015 and 2016.

The following data is collected to control for potential covariates (at
the state level) including median age, population density, violent crime
rate, gun ownership, percent male, percent white, percent black, percent
hispanic, unemployment rate, and education.

  - United States Census Bureau: State Population by Characteristics:
    [2010-2017](https://www.census.gov/content/census/en/data/tables/2017/demo/popest/state-detail.html)
  - FBI’s Uniform Crime Report: [Crime in the United States by
    State 2015](https://ucr.fbi.gov/crime-in-the-u.s/2015/crime-in-the-u.s.-2015/tables/table-5)
  - United States Bureau of Labor Statistics (BLS): [Unemployment Rates
    for States 2015 Annual
    Averages](https://www.bls.gov/lau/lastrk15.htm)
  - United States Census Bureau: [Land
    Area](https://www.census.gov/support/USACdataDownloads.html#LND)

### Analysis

The bulk of the analysis is collecting, cleaning, manipulating and
merging data.

  - dplyr is used to filter and group data and calculate relevant
    statistics by state (group\_by, tally, filter, summarize, select)
  - rvest is used to create a web scraper & retrieve the unemployment
    data from the BLS.

The statistical analysis involves Poisson regression and statistical
significance tests, which will be completed shortly.

### Other notes and resources

Again, we make no claims to the results or findings of this study, as we
are recreating the American Journal of Public Health study, “Firearm
Legislation and Fatal Police Shootings in the United States” found at
<https://ajph.aphapublications.org/doi/suppl/10.2105/AJPH.2017.303770>.
