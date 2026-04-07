# Fetch data from the BigDataPE API

This function retrieves data from the BigDataPE API using securely
stored tokens associated with datasets. Users can specify pagination
parameters (`limit` and `offset`) and additional query filters to
customize the data retrieval.

## Usage

``` r
bdpe_fetch_data(
  base_name,
  limit = Inf,
  offset = 0L,
  query = list(),
  verbosity = 0L,
  endpoint = "https://www.bigdata.pe.gov.br/api/buscar"
)
```

## Arguments

- base_name:

  A string specifying the name of the dataset associated with the token.

- limit:

  An integer specifying the maximum number of records to retrieve per
  request. Default is Inf (all records). If set to a non-positive value
  or `Inf`, no limit will be applied.

- offset:

  An integer specifying the starting record for the query. Default is 0.
  If set to a non-positive value or `Inf`, no offset will be applied.

- query:

  A named list of additional query parameters to filter the API results.
  Default is an empty list.

- verbosity:

  An integer specifying the verbosity level. Values are: - `0`: No
  output (default). - `1`: Show progress messages (records fetched,
  totals). - `2`: Show progress messages **and** full HTTP
  request/response details.

- endpoint:

  A string specifying the API endpoint URL. Default is
  "https://www.bigdata.pe.gov.br/api/buscar".

## Value

A tibble containing the data returned by the API.

## Examples

``` r
if (FALSE) { # \dontrun{
# Store a token for the dataset
bdpe_store_token("dengue_dataset", "token")

# Fetch 50 records from the beginning
data <- bdpe_fetch_data("dengue_dataset", limit = 50)

# Fetch records with additional query parameters
data <- bdpe_fetch_data("dengue_dataset", query = list(field = "value"))

# Fetch all data without limits
data <- bdpe_fetch_data("dengue_dataset", limit = Inf)
} # }
```
