---
swagger: "2.0"
x-collection-name: GetStream.io
x-complete: 0
info:
  title: Stream API Retrieve a feed - ID filters and pagination
  description: |-
    Retrieves the activities within a feed with ID filtering on the activities to be returned.

    See the [docs](https://getstream.io/docs_rest/#feed) for restrictions and recommendations on how to best make use of these parameters.
  version: 1.0.0
host: eu-central-api.stream-io-api.com
basePath: /api/v1.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /feed/user/eric:
    get:
      summary: Retrieve a feed - ID filters and pagination
      description: |-
        Retrieves the activities within a feed with ID filtering on the activities to be returned.

        See the [docs](https://getstream.io/docs_rest/#feed) for restrictions and recommendations on how to best make use of these parameters.
      operationId: FeedUserEricGet4
      x-api-path-slug: feedusereric-get
      parameters:
      - in: query
        name: api_key
      - in: query
        name: id_lt
      - in: header
        name: Stream-Auth-Type
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Feed
      - User
      - Eric
x-streamrank:
  polling_total_time_average: "0"
  polling_size_download_average: "0"
  streaming_total_time_average: "0"
  streaming_size_download_average: "0"
  change_yes: "0"
  change_no: "0"
  time_percentage: "0"
  size_percentage: "0"
  change_percentage: "200"
  last_run: ~
  days_run: "0"
  minute_run: "0"
---