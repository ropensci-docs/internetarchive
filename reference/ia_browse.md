# Open an Internet Archive item in the browser

Open an Internet Archive item in the browser

## Usage

``` r
ia_browse(item_id, type = c("details", "stream"))
```

## Arguments

- item_id:

  The item identifier. If multiple item identifiers are passed in, only
  the first will be opened.

- type:

  Which page to open: `details` is the metadata page, `stream` is the
  viewing page for items which are associated with a PDF.

## Value

Returns the item ID(s) passed to the function.

## Examples

``` r
# Distinguished Converts to Rome in America
ia_browse("distinguishedcon00scanuoft")
#> [1] "distinguishedcon00scanuoft"
```
