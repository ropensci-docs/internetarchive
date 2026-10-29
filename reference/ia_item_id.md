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
#> 1540 total items found. This query requested 3 results.
items     <- ia_get_items(ids)
#> Getting jamesshermankimb00kimb
#> Getting memoirofnathanwd0000abbo
#> Getting memoiroflifeofja00stonrich
ia_item_id(items)
#> [1] "jamesshermankimb00kimb"     "memoirofnathanwd0000abbo"  
#> [3] "memoiroflifeofja00stonrich"
```
