---
swagger: "2.0"
x-collection-name: CoinMarketCap
x-complete: 0
info:
  title: CoinMarketCap List all exchanges (historical)
  description: |-
    **This endpoint is not yet available. It is slated for release in Q3 2018.**


    Get a paginated list of all cryptocurrency exchanges with historical market data for a given point in time. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.
  termsOfService: https://coinmarketcap.com/terms/
  version: 1.0.0
host: pro-api.coinmarketcap.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/exchange/listings/latest:
    get:
      summary: List all exchanges (latest)
      description: "Get a paginated list of all cryptocurrency exchanges with 24 hour
        volume. Additional market data fields will be available in the future. You
        can configure this call to sort by 24 hour volume or another field. Use the
        \"convert\" option to return market values in multiple fiat and cryptocurrency
        conversions in the same call.  \n  \n**This endpoint is available on the following
        API plans:**\n  - ~~Starter~~\n  - ~~Hobbyist~~\n  - Standard\n  - Professional\n
        \ - Enterprise\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint
        will be migrated to ~1 minute updates shortly.  \n  \n  *NOTE: Use this endpoint
        if you need a sorted and paginated list of exchanges. If you want to query
        for market data on a few specific exchanges use /v1/exchange/quotes/latest
        which is optimized for that purpose. The response data between these endpoints
        is otherwise the same.*"
      operationId: getV1ExchangeListingsLatest
      x-api-path-slug: v1exchangelistingslatest-get
      parameters:
      - in: query
        name: convert
        description: Optionally calculate market quotes in up to 32 currencies at
          once by passing a comma-separated list of cryptocurrency or fiat currency
          symbols
      - in: query
        name: limit
        description: Optionally specify the number of results to return
      - in: query
        name: market_type
        description: The type of exchange markets to include in rankings
      - in: query
        name: sort
        description: What field to sort the list of exchanges by
      - in: query
        name: sort_dir
        description: The direction in which to order exchanges against the specified
          sort
      - in: query
        name: start
        description: Optionally offset the start (1-based index) of the paginated
          list of items to return
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - List
      - ""
      - Exchanges
      - (latest)
  /v1/exchange/listings/historical:
    get:
      summary: List all exchanges (historical)
      description: |-
        **This endpoint is not yet available. It is slated for release in Q3 2018.**


        Get a paginated list of all cryptocurrency exchanges with historical market data for a given point in time. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.
      operationId: getV1ExchangeListingsHistorical
      x-api-path-slug: v1exchangelistingshistorical-get
      parameters:
      - in: query
        name: convert
        description: Optionally calculate market quotes in up to 32 currencies at
          once by passing a comma-separated list of cryptocurrency or fiat currency
          symbols
      - in: query
        name: limit
        description: Optionally specify the number of results to return
      - in: query
        name: market_type
        description: The type of exchange markets to include in rankings
      - in: query
        name: sort
        description: What field to sort the list of exchanges by
      - in: query
        name: sort_dir
        description: The direction in which to order exchanges against the specified
          sort
      - in: query
        name: start
        description: Optionally offset the start (1-based index) of the paginated
          list of items to return
      - in: query
        name: timestamp
        description: Timestamp (Unix or ISO 8601) to return historical exchange listings
          for
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - List
      - ""
      - Exchanges
      - (historical)
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---