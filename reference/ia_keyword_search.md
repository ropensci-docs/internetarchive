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
#> 84 total items found. This query requested 20 results.
#>  [1] "fatherheckerhisf0000mcso"                               
#>  [2] "cia-readingroom-document-cia-rdp96-00788r001200340011-1"
#>  [3] "fav-isaac_potter"                                       
#>  [4] "isaacthomashecke0000behn"                               
#>  [5] "WHDH_20161024_090000_7News_Today_in_New_England"        
#>  [6] "catholicworld01unkngoog"                                
#>  [7] "paulistfatherisa0000hanl"                               
#>  [8] "catholicworld02unkngoog"                                
#>  [9] "bwb_T5-BCL-008"                                         
#> [10] "americanexperien00fari"                                 
#> [11] "a589111500unknuoft"                                     
#> [12] "yankeepaulisaact0000unse"                               
#> [13] "lifeoffatherheck00elli_0"                               
#> [14] "catholicworld01projgoog"                                
#> [15] "abitunpublished00heckgoog"                              
#> [16] "ERIC_ED250755"                                          
#> [17] "fatherhecker01sedg"                                     
#> [18] "roadstoromeanteb0000fran"                               
#> [19] "TheLightOfTheCrossV2"                                   
#> [20] "celestialhomespu0000kath"                               
```
