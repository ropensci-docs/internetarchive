# Access the item IDs from an Internet Archive items

Access the item IDs from an Internet Archive items

## Usage

``` r
ia_item_id(item)
```

## Arguments

- item:

  A list describing an Internet Archive items returned from the API.
  This argument is vectorized.

## Value

A character vector containing the item IDs.

## Examples

``` r
ats_query <- c("publisher" = "american tract society")
ids       <- ia_search(ats_query, num_results = 3)
#> 1539 total items found. This query requested 3 results.
items     <- ia_get_items(ids)
#> Getting childsbookofbibl00gall
#> Getting bwb_P9-CSD-816
#> Getting christknockinga00socigoog
ia_item_id(items)
#> [1] "childsbookofbibl00gall"    "bwb_P9-CSD-816"           
#> [3] "christknockinga00socigoog"
```
