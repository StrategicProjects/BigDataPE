# Store a token in an environment variable for a specific dataset

This function stores an authentication token for a specific dataset in a
system environment variable. The environment variable name is
constructed by converting the dataset name to ASCII (removing accents),
replacing spaces with underscores, and prefixing it with "BigDataPE\_".

## Usage

``` r
bdpe_store_token(base_name, token)
```

## Arguments

- base_name:

  The name of the dataset (character).

- token:

  The authentication token for the dataset (character).

## Value

No return value, called for side effects.

## Details

If a variable with that name already exists (and is non-empty), the
function will stop and notify you to avoid overwriting. Adjust this
behavior as needed.

## Examples

``` r
bdpe_store_token("education_dataset", "your-token-here")
#> ✔ Token stored in environment variable: `BigDataPE_education_dataset`
```
