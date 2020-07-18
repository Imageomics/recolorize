# recolorize v 0.0.0.9000 [![Build Status](https://travis-ci.org/hiweller/recolorize.svg?branch=master)](https://travis-ci.org/hiweller/recolorize)
> "As we computer programmers put it, if it doesn't have to work, I can make it run as fast as you want."  
> —*Maciej Cegłowski*

A tentatively working R package for simplifying and remapping colors.

<img src="https://github.com/hiweller/graphics/blob/master/recolorize_gifs/corbetti_hist.gif" alt="drawing" width="500"/>

> Original image credit: Nathan P. Lord / Able Chow

## What is this?

Functions for recoloring images based on various color binning schemes. Eventually for use going between patternize, pavo, colordistance, etc. The idea is to simplify the colors of an image according to a metric that is useful for the user.

## Quick start

To generate the images above:
```{r}
devtools::install_github("hiweller/recolorize")

corbetti <- system.file("extdata/corbetti.png", package = "recolorize")

for (i in 1:10) {
  recolorize::recolorize(corbetti, method = "hist", bins = i)
 }
```
Vignettes and better documentation coming soon.

## How does it work?

You put in a binning scheme, an image, and (optional) a background masking condition. You get out a recolored image and a color palette with (optional) the proportion of pixels assigned to each color. The above gif was generated by binning colors in RGB color space in increasingly smaller (finer resolution) bins.

## Contact

Email: [hannahiweller@gmail.com](hannahiweller@gmail.com)
