# Access the list of files associated with an Internet Archive item

Access the list of files associated with an Internet Archive item

## Usage

``` r
ia_files(items)
```

## Arguments

- items:

  A list describing an Internet Archive items returned from the API.

## Value

A list containing the files as a list of character vectors.

## Examples

``` r
if (FALSE) { # \dontrun{
ats_query <- c("publisher" = "american tract society")
ids       <- ia_search(ats_query, num_results = 3)
items     <- ia_get_items(ids)
files     <- ia_files(items)
files
} # }
```
