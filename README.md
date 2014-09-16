r-incanter-usage-map
====================

function and data-type map between R and Incanter

For brevity, Incanter namespaces are abbreviated as (e.g.) ```datasets``` instead of ```incanter.datasets```.

| R           | Incanter           | Equivalency Rating | Category | Comments                                     |
|-------------|--------------------|--------------------|----------|----------------------------------------------|
| data.frame  | dataset            | equivalent         | datatype | See datasets/get-dataset, io/read-dataset    |
| matrix      | incanter.Matrix    | instead            | datatype | Incanter matrices exclusive to type Double   |
| matrix      | core/matrix        | equivalent         | function |                                              |
| nrow        | core/nrow          | equivalent         | function |                                              |


# Categories #
1. function
2. datatype

# Equivalency Ratings #
1. equivalent
2. instead [nearest equivalent, or substitute]
3. related [see also]
