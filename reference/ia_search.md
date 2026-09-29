# Search the Internet Archive

Perform an advanced search of the Internet Archive, specifying which
metadata fields to search. Note that all searches are in the form of
"contains," i.e., the title contains the search term.

## Usage

``` r
ia_search(terms, num_results = 5, page = 1, print_url = FALSE,
  print_total = TRUE)
```

## Arguments

- terms:

  A set of metadata fields and corresponding values to search. These
  should take the form of a named character vector.

- num_results:

  The number of results to return per page.

- page:

  When results are paged, which page of results to return.

- print_url:

  Should the URL used for the query be printed as a message?

- print_total:

  Should the total number of results for this query be printed as a
  message?

## Value

A character vector of Internet Archive item IDs.

## References

See the documentation on the Internet Archive's [advanced search
page](https://archive.org/advancedsearch.php).

## Examples

``` r
query1 <- c("title" = "damnation of theron ware")
ia_search(query1)
#> 31 total items found. This query requested 5 results.
#> [1] "damnationofthero00haro_0"           "damnationtheron02fredgoog"         
#> [3] "11817472"                           "damnation_theronware_1005_librivox"
#> [5] "dli.ernet.214419"                  
query2 <- c("title" = "damnation of theron ware",
            "contributor" = "gutenberg")
ia_search(query2)
#> 2 total items found. This query requested 5 results.
#> [1] "thedamnationofth00133gut" "dware10"                 
```
