r-incanter-usage-map
====================

function and data-type map between R and Incanter

This is intended just to be a starting point, and is being added to gradually.
(Feel free to help!)

At this moment, the "equivalent to R's ...." strings from Incanter doc strings
from the following namespaces have been verified to be included here:

1. incanter.core

For brevity, Incanter namespaces are abbreviated as (e.g.) ```datasets```
instead of ```incanter.datasets```.

Most Incanter docs show this kind of pattern: ```(use '(incanter core stats
charts))```.  Namespaces are included here to help you avoid using ```use``` in
this way, while also avoiding frustration at not knowing which namespaces have
what.

| R           | Incanter               | Equivalency Rating | Category | Comments                                       |
|-------------|------------------------|--------------------|----------|----------------------------------------------  |
| %*%         | core/mmult             | equivalent         | function |                                                |
| *           | core/minus             | equivalent         | function |                                                |
| +           | core/mult              | equivalent         | function |                                                |
| -           | core/minus             | equivalent         | function |                                                |
| /           | core/div               | equivalent         | function |                                                |
| ^           | core/pow               | equivalent         | function |                                                |
| abs         | core/abs               | equivalent         | function |                                                |
| acos        | core/acos              | equivalent         | function |                                                |
| as.matrix   | core/to-matrix         | equivalent         | function | equivalent when operating on datasets          |
| asin        | core/asin              | equivalent         | function |                                                |
| atan        | core/atan              | equivalent         | function |                                                |
| atan2       | core/atan2             | equivalent         | function |                                                |
| beta        | core/beta              | equivalent         | function |                                                |
| cbind       | core/bind-columns      | equivalent         | function |                                                |
| chol        | core/decomp-cholesky   | equivalent         | function |                                                |
| choose      | core/choose            | equivalent         | function |                                                |
| cos         | core/cos               | equivalent         | function |                                                |
| data.frame  | dataset                | equivalent         | datatype | See datasets/get-dataset, io/read-dataset      |
| det         | core/det               | equivalent         | function |                                                |
| diag        | core/diag              | equivalent         | function |                                                |
| eig         | core/decomp-eigenvalue | equivalent         | function |                                                |
| exp         | core/exp               | equivalent         | function |                                                |
| factor      | core/categorical-var   | equivalent         | function |                                                |
| factorial   | core/factorial         | equivalent         | function |                                                |
| gamma       | core/gamma             | equivalent         | function |                                                |
| length      | core/length            | equivalent         | function |                                                |
| log         | core/log               | equivalent         | function |                                                |
| log2        | core/log2              | equivalent         | function |                                                |
| log10       | core/log10             | equivalent         | function |                                                |
| matrix      | incanter.Matrix        | instead            | datatype | Incanter matrices are exclusive to type Double |
| matrix      | core/matrix            | equivalent         | function |                                                |
| pbeta       | core/regularized-beta  | equivalent         | function |                                                |
| qr          | core/decomp-qr         | equivalent         | function |                                                |
| ncol        | core/ncol              | equivalent         | function | Incanter's only works on matrices              |
| nrow        | core/nrow              | equivalent         | function | Incanter's only works on matrices              |
| rbind       | core/bind-rows         | equivalent         | function |                                                |
| sin         | core/sin               | equivalent         | function |                                                |
| solve       | core/solve             | equivalent         | function |                                                |
| sq          | core/sq                | equivalent         | function |                                                |
| sqrt        | core/sqrt              | equivalent         | function |                                                |
| svd         | core/decomp-svd        | equivalent         | function |                                                |
| t           | core/trans             | equivalent         | function |                                                |
| tan         | core/tan               | equivalent         | function |                                                |


# Categories #
1. function [including R operators]
2. datatype

# Equivalency Ratings #
1. equivalent
2. instead [nearest equivalent, or substitute]
3. related [see also]
