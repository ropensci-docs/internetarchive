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
#> 1539 total items found. This query requested 3 results.
items     <- ia_get_items(ids)
#> Getting childsbookofbibl00gall
#> Getting bwb_P9-CSD-816
#> Getting christknockinga00socigoog
metadata  <- ia_metadata(items)
#> Warning: `data_frame()` was deprecated in tibble 1.1.0.
#> ℹ Please use `tibble()` instead.
#> ℹ The deprecated feature was likely used in the internetarchive package.
#>   Please report the issue at
#>   <https://github.com/ropensci/internetarchive/issues>.
metadata
#> # A tibble: 126 × 3
#>    id                     field            value                                
#>    <chr>                  <chr>            <chr>                                
#>  1 childsbookofbibl00gall title            "The child's book of Bible stories :…
#>  2 childsbookofbibl00gall creator          "Gallaudet, T. H. (Thomas Hopkins), …
#>  3 childsbookofbibl00gall subject1         "Christian life"                     
#>  4 childsbookofbibl00gall subject2         "Christian ethics"                   
#>  5 childsbookofbibl00gall description      "On title page: \"No. 1\""           
#>  6 childsbookofbibl00gall publisher        "New York : American Tract Society"  
#>  7 childsbookofbibl00gall date             "1834"                               
#>  8 childsbookofbibl00gall language         "eng"                                
#>  9 childsbookofbibl00gall page-progression "lr"                                 
#> 10 childsbookofbibl00gall sponsor          "University of North Carolina at Cha…
#> # ℹ 116 more rows
```
