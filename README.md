
<!-- README.md is generated from README.Rmd. Please edit that file -->

# NHS-R Theme <a alt="NHS-R Community's logo" href="https://nhsrcommunity.com/"><img src="https://nhs-r-community.github.io/assets/logo/nhsr-logo.png" align="right" height="80" /></a>

<!-- badges: start -->

[![R build
status](https://github.com/nhs-r-community/NHSRtheme/workflows/R-CMD-check/badge.svg)](https://github.com/nhs-r-community/NHSRtheme/actions)
<!-- badges: end -->

This is my personal edit of the package to give large xaringan slide text and add my own org's logo. Install it with `remotes::install_github('ChrisBeeley/NHSRtheme')`.

This repo attempts to build an R package that can provide themes to
ggplot for producing charts that follow the [NHS
Identity](https://www.england.nhs.uk/nhsidentity/).

## Examples

``` r
library(ggplot2)
library(NHSRtheme)
df <- data.frame(x = c("a", "b", "c", "d"), y = c(3, 4, 1, 2))
bars <- ggplot(df, aes(x, y, fill = x)) + 
    geom_bar(stat = "identity") + 
    labs(x = NULL, y = NULL) +
    theme(legend.position = "none")
```

``` r
bars + scale_fill_nhs()
```

![](man/figures/README-default_bars-1.png)<!-- -->

``` r
bars + scale_fill_nhs(palette = 'blues')
```

![](man/figures/README-blues_bars-1.png)<!-- -->

``` r
bars + scale_fill_nhs(palette = 'neutrals') 
```

![](man/figures/README-neutral_bars-1.png)<!-- -->

``` r
bars + scale_fill_nhs(palette = 'support greens')
```

![](man/figures/README-green_bars-1.png)<!-- -->

``` r
df2 <- data.frame(x = c("a", "b", "c", "d", "e", "f" ,"g", "h"), 
                  y = c(3, 4, 1, 2, 5, 9, 7, 4))

bars2 <- ggplot(df2, aes(x, y, fill = x)) + 
    geom_bar(stat = "identity") + 
    labs(x = NULL, y = NULL) +
    theme(legend.position = "none")

bars2 + scale_fill_nhs(palette = 'highlights')
```

![](man/figures/README-highlights_bars-1.png)<!-- -->
