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
#> 80 total items found. This query requested 20 results.
#>  [1] "bwb_T5-BCL-008"                                 
#>  [2] "B-001-035-841-ALL"                              
#>  [3] "catholicworld00projgoog"                        
#>  [4] "youtube-KVB_FgVidWk"                            
#>  [5] "TheLifeOfFatherHecker"                          
#>  [6] "lifeoffatherheck0000elli"                       
#>  [7] "a589111500unknuoft"                             
#>  [8] "isaacthomashecke0000behn"                       
#>  [9] "yankeepaulisaact0000unse"                       
#> [10] "celestialhomespu0000burt"                       
#> [11] "abitunpublished00heckgoog"                      
#> [12] "QuestionsOfTheSoul"                             
#> [13] "paulistvocation00paul"                          
#> [14] "WHDH_20161024_090000_7News_Today_in_New_England"
#> [15] "lifeoffatherheck00elli_0"                       
#> [16] "catholicworld01unkngoog"                        
#> [17] "yankeepaulisaact00hold"                         
#> [18] "fav-isaac_potter"                               
#> [19] "questionsofsoul00heck_0"                        
#> [20] "americanpersonal0000unse"                       
```
