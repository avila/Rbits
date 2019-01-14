# Rbits
a repo related to R. Should include nice helper functions and more, or less, stuff.


## R helper functions 

from http://r.789695.n4.nabble.com/Apply-as-factor-or-as-numeric-etc-to-multiple-columns-tp893777p893781.html

```{r}
ize <- function (dataFrame, columns = names(dataFrame), izer = as.factor) {
    dataFrame[columns] = lapply(dataFrame[columns], izer)
    dataFrame
} 

# example: turn every variable starting with "cod_" into a factor. 
ize(dataFrame = dfPesHead,
    columns = grepl(pattern = "cod_*", x = names(dfPesHead)))
```

## Rmarkdown Chunk options

change number of rows in a interactive data.frame
`rows.print=20`
