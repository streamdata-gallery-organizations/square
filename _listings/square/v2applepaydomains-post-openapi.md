---
swagger: "2.0"
x-collection-name: Square
x-complete: 0
info:
  title: Square Connect API Post V2 Apple Pay Domains
  description: |-
    Activates a domain for use with Web Apple Pay and Square. A validation
    will be performed on this domain by Apple to ensure is it properly set up as
    an Apple Pay enabled domain.

    This endpoint provides an easy way for platform developers to bulk activate
    Web Apple Pay with Square for merchants using their platform.

    To learn more about Apple Pay on Web see the Apple Pay section in the [Embedding the Square Payment Form](https://docs.connect.squareup.com/articles/adding-payment-form) guide.
  termsOfService: https://connect.squareup.com/tos
  contact:
    name: Square Developer Platform
    url: https://squareup.com/developers
    email: developers@squareup.com
  version: 1.0.0
host: connect.squareup.com
basePath: v1/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v2/apple-pay/domains:
    post:
      summary: Post V2 Apple Pay Domains
      description: |-
        Activates a domain for use with Web Apple Pay and Square. A validation
        will be performed on this domain by Apple to ensure is it properly set up as
        an Apple Pay enabled domain.

        This endpoint provides an easy way for platform developers to bulk activate
        Web Apple Pay with Square for merchants using their platform.

        To learn more about Apple Pay on Web see the Apple Pay section in the [Embedding the Square Payment Form](https://docs.connect.squareup.com/articles/adding-payment-form) guide.
      operationId: postV2ApplePayDomains
      x-api-path-slug: v2applepaydomains-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Apple-pay
      - Domains
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