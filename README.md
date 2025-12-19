<p align="center">
  <img src="inst/hex/ggdatalab.png" width="200" alt="ggdatalab logo"/>
</p>

<!-- badges: start -->
[![R-CMD-check](https://github.com/kubdatalab/ggdatalab/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/kubdatalab/ggdatalab/actions/workflows/R-CMD-check.yaml)
[![pkgdown](https://github.com/kubdatalab/ggdatalab/actions/workflows/pkgdown.yaml/badge.svg)](https://github.com/kubdatalab/ggdatalab/actions/workflows/pkgdown.yaml)
[![Lifecycle: experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html)
<!-- badges: end -->

# ggdatalab

`ggdatalab` is a small **ggplot2 extension** that provides:

- a consistent theme (`theme_datalab()`)
- discrete and continuous colour scales built from a fixed palette
- simple palette helpers for reuse outside ggplot

The package is written to be **R CMD check clean** and suitable for CRAN submission.

---

## Installation

### CRAN

When available on CRAN:

```r
install.packages("ggdatalab")
```

### Development version (GitHub)

```r
install.packages("remotes")
remotes::install_github("kubdatalab/ggdatalab", build_vignettes = TRUE)
```

---

## Quick start

```r
library(ggplot2)
library(ggdatalab)

ggplot(mtcars, aes(wt, mpg, colour = hp)) +
  geom_point(size = 3) +
  scale_colour_datalab_c() +
  theme_datalab()
```

---

## What’s included

### Theme

- `theme_datalab()`

A minimal theme based on `theme_minimal()` with restrained grid lines and sensible typography defaults.

### Discrete colour scales

- `scale_fill_datalab_d()`
- `scale_colour_datalab_d()`
- `scale_color_datalab_d()` (US spelling)

### Continuous colour scales

- `scale_fill_datalab_c()`
- `scale_colour_datalab_c()`
- `scale_color_datalab_c()` (US spelling)

### Palette helpers

- `datalab_cols()`
- `datalab_pal(type = c("discrete", "continuous"))`

---

## Vignette

```r
vignette("using-ggdatalab")
```

Or:

```r
browseVignettes("ggdatalab")
```

---

## Contributing

Issues and pull requests are welcome. Please include a minimal reproducible example when reporting bugs.

---

## License

MIT © KUB Datalab
