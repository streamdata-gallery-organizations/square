---
swagger: "2.0"
x-collection-name: Square
x-complete: 0
info:
  title: Square Connect API Post V2 Catalog Batch Upsert
  description: |-
    Creates or updates up to 10,000 target objects based on the provided
    list of objects. The target objects are grouped into batches and each batch is
    inserted/updated in an all-or-nothing manner. If an object within a batch is
    malformed in some way, or violates a database constraint, the entire batch
    containing that item will be disregarded. However, other batches in the same
    request may still succeed. Each batch may contain up to 1,000 objects, and
    batches will be processed in order as long as the total object count for the
    request (items, variations, modifier lists, discounts, and taxes) is no more
    than 10,000.
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
  /v2/catalog/batch-delete:
    post:
      summary: Post V2 Catalog Batch Delete
      description: |-
        Deletes a set of [CatalogItem](#type-catalogitem)s based on the
        provided list of target IDs and returns a set of successfully deleted IDs in
        the response. Deletion is a cascading event such that all children of the
        targeted object are also deleted. For example, deleting a CatalogItem will
        also delete all of its [CatalogItemVariation](#type-catalogitemvariation)
        children.

        `BatchDeleteCatalogObjects` succeeds even if only a portion of the targeted
        IDs can be deleted. The response will only include IDs that were
        actually deleted.
      operationId: postV2CatalogBatchDelete
      x-api-path-slug: v2catalogbatchdelete-post
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
      - Catalog
      - Batch-delete
  /v2/catalog/batch-retrieve:
    post:
      summary: Post V2 Catalog Batch Retrieve
      description: |-
        Returns a set of objects based on the provided ID.
        Each [CatalogItem](#type-catalogitem) returned in the set includes all of its
        child information including: all of its
        [CatalogItemVariation](#type-catalogitemvariation) objects, references to
        its [CatalogModifierList](#type-catalogmodifierlist) objects, and the ids of
        any [CatalogTax](#type-catalogtax) objects that apply to it.
      operationId: postV2CatalogBatchRetrieve
      x-api-path-slug: v2catalogbatchretrieve-post
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
      - Catalog
      - Batch-retrieve
  /v2/catalog/batch-upsert:
    post:
      summary: Post V2 Catalog Batch Upsert
      description: |-
        Creates or updates up to 10,000 target objects based on the provided
        list of objects. The target objects are grouped into batches and each batch is
        inserted/updated in an all-or-nothing manner. If an object within a batch is
        malformed in some way, or violates a database constraint, the entire batch
        containing that item will be disregarded. However, other batches in the same
        request may still succeed. Each batch may contain up to 1,000 objects, and
        batches will be processed in order as long as the total object count for the
        request (items, variations, modifier lists, discounts, and taxes) is no more
        than 10,000.
      operationId: postV2CatalogBatchUpsert
      x-api-path-slug: v2catalogbatchupsert-post
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
      - Catalog
      - Batch-upsert
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