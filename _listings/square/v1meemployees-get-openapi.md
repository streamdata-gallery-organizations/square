---
swagger: "2.0"
x-collection-name: Square
x-complete: 0
info:
  title: Square Connect API Provides summary information for all of a business's employees.
  description: Provides summary information for all of a business's employees.
  termsOfService: https://connect.squareup.com/tos
  contact:
    name: Square Developer Platform
    url: https://squareup.com/developers
    email: developers@squareup.com
  version: "2.0"
host: connect.squareup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/me:
    get:
      summary: Get a business's information.
      description: Get a business's information.
      operationId: RetrieveBusiness
      x-api-path-slug: v1me-get
      responses:
        200:
          description: OK
      tags:
      - Businesss
      - Information
  /v1/me/employees:
    get:
      summary: Provides summary information for all of a business's employees.
      description: Provides summary information for all of a business's employees.
      operationId: ListEmployees
      x-api-path-slug: v1meemployees-get
      parameters:
      - in: query
        name: batch_token
        description: A pagination cursor to retrieve the next set of results for youroriginal
          query to the endpoint
      - in: query
        name: begin_created_at
        description: If filtering results by their created_at field, the beginning
          of the requested reporting period, in ISO 8601 format
      - in: query
        name: begin_updated_at
        description: If filtering results by their updated_at field, the beginning
          of the requested reporting period, in ISO 8601 format
      - in: query
        name: end_created_at
        description: If filtering results by their created_at field, the end of the
          requested reporting period, in ISO 8601 format
      - in: query
        name: end_updated_at
        description: If filtering results by there updated_at field, the end of the
          requested reporting period, in ISO 8601 format
      - in: query
        name: external_id
        description: If provided, the endpoint returns only employee entities with
          the specified external_id
      - in: query
        name: limit
        description: The maximum integer number of employee entities to return in
          a single response
      - in: query
        name: order
        description: The order in which employees are listed in the response, based
          on their created_at field
      - in: query
        name: status
        description: If provided, the endpoint returns only employee entities with
          the specified status (ACTIVE or INACTIVE)
      responses:
        200:
          description: OK
      tags:
      - Provides
      - Summary
      - Information
      - Of
      - Businesss
      - Employees
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