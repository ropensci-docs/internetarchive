# Download files for Internet Archive items.

Download files for Internet Archive items.

## Usage

``` r
ia_download(files, dir = ".", extended_name = TRUE, overwrite = FALSE,
  silence = FALSE)
```

## Arguments

- files:

  A data frame of files returned by
  [ia_files](https://docs.ropensci.org/internetarchive/reference/ia_files.md).
  You should filter this data frame to download only the files that you
  actually want.

- dir:

  The directory in which to save the downloaded files.

- extended_name:

  If this argument is `FALSE`, then the downloaded file will have a
  filename in the following format: `itemidentifier.extension`, e.g.,
  `thedamnationofth00133gut.txt`. If there are multiple files of the
  same file type for an item, then the file names will not be unique. If
  this argument is `TRUE`, them the downloaded file will have a filename
  in the following format: `itemidentifier-original-filename.extension`,
  e.g., `thedamnationofth00133gut-133.txt`.

- overwrite:

  If `TRUE`, this function will download all files and overwrite them on
  disk if they have already been downloaded. If `FALSE`, then if a file
  already exists on disk it will not be downloaded again but other
  downloads will proceed normally.

- silence:

  If false, print the item IDs as they are downloaded.

## Value

A data frame including the file names of the downloaded files.

## Examples

``` r
if (FALSE) { # \dontrun{
if (require(dplyr)) {
  dir <- tempdir()
  ia_get_items("thedamnationofth00133gut") %>%
    ia_files() %>%
    filter(type == "txt") %>% # download only the files we want
    ia_download(dir = dir, extended_name = FALSE)
}
} # }
```
