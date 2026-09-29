# Access the item metadata from an Internet Archive item

Access the item metadata from an Internet Archive item

## Usage

``` r
ia_metadata(items)
```

## Arguments

- items:

  A list object describing an Internet Archive items returned from the
  API.

## Value

A data frame containing the metadata, with columns `id` for the item
identifier, `field` for the name of the metadata field, and `value` for
the metadata values.

## Examples

``` r
ats_query <- c("publisher" = "american tract society")
ids       <- ia_search(ats_query, num_results = 3)
#> 1540 total items found. This query requested 3 results.
items     <- ia_get_items(ids)
#> Getting grammaranddicti00missgoog
#> Getting healthychristian00crosrich
#> Getting williejessie00milliala
metadata  <- ia_metadata(items)
#> Warning: `data_frame()` was deprecated in tibble 1.1.0.
#> ℹ Please use `tibble()` instead.
#> ℹ The deprecated feature was likely used in the internetarchive package.
#>   Please report the issue at
#>   <https://github.com/ropensci/internetarchive/issues>.
metadata
#> # A tibble: 142 × 3
#>    id                        field                     value                    
#>    <chr>                     <chr>                     <chr>                    
#>  1 grammaranddicti00missgoog publisher                 New York, American Tract…
#>  2 grammaranddicti00missgoog identifier                grammaranddicti00missgoog
#>  3 grammaranddicti00missgoog scanner                   google                   
#>  4 grammaranddicti00missgoog title                     Grammar and dictionary o…
#>  5 grammaranddicti00missgoog creator1                  Morrison, W. M. (William…
#>  6 grammaranddicti00missgoog creator2                  Presbyterian Church in t…
#>  7 grammaranddicti00missgoog contributor               Harvard University       
#>  8 grammaranddicti00missgoog mediatype                 texts                    
#>  9 grammaranddicti00missgoog collection                americana                
#> 10 grammaranddicti00missgoog possible-copyright-status NOT_IN_COPYRIGHT         
#> # ℹ 132 more rows
```
