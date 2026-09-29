# Get the metadata for Internet Archive items

Get the metadata for Internet Archive items

## Usage

``` r
ia_get_items(item_id, silence = FALSE)
```

## Arguments

- item_id:

  A character vector containing the ID for an Internet Archive item.
  This argument is vectorized, so you can retrieve multiple items at
  once.

- silence:

  If false, print the item IDs as they are retrieved.

## Value

A list containing the metadata returned by the API. List names
correspond to the item IDs.

## Examples

``` r
if (FALSE) { # \dontrun{
ia_get_items("thedamnationofth00133gut")

ats_query <- c("publisher" = "american tract society")
ids       <- ia_search(ats_query, num_results = 2)
ia_get_items(ids)
} # }
```
