[![Build Status](https://travis-ci.org/nmecsys/BETS.svg?branch=master)](https://travis-ci.org/nmecsys/BETS) [![CRAN_Status_Badge](http://www.r-pkg.org/badges/version/BETS)](https://CRAN.R-project.org/package=BETS) [![downloads](http://cranlogs.r-pkg.org/badges/BETS)](http://cran.rstudio.com/web/packages/BETS/index.html)
![Build Status](https://ci.appveyor.com/api/projects/status/github/nmecsys/BETS?branch=master&svg=true)
![](http://cranlogs.r-pkg.org/badges/last-week/BETS?color=black)

# BETS - Brazilian Economic Times Series

## Installation

```R
install.packages("BETS") 
```
## Usage

```R
library(BETS)
```
## Warning

The last version of RMySQL is not working properly, therefore, if you install it along with BETS, some functions won't work. To solve it, do the following:

```R
remove.packages(c("RMySQL","DBI"))
install.packages("devtools")
devtools::install_version("DBI", version = "0.5", repos = "http://cran.us.r-project.org")
devtools::install_version("RMySQL", version = "0.10.9", repos = "http://cran.us.r-project.org") 
```

### Information
 
 The Brazilian Economic Uncertainty Indicator (IIE-Br) is standardized in a new window
 
   ```R
   # To get the IIEBR and components, run:
   iiebr <- BETS.get(code = "ST_100.0")
   market <- BETS.get(code = "ST_100.1")
   expectations <- BETS.get(code = "ST_100.2")
   media <- BETS.get(code = "ST_100.3")
   ```

