# List all datasets that have stored tokens in environment variables

This function returns a character vector of dataset names that have
their tokens stored in environment variables. Specifically, it looks for
variables that begin with the prefix `"BigDataPE_"`.

## Usage

``` r
bdpe_list_tokens()
```

## Value

A character vector of dataset names with stored tokens. If no tokens are
found, an empty vector is returned and a message is printed.

## Examples

``` r
bdpe_list_tokens()
#> [1] "dengue"            "education_dataset"
```
