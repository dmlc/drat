## DMLC drat Repo

This [drat](http://dirk.eddelbuettel.com/code/drat.html) package repository provides R packages from DMLC code repositories.

### Usage

```{.r}
# first add the repo
drat::addRepo("dmlc")
# either install just one or more given packages
install.packages("xgboost")
# or update already installed packages
update.packages()
```

### Note

The `mxnet` package has been moved to S3.

To install the CPU-only package on Windows/OSX:

```r
cran <- getOption("repos")
cran["dmlc"] <- "https://s3-us-west-2.amazonaws.com/apache-mxnet/R/CRAN/"
options(repos = cran)
install.packages("mxnet")
```

To install the GPU-enabled package on Windows:

```r
cran <- getOption("repos")
cran["dmlc"] <- "https://s3-us-west-2.amazonaws.com/apache-mxnet/R/CRAN/GPU"
options(repos = cran)
install.packages("mxnet")
```

### License

Packages in this repository are available under their respective license.
