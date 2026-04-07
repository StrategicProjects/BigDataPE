# Remove the token associated with a specific dataset

This function removes the authentication token stored in an environment
variable for a specific dataset. If the token is not found, it prints a
message and does not throw an error.

## Usage

``` r
bdpe_remove_token(base_name)
```

## Arguments

- base_name:

  The name of the dataset (character).

## Value

No return value. If the token is found, it is removed. If not, a message
is displayed.

## Examples

``` r
bdpe_remove_token("education_dataset")
#> ✔ Token successfully removed for dataset: "education_dataset"
```
