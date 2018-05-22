---
swagger: "2.0"
x-collection-name: Square
x-complete: 0
info:
  title: Square Connect API Get V2 Locations Location Transactions
  description: |-
    Lists transactions for a particular location.

    Transactions include payment information from sales and exchanges and refund
    information from returns and exchanges.

    Max results per [page](#paginatingresults): 50
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
  /v2/catalog/info:
    get:
      summary: Get V2 Catalog Info
      description: |-
        Returns information about the Square Catalog API, such as batch size
        limits for `BatchUpsertCatalogObjects`.
      operationId: getV2CatalogInfo
      x-api-path-slug: v2cataloginfo-get
      responses:
        200:
          description: OK
      tags:
      - Catalog
      - Info
  /v2/catalog/list:
    get:
      summary: Get V2 Catalog List
      description: |-
        Returns a list of [CatalogObject](#type-catalogobject)s that includes
        all objects of a set of desired types (for example, all [CatalogItem](#type-catalogitem)
        and [CatalogTax](#type-catalogtax) objects) in the catalog. The types parameter
        is specified as a comma-separated list of valid [CatalogObject](#type-catalogobject) types:
        `ITEM`, `ITEM_VARIATION`, `MODIFIER`, `MODIFIER_LIST`, `CATEGORY`, `DISCOUNT`, `TAX`.
      operationId: getV2CatalogList
      x-api-path-slug: v2cataloglist-get
      parameters:
      - in: query
        name: cursor
        description: The pagination cursor returned in the previous response
      - in: query
        name: types
        description: An optional case-insensitive, comma-separated list of object
          types to retrieve, for example`ITEM,ITEM_VARIATION,CATEGORY`
      responses:
        200:
          description: OK
      tags:
      - Catalog
      - List
  /v2/catalog/object:
    post:
      summary: Post V2 Catalog Object
      description: Creates or updates the target [CatalogObject](#type-catalogobject).
      operationId: postV2CatalogObject
      x-api-path-slug: v2catalogobject-post
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
      - Object
  /v2/catalog/object/{object_id}:
    delete:
      summary: Delete V2 Catalog Object Object
      description: |-
        Deletes a single [CatalogObject](#type-catalogobject) based on the
        provided ID and returns the set of successfully deleted IDs in the response.
        Deletion is a cascading event such that all children of the targeted object
        are also deleted. For example, deleting a [CatalogItem](#type-catalogitem)
        will also delete all of its
        [CatalogItemVariation](#type-catalogitemvariation) children.
      operationId: deleteV2CatalogObjectObject
      x-api-path-slug: v2catalogobjectobject-id-delete
      parameters:
      - in: path
        name: object_id
        description: The ID of the [CatalogObject](#type-catalogobject) to be deleted
      responses:
        200:
          description: OK
      tags:
      - Catalog
      - Object
      - Object
    get:
      summary: Get V2 Catalog Object Object
      description: |-
        Returns a single [CatalogItem](#type-catalogitem) as a
        [CatalogObject](#type-catalogobject) based on the provided ID. The returned
        object includes all of the relevant [CatalogItem](#type-catalogitem)
        information including: [CatalogItemVariation](#type-catalogitemvariation)
        children, references to its
        [CatalogModifierList](#type-catalogmodifierlist) objects, and the ids of
        any [CatalogTax](#type-catalogtax) objects that apply to it.
      operationId: getV2CatalogObjectObject
      x-api-path-slug: v2catalogobjectobject-id-get
      parameters:
      - in: query
        name: include_related_objects
        description: If `true`, the response will include additional objects that
          are related to therequested object, as follows:If the `object` field of
          the response contains a [CatalogItem](#type-catalogitem),its associated
          [CatalogCategory](#type-catalogcategory), [CatalogTax](#type-catalogtax)es,
          and[CatalogModifierList](#type-catalogmodifierlist)s will be returned in
          the `related_objects` field of theresponse
      - in: path
        name: object_id
        description: The object ID of any type of [CatalogObject](#type-catalogobject)s
          to be retrieved
      responses:
        200:
          description: OK
      tags:
      - Catalog
      - Object
      - Object
  /v2/catalog/search:
    post:
      summary: Post V2 Catalog Search
      description: |-
        Queries the targeted catalog using a variety of query types:
        [CatalogQuerySortedAttribute](#type-catalogquerysortedattribute),
        [CatalogQueryExact](#type-catalogqueryexact),
        [CatalogQueryRange](#type-catalogqueryrange),
        [CatalogQueryText](#type-catalogquerytext),
        [CatalogQueryItemsForTax](#type-catalogqueryitemsfortax), and
        [CatalogQueryItemsForModifierList](#type-catalogqueryitemsformodifierlist).
      operationId: postV2CatalogSearch
      x-api-path-slug: v2catalogsearch-post
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
      - Search
  /v2/catalog/update-item-modifier-lists:
    post:
      summary: Post V2 Catalog Update Item Modifier Lists
      description: |-
        Updates the [CatalogModifierList](#type-catalogmodifierlist) objects
        that apply to the targeted [CatalogItem](#type-catalogitem) without having
        to perform an upsert on the entire item.
      operationId: postV2CatalogUpdateItemModifierLists
      x-api-path-slug: v2catalogupdateitemmodifierlists-post
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
      - Update-item-modifier-lists
  /v2/catalog/update-item-taxes:
    post:
      summary: Post V2 Catalog Update Item Taxes
      description: |-
        Updates the [CatalogTax](#type-catalogtax) objects that apply to the
        targeted [CatalogItem](#type-catalogitem) without having to perform an
        upsert on the entire item.
      operationId: postV2CatalogUpdateItemTaxes
      x-api-path-slug: v2catalogupdateitemtaxes-post
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
      - Update-item-taxes
  /v2/customers:
    get:
      summary: Get V2 Customers
      description: Lists a business's customers.
      operationId: getV2Customers
      x-api-path-slug: v2customers-get
      parameters:
      - in: query
        name: cursor
        description: A pagination cursor returned by a previous call to this endpoint
      responses:
        200:
          description: OK
      tags:
      - Customers
    post:
      summary: Post V2 Customers
      description: |-
        Creates a new customer for a business, which can have associated cards on file.

        You must provide __at least one__ of the following values in your request to this
        endpoint:

        - `given_name`
        - `family_name`
        - `company_name`
        - `email_address`
        - `phone_number`

        This endpoint does not accept an idempotency key. If you accidentally create
        a duplicate customer, you can delete it with the
        [DeleteCustomer](#endpoint-deletecustomer) endpoint.
      operationId: postV2Customers
      x-api-path-slug: v2customers-post
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
      - Customers
  /v2/customers/{customer_id}:
    delete:
      summary: Delete V2 Customers Customer
      description: Deletes a customer from a business, along with any linked cards
        on file.
      operationId: deleteV2CustomersCustomer
      x-api-path-slug: v2customerscustomer-id-delete
      parameters:
      - in: path
        name: customer_id
        description: The ID of the customer to delete
      responses:
        200:
          description: OK
      tags:
      - Customers
      - Customer
    get:
      summary: Get V2 Customers Customer
      description: Returns details for a single customer.
      operationId: getV2CustomersCustomer
      x-api-path-slug: v2customerscustomer-id-get
      parameters:
      - in: path
        name: customer_id
        description: The ID of the customer to retrieve
      responses:
        200:
          description: OK
      tags:
      - Customers
      - Customer
    put:
      summary: Put V2 Customers Customer
      description: |-
        Updates the details of an existing customer.
        The ID of the customer may change if the customer has been merged into another customer.

        You cannot edit a customer's cards on file with this endpoint. To make changes
        to a card on file, you must delete the existing card on file with the
        [DeleteCustomerCard](#endpoint-deletecustomercard) endpoint, then create a new one with the
        [CreateCustomerCard](#endpoint-createcustomercard) endpoint.
      operationId: putV2CustomersCustomer
      x-api-path-slug: v2customerscustomer-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: customer_id
        description: The ID of the customer to update
      responses:
        200:
          description: OK
      tags:
      - Customers
      - Customer
  /v2/customers/{customer_id}/cards:
    post:
      summary: Post V2 Customers Customer Cards
      description: |-
        Adds a card on file to an existing customer. In the United States
        Square takes care of automatically updating any cards on file that might
        have expired since you first attached them to a customer.

        As with charges, calls to `CreateCustomerCard` are idempotent. Multiple
        calls with the same card nonce return the same card record that was created
        with the provided nonce during the _first_ call.
      operationId: postV2CustomersCustomerCards
      x-api-path-slug: v2customerscustomer-idcards-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: customer_id
        description: The ID of the customer to link the card on file to
      responses:
        200:
          description: OK
      tags:
      - Customers
      - Customer
      - Cards
  /v2/customers/{customer_id}/cards/{card_id}:
    delete:
      summary: Delete V2 Customers Customer Cards Card
      description: Delete v2 customers customer cards card.
      operationId: deleteV2CustomersCustomerCardsCard
      x-api-path-slug: v2customerscustomer-idcardscard-id-delete
      parameters:
      - in: path
        name: card_id
        description: The ID of the card on file to delete
      - in: path
        name: customer_id
        description: The ID of the customer that the card on file belongs to
      responses:
        200:
          description: OK
      tags:
      - Customers
      - Customer
      - Cards
      - Card
  /v2/locations:
    get:
      summary: Get V2 Locations
      description: |-
        Provides the details for all of a business's locations.

        Most other Connect API endpoints have a required `location_id` path parameter.
        The `id` field of the [`Location`](#type-location) objects returned by this
        endpoint correspond to that `location_id` parameter.
      operationId: getV2Locations
      x-api-path-slug: v2locations-get
      responses:
        200:
          description: OK
      tags:
      - Locations
  /v2/locations/{location_id}/additional-recipient-receivable-refunds:
    get:
      summary: Get V2 Locations Location Additional Recipient Receivable Refunds
      description: |-
        Returns a list of refunded transactions (across all possible originating locations) relating to monies
        credited to the provided location ID by another Square account using the `additional_recipients` field in a transaction.

        Max results per [page](#paginatingresults): 50
      operationId: getV2LocationsLocationAdditionalRecipientReceivableRefunds
      x-api-path-slug: v2locationslocation-idadditionalrecipientreceivablerefunds-get
      parameters:
      - in: query
        name: begin_time
        description: The beginning of the requested reporting period, in RFC 3339
          format
      - in: query
        name: cursor
        description: A pagination cursor returned by a previous call to this endpoint
      - in: query
        name: end_time
        description: The end of the requested reporting period, in RFC 3339 format
      - in: path
        name: location_id
        description: The ID of the location to list AdditionalRecipientReceivableRefunds
          for
      - in: query
        name: sort_order
        description: The order in which results are listed in the response (`ASC`
          foroldest first, `DESC` for newest first)
      responses:
        200:
          description: OK
      tags:
      - Locations
      - Location
      - Additional-recipient-receivable-refunds
  /v2/locations/{location_id}/additional-recipient-receivables:
    get:
      summary: Get V2 Locations Location Additional Recipient Receivables
      description: |-
        Returns a list of receivables (across all possible sending locations) representing monies credited
        to the provided location ID by another Square account using the `additional_recipients` field in a transaction.

        Max results per [page](#paginatingresults): 50
      operationId: getV2LocationsLocationAdditionalRecipientReceivables
      x-api-path-slug: v2locationslocation-idadditionalrecipientreceivables-get
      parameters:
      - in: query
        name: begin_time
        description: The beginning of the requested reporting period, in RFC 3339
          format
      - in: query
        name: cursor
        description: A pagination cursor returned by a previous call to this endpoint
      - in: query
        name: end_time
        description: The end of the requested reporting period, in RFC 3339 format
      - in: path
        name: location_id
        description: The ID of the location to list AdditionalRecipientReceivables
          for
      - in: query
        name: sort_order
        description: The order in which results are listed in the response (`ASC`
          foroldest first, `DESC` for newest first)
      responses:
        200:
          description: OK
      tags:
      - Locations
      - Location
      - Additional-recipient-receivables
  /v2/locations/{location_id}/checkouts:
    post:
      summary: Post V2 Locations Location Checkouts
      description: |-
        Creates a [Checkout](#type-checkout) response that links a
        `checkoutId` and `checkout_page_url` that customers can be directed to in
        order to provide their payment information using a payment processing
        workflow hosted on connect.squareup.com.
      operationId: postV2LocationsLocationCheckouts
      x-api-path-slug: v2locationslocation-idcheckouts-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the business location to associate the checkout with
      responses:
        200:
          description: OK
      tags:
      - Locations
      - Location
      - Checkouts
  /v2/locations/{location_id}/orders:
    post:
      summary: Post V2 Locations Location Orders
      description: |-
        Creates an [Order](#type-order) that can then be referenced as `order_id` in a
        request to the [Charge](#endpoint-charge) endpoint. Orders specify products for
        purchase, along with discounts, taxes, and other settings to apply to the purchase.

        To associate a created order with a request to the Charge endpoint, provide the
        order's `id` in the `order_id` field of your request.

        You cannot modify an order after you create it. If you need to modify an order,
        instead create a new order with modified details.

        To learn more about the Orders API, see the [Orders API Overview](https://docs.connect.squareup.com/articles/orders-api-overview).
      operationId: postV2LocationsLocationOrders
      x-api-path-slug: v2locationslocation-idorders-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the business location to associate the order with
      responses:
        200:
          description: OK
      tags:
      - Locations
      - Location
      - Orders
  /v2/locations/{location_id}/orders/batch-retrieve:
    post:
      summary: Post V2 Locations Location Orders Batch Retrieve
      description: |-
        Retrieves a set of [Order](#type-order)s by their IDs.

        If a given Order ID does not exist, the ID is ignored instead of generating an error.
      operationId: postV2LocationsLocationOrdersBatchRetrieve
      x-api-path-slug: v2locationslocation-idordersbatchretrieve-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the orders associated location
      responses:
        200:
          description: OK
      tags:
      - Locations
      - Location
      - Orders
      - Batch-retrieve
  /v2/locations/{location_id}/refunds:
    get:
      summary: Get V2 Locations Location Refunds
      description: |-
        Lists refunds for one of a business's locations.

        In addition to full or partial tender refunds processed through Square APIs,
        refunds may result from itemized returns or exchanges through Square's
        Point of Sale applications.

        Refunds with a `status` of `PENDING` are not currently included in this
        endpoint's response.

        Max results per [page](#paginatingresults): 50
      operationId: getV2LocationsLocationRefunds
      x-api-path-slug: v2locationslocation-idrefunds-get
      parameters:
      - in: query
        name: begin_time
        description: The beginning of the requested reporting period, in RFC 3339
          format
      - in: query
        name: cursor
        description: A pagination cursor returned by a previous call to this endpoint
      - in: query
        name: end_time
        description: The end of the requested reporting period, in RFC 3339 format
      - in: path
        name: location_id
        description: The ID of the location to list refunds for
      - in: query
        name: sort_order
        description: The order in which results are listed in the response (`ASC`
          foroldest first, `DESC` for newest first)
      responses:
        200:
          description: OK
      tags:
      - Locations
      - Location
      - Refunds
  /v2/locations/{location_id}/transactions:
    get:
      summary: Get V2 Locations Location Transactions
      description: |-
        Lists transactions for a particular location.

        Transactions include payment information from sales and exchanges and refund
        information from returns and exchanges.

        Max results per [page](#paginatingresults): 50
      operationId: getV2LocationsLocationTransactions
      x-api-path-slug: v2locationslocation-idtransactions-get
      parameters:
      - in: query
        name: begin_time
        description: The beginning of the requested reporting period, in RFC 3339
          format
      - in: query
        name: cursor
        description: A pagination cursor returned by a previous call to this endpoint
      - in: query
        name: end_time
        description: The end of the requested reporting period, in RFC 3339 format
      - in: path
        name: location_id
        description: The ID of the location to list transactions for
      - in: query
        name: sort_order
        description: The order in which results are listed in the response (`ASC`
          foroldest first, `DESC` for newest first)
      responses:
        200:
          description: OK
      tags:
      - Locations
      - Location
      - Transactions
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