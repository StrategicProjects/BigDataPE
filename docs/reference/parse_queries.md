# Constructs a URL with query parameters

This function appends a list of query parameters to a base URL.

## Usage

``` r
parse_queries(url, query_list)
```

## Arguments

- url:

  The base URL to which query parameters will be added.

- query_list:

  A list of query parameters to be added to the URL.

## Value

The complete URL with the query parameters appended.

## Examples

``` r
parse_queries("https://www.example.com", list(param1 = "value1", param2 = "value2"))
#> [1] "https://www.example.com?param1=value1&param2=value2"
```
