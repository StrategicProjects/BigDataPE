# Retrieve the token associated with a specific dataset

This function retrieves the authentication token stored in an
environment variable for a specific dataset. If the token is not found,
it returns `NULL` and prints a message instead of throwing an error.

## Usage

``` r
bdpe_get_token(base_name)
```

## Arguments

- base_name:

  The name of the dataset (character).

## Value

A string containing the authentication token, or `NULL` if the token is
not found.

## Examples

``` r
token <- bdpe_get_token("education_dataset")
```
