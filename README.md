

This is a R package that wraps the tnt javascript library (https://github.com/tntvis).
It can provide tree- and track-based visulizations, including a simple genome browser.
You can install it by

```r
devtools::install_github("marlin-na/TnT")
```

This package is currently in development, but the following snippet of code may
illustrate the way of using:

```r
library(TnT)
mydata1 <- data.frame (
    start = c(42, 69, 233),
    end = c(54, 99, 250)
)
mydata2 <- data.frame(
    start = c(23, 66, 300),
    end = c(38, 74, 318)
)
tnt_board(from = 14, to = 114, min = -100, max = 500) %>%
    add_track_block(mydata1, label = "My Track 1") %>%
    add_track_block(mydata2, label = "My Track 2", color.feature = "green") %>%
    TnT()
```

