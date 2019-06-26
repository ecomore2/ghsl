
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Global Human Settlement Layers

<!-- badges: start -->

<!-- badges: end -->

Raster file are downloaded from the
[GHSL](https://ghsl.jrc.ec.europa.eu/datasets.php) website and then
cropped onto the province of Vientiane (see
[here](https://ecomore2.github.io/ghsl/make_data.html)). Data are
projected on the spherical Mercator projection (
[EPSG](http://www.epsg.org):[3857](https://epsg.io/3857), which is the
projection used by [Google Maps](https://www.google.com/maps),
[OpenStreetMap](https://www.openstreetmap.org) and [Bing
Maps](https://www.bing.com/maps) among other) with a resolution of 38 m.
Data are available for 1999 (1 MB), 2000 (1 MB) and 2014 (1 MB)
[here](https://www.dropbox.com/sh/uj3872y5keso5ev/AACXrlnC1YCk_PYkb0nhgD5Ea?dl=0).

Raster file can be downloaded directly from R as
so:

``` r
download.file("https://www.dropbox.com/s/4sxdsmj0s2nxy5c/builtup1990res38m3857.tif?raw=1", "builtup1990res38m3857.tif")
download.file("https://www.dropbox.com/s/en0u787brvk75pe/builtup2000res38m3857.tif?raw=1", "builtup2000res38m3857.tif")
download.file("https://www.dropbox.com/s/0jxx754zudgldf2/builtup2014res38m3857.tif?raw=1", "builtup2014res38m3857.tif")
```

And then loaded into R as so:

``` r
library(raster)
builtup1990 <- raster("builtup1990res38m3857.tif")
builtup2000 <- raster("builtup2000res38m3857.tif")
builtup2014 <- raster("builtup2014res38m3857.tif")
```
