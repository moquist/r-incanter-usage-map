r-incanter-usage-map
====================

function and data-type map between R and Incanter

This is intended just to be a starting point, and is being added to gradually.
(Feel free to help!)

At this moment, the "equivalent to R's ...." strings from Incanter doc strings
([from this
commit](https://github.com/incanter/incanter/tree/d710e5e7af129841d470abf8eb7fbba004e10f79))
from the following namespaces have been verified to be included here:

1. incanter.core
1. incanter.stats

For brevity, Incanter namespaces are abbreviated as (e.g.) ```datasets```
instead of ```incanter.datasets```.

Most Incanter docs show this kind of pattern: ```(use '(incanter core stats
charts))```.  Namespaces are included here to help you avoid using ```use``` in
this way, while also avoiding frustration at not knowing which namespaces have
what.

| R                | Incanter                   | Equivalency Rating | Category | Comments                                       |
|------------------|----------------------------|--------------------|----------|----------------------------------------------  |
| %*%              | core/mmult                 | equivalent         | function |                                                |
| *                | core/minus                 | equivalent         | function |                                                |
| +                | core/mult                  | equivalent         | function |                                                |
| -                | core/minus                 | equivalent         | function |                                                |
| /                | core/div                   | equivalent         | function |                                                |
| ^                | core/pow                   | equivalent         | function |                                                |
| abs              | core/abs                   | equivalent         | function |                                                |
| acos             | core/acos                  | equivalent         | function |                                                |
| as.matrix        | core/to-matrix             | equivalent         | function | equivalent when operating on datasets          |
| asin             | core/asin                  | equivalent         | function |                                                |
| atan             | core/atan                  | equivalent         | function |                                                |
| atan2            | core/atan2                 | equivalent         | function |                                                |
| beta             | core/beta                  | equivalent         | function |                                                |
| cbind            | core/bind-columns          | equivalent         | function |                                                |
| chol             | core/decomp-cholesky       | equivalent         | function |                                                |
| choose           | core/choose                | equivalent         | function |                                                |
| cos              | core/cos                   | equivalent         | function |                                                |
| data.frame       | core.Dataset               | equivalent         | datatype | See datasets/get-dataset, io/read-dataset      |
| det              | core/det                   | equivalent         | function |                                                |
| dbeta            | stats/pdf-beta             | equivalent         | function |                                                |
| dbinom           | stats/pdf-binomial         | equivalent         | function |                                                |
| dchisq           | stats/pdf-chisq            | equivalent         | function |                                                |
| dexp             | stats/pdf-exp              | equivalent         | function |                                                |
| df               | stats/pdf-f                | equivalent         | function |                                                |
| dgamma           | stats/pdf-gamma            | equivalent         | function |                                                |
| diag             | core/diag                  | equivalent         | function |                                                |
| dnbinom          | stats/pdf-neg-binomial     | equivalent         | function | see also: stats/cdf-neg-binomial               |
| dnbinom          | stats/cdf-neg-binomial     | equivalent         | function | see also: stats/pdf-neg-binomial               |
| dnorm            | stats/pdf-normal           | equivalent         | function |                                                |
| dpois            | stats/pdf-poisson          | equivalent         | function |                                                |
| dt               | stats/pdf-t                | equivalent         | function |                                                |
| dunif            | stats/pdf-uniform          | equivalent         | function |                                                |
| ecdf             | stats/cdf-empirical        | equivalent         | function |                                                |
| eig              | core/decomp-eigenvalue     | equivalent         | function |                                                |
| exp              | core/exp                   | equivalent         | function |                                                |
| factor           | core/categorical-var       | equivalent         | function |                                                |
| factorial        | core/factorial             | equivalent         | function |                                                |
| gamma            | core/gamma                 | equivalent         | function |                                                |
| length           | core/length                | equivalent         | function |                                                |
| log              | core/log                   | equivalent         | function |                                                |
| log2             | core/log2                  | equivalent         | function |                                                |
| log10            | core/log10                 | equivalent         | function |                                                |
| matrix           | clatrix.core.Matrix        | instead            | datatype | Clatrix matrices are exclusive to type Double  |
| matrix           | core/matrix                | equivalent         | function |                                                |
| mvtnorm::rmvnorm | stats/sample-mvn           | equivalent         | function |                                                |
| pbeta            | core/regularized-beta      | equivalent         | function | see also: stats/cdf-beta                       |
| pbeta            | stats/cdf-beta             | equivalent         | function | see also: core/regularized-beta                |
| pbnimom          | stats/cdf-binomial         | equivalent         | function |                                                |
| pchisq           | stats/cdf-chisq            | equivalent         | function |                                                |
| pexp             | stats/cdf-exp              | equivalent         | function |                                                |
| pf               | stats/cdf-f                | equivalent         | function |                                                |
| pgamma           | stats/cdf-gamma            | equivalent         | function |                                                |
| pnorm            | stats/cdf-normal           | equivalent         | function |                                                |
| ppois            | stats/cdf-poisson          | equivalent         | function |                                                |
| prcomp           | stats/principal-components | equivalent         | function |                                                |
| pt               | stats/cdf-t                | equivalent         | function |                                                |
| punif            | stats/cdf-uniform          | equivalent         | function |                                                |
| qnorm            | stats/quantile-normal      | equivalent         | function |                                                |
| rbeta            | stats/sample-beta          | equivalent         | function | see also: core/regularized-beta                |
| rbinom           | stats/sample-binomial      | equivalent         | function | see also: stats/sample-neg-binomial            |
| rbinom           | stats/sample-neg-binomial  | equivalent         | function | see also: stats/sample-binomial                |
| rchisq           | stats/sample-chisq         | equivalent         | function |                                                |
| rexp             | stats/sample-exp           | equivalent         | function |                                                |
| rgamma           | stats/sample-gamma         | equivalent         | function |                                                |
| rnorm            | stats/sample-normal        | equivalent         | function |                                                |
| rpois            | stats/sample-poisson       | equivalent         | function |                                                |
| rt               | stats/sample-t             | equivalent         | function |                                                |
| qr               | core/decomp-qr             | equivalent         | function |                                                |
| qt               | stats/quantile-t           | equivalent         | function |                                                |
| ncol             | core/ncol                  | equivalent         | function | Incanter's only works on matrices              |
| nrow             | core/nrow                  | equivalent         | function | Incanter's only works on matrices              |
| rbind            | core/bind-rows             | equivalent         | function |                                                |
| runif            | stats/sample-uniform       | equivalent         | function |                                                |
| sd               | stats/sd                   | equivalent         | function |                                                |
| sin              | core/sin                   | equivalent         | function |                                                |
| solve            | core/solve                 | equivalent         | function |                                                |
| sq               | core/sq                    | equivalent         | function |                                                |
| sqrt             | core/sqrt                  | equivalent         | function |                                                |
| svd              | core/decomp-svd            | equivalent         | function |                                                |
| t                | core/trans                 | equivalent         | function |                                                |
| tan              | core/tan                   | equivalent         | function |                                                |
| var              | stats/variance             | equivalent         | function |                                                |


# Categories #
1. function [including R operators]
2. datatype

# Equivalency Ratings #
1. equivalent
2. instead [nearest equivalent, or substitute]
3. related [see also]
