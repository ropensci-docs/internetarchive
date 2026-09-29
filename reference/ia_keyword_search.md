# Perform an simple keyword search of the Internet Archive.

Perform an simple keyword search of the Internet Archive.

## Usage

``` r
ia_keyword_search(keywords, num_results = 5, page = 1, print_total = TRUE)
```

## Arguments

- keywords:

  The keywords to search for.

- num_results:

  The number of results to return per page.

- page:

  When results are paged, which page of results to return.

- print_total:

  Should the total number of results for this query be printed as a
  message?

## Value

A character vector of Internet Archive item IDs.

## Examples

``` r
ia_keyword_search("isaac hecker", num_results = 20)
#> 83 total items found. This query requested 20 results.
#>  [1] "fatherheckerhisf0000mcso_b6n1" "yankeepaulisaact0000unse"     
#>  [3] "unboundedframefr0000fell"      "yankeepaulisaact0000hold"     
#>  [5] "the-secret-to-self-motivation" "fav-isaac_potter"             
#>  [7] "somethingaboutau03anne"        "questionsofsoul00heck_0"      
#>  [9] "yankeepaulisaact00hold"        "lifeoffatherheck01elli"       
#> [11] "abitunpublished00heckgoog"     "publiccharities00heck"        
#> [13] "catholicworld01unkngoog"       "fatherhecker01sedg"           
#> [15] "heckerstudiesess0000unse"      "americanexperien00fari"       
#> [17] "aspirationsofnat00heck_3"      "unset0003unse_y5b3"           
#> [19] "catholicchurchi00heckgoog"     "youngconvertsorm00smal"       
```
