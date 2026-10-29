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
#> Getting jamesshermankimb00kimb
#> Getting memoirofnathanwd0000abbo
#> Getting memoiroflifeofja00stonrich
metadata  <- ia_metadata(items)
#> Warning: `data_frame()` was deprecated in tibble 1.1.0.
#> ℹ Please use `tibble()` instead.
#> ℹ The deprecated feature was likely used in the internetarchive package.
#>   Please report the issue at
#>   <https://github.com/ropensci/internetarchive/issues>.
metadata
#> # A tibble: 153 × 3
#>    id                     field            value                                
#>    <chr>                  <chr>            <chr>                                
#>  1 jamesshermankimb00kimb title            James Sherman Kimball. A sketch      
#>  2 jamesshermankimb00kimb creator          Kimball, James William, 1812-1885    
#>  3 jamesshermankimb00kimb subject1         Kimball, James Sherman, d. 1864      
#>  4 jamesshermankimb00kimb subject2         United States Christian Commission   
#>  5 jamesshermankimb00kimb description      A record of service with the U.S. Ch…
#>  6 jamesshermankimb00kimb publisher        Boston, The American Tract Society   
#>  7 jamesshermankimb00kimb date             1865                                 
#>  8 jamesshermankimb00kimb language         eng                                  
#>  9 jamesshermankimb00kimb page-progression lr                                   
#> 10 jamesshermankimb00kimb sponsor          Sloan Foundation                     
#> # ℹ 143 more rows
```
