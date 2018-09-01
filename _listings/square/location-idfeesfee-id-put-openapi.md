---
swagger: "2.0"
x-collection-name: Square
x-complete: 0
info:
  title: Square Connect API Put Location Fees Fee
  description: Modifies the details of an existing fee (tax).
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
    post:
      summary: Post V2 Locations Location Transactions
      description: |-
        Charges a card represented by a card nonce or a customer's card on file.

        Your request to this endpoint must include _either_:

        - A value for the `card_nonce` parameter (to charge a card nonce generated
        with the `SqPaymentForm`)
        - Values for the `customer_card_id` and `customer_id` parameters (to charge
        a customer's card on file)

        In order for an eCommerce payment to potentially qualify for
        [Square chargeback protection](https://squareup.com/help/article/5394), you
        _must_ provide values for the following parameters in your request:

        - `buyer_email_address`
        - At least one of `billing_address` or `shipping_address`

        When this response is returned, the amount of Square's processing fee might not yet be
        calculated. To obtain the processing fee, wait about ten seconds and call
        [RetrieveTransaction](#endpoint-retrievetransaction). See the `processing_fee_money`
        field of each [Tender included](#type-tender) in the transaction.
      operationId: postV2LocationsLocationTransactions
      x-api-path-slug: v2locationslocation-idtransactions-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the location to associate the created transaction with
      responses:
        200:
          description: OK
      tags:
      - Locations
      - Location
      - Transactions
  /v2/locations/{location_id}/transactions/{transaction_id}:
    get:
      summary: Get V2 Locations Location Transactions Transaction
      description: Get v2 locations location transactions transaction.
      operationId: getV2LocationsLocationTransactionsTransaction
      x-api-path-slug: v2locationslocation-idtransactionstransaction-id-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the transactions associated location
      - in: path
        name: transaction_id
        description: The ID of the transaction to retrieve
      responses:
        200:
          description: OK
      tags:
      - Locations
      - Location
      - Transactions
      - Transaction
  /v2/locations/{location_id}/transactions/{transaction_id}/capture:
    post:
      summary: Post V2 Locations Location Transactions Transaction Capture
      description: |-
        Captures a transaction that was created with the [Charge](#endpoint-charge)
        endpoint with a `delay_capture` value of `true`.

        See [Delayed capture transactions](/articles/delayed-capture-transactions/)
        for more information.
      operationId: postV2LocationsLocationTransactionsTransactionCapture
      x-api-path-slug: v2locationslocation-idtransactionstransaction-idcapture-post
      parameters:
      - in: path
        name: location_id
      - in: path
        name: transaction_id
      responses:
        200:
          description: OK
      tags:
      - Locations
      - Location
      - Transactions
      - Transaction
      - Capture
  /v2/locations/{location_id}/transactions/{transaction_id}/refund:
    post:
      summary: Post V2 Locations Location Transactions Transaction Refund
      description: |-
        Initiates a refund for a previously charged tender.

        You must issue a refund within 120 days of the associated payment. See
        [this article](https://squareup.com/help/us/en/article/5060) for more information
        on refund behavior.
      operationId: postV2LocationsLocationTransactionsTransactionRefund
      x-api-path-slug: v2locationslocation-idtransactionstransaction-idrefund-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the original transactions associated location
      - in: path
        name: transaction_id
        description: The ID of the original transaction that includes the tender to
          refund
      responses:
        200:
          description: OK
      tags:
      - Locations
      - Location
      - Transactions
      - Transaction
      - Refund
  /v2/locations/{location_id}/transactions/{transaction_id}/void:
    post:
      summary: Post V2 Locations Location Transactions Transaction Vo
      description: |-
        Cancels a transaction that was created with the [Charge](#endpoint-charge)
        endpoint with a `delay_capture` value of `true`.

        See [Delayed capture transactions](/articles/delayed-capture-transactions/)
        for more information.
      operationId: postV2LocationsLocationTransactionsTransactionVo
      x-api-path-slug: v2locationslocation-idtransactionstransaction-idvoid-post
      parameters:
      - in: path
        name: location_id
      - in: path
        name: transaction_id
      responses:
        200:
          description: OK
      tags:
      - Locations
      - Location
      - Transactions
      - Transaction
      - Void
  /me:
    get:
      summary: Get Me
      description: Get a business's information.
      operationId: getMe
      x-api-path-slug: me-get
      responses:
        200:
          description: OK
      tags:
      - Me
  /me/locations:
    get:
      summary: Get Me Locations
      description: Provides details for a business's locations, including their IDs.
      operationId: getMeLocations
      x-api-path-slug: melocations-get
      responses:
        200:
          description: OK
      tags:
      - Me
      - Locations
  /me/employees:
    post:
      summary: Post Me Employees
      description: Creates an employee for a business.
      operationId: postMeEmployees
      x-api-path-slug: meemployees-post
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
      - Me
      - Employees
    get:
      summary: Get Me Employees
      description: Provides summary information for all of a business's employees.
      operationId: getMeEmployees
      x-api-path-slug: meemployees-get
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
      - Me
      - Employees
  /me/employees/{employee_id}:
    get:
      summary: Get Me Employees Employee
      description: Provides the details for a single employee.
      operationId: getMeEmployeesEmployee
      x-api-path-slug: meemployeesemployee-id-get
      parameters:
      - in: path
        name: employee_id
        description: The employees ID
      responses:
        200:
          description: OK
      tags:
      - Me
      - Employees
    put:
      summary: Put Me Employees Employee
      description: Put me employees employee.
      operationId: putMeEmployeesEmployee
      x-api-path-slug: meemployeesemployee-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: employee_id
        description: The ID of the role to modify
      responses:
        200:
          description: OK
      tags:
      - Me
      - Employees
  /me/roles:
    post:
      summary: Post Me Roles
      description: Creates an employee role you can then assign to employees.
      operationId: postMeRoles
      x-api-path-slug: meroles-post
      parameters:
      - in: body
        name: EmployeeRole
        description: An EmployeeRole object with a name and permissions, and an optional
          owner flag
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Me
      - Roles
    get:
      summary: Get Me Roles
      description: Provides summary information for all of a business's employee roles.
      operationId: getMeRoles
      x-api-path-slug: meroles-get
      parameters:
      - in: query
        name: batch_token
        description: A pagination cursor to retrieve the next set of results for youroriginal
          query to the endpoint
      - in: query
        name: limit
        description: The maximum integer number of employee entities to return in
          a single response
      - in: query
        name: order
        description: The order in which employees are listed in the response, based
          on their created_at field
      responses:
        200:
          description: OK
      tags:
      - Me
      - Roles
  /me/roles/{role_id}:
    get:
      summary: Get Me Roles Role
      description: Provides the details for a single employee role.
      operationId: getMeRolesRole
      x-api-path-slug: merolesrole-id-get
      parameters:
      - in: path
        name: role_id
        description: The roles ID
      responses:
        200:
          description: OK
      tags:
      - Me
      - Roles
    put:
      summary: Put Me Roles Role
      description: Modifies the details of an employee role.
      operationId: putMeRolesRole
      x-api-path-slug: merolesrole-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: role_id
        description: The ID of the role to modify
      responses:
        200:
          description: OK
      tags:
      - Me
      - Roles
  /me/timecards:
    post:
      summary: Post Me Timecards
      description: Creates a timecard for an employee. Each timecard corresponds to
        a single shift.
      operationId: postMeTimecards
      x-api-path-slug: metimecards-post
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
      - Me
      - Timecards
    get:
      summary: Get Me Timecards
      description: Provides summary information for all of a business's employee timecards.
      operationId: getMeTimecards
      x-api-path-slug: metimecards-get
      parameters:
      - in: query
        name: batch_token
        description: A pagination cursor to retrieve the next set of results for youroriginal
          query to the endpoint
      - in: query
        name: begin_clockin_time
        description: If filtering results by their clockin_time field, the beginning
          of the requested reporting period, in ISO 8601 format
      - in: query
        name: begin_clockout_time
        description: If filtering results by their clockout_time field, the beginning
          of the requested reporting period, in ISO 8601 format
      - in: query
        name: begin_updated_at
        description: If filtering results by their updated_at field, the beginning
          of the requested reporting period, in ISO 8601 format
      - in: query
        name: deleted
        description: If true, only deleted timecards are returned
      - in: query
        name: employee_id
        description: If provided, the endpoint returns only timecards for the employee
          with the specified ID
      - in: query
        name: end_clockin_time
        description: If filtering results by their clockin_time field, the end of
          the requested reporting period, in ISO 8601 format
      - in: query
        name: end_clockout_time
        description: If filtering results by their clockout_time field, the end of
          the requested reporting period, in ISO 8601 format
      - in: query
        name: end_updated_at
        description: If filtering results by their updated_at field, the end of the
          requested reporting period, in ISO 8601 format
      - in: query
        name: limit
        description: The maximum integer number of employee entities to return in
          a single response
      - in: query
        name: order
        description: The order in which timecards are listed in the response, based
          on their created_at field
      responses:
        200:
          description: OK
      tags:
      - Me
      - Timecards
  /me/timecards/{timecard_id}:
    get:
      summary: Get Me Timecards
      description: Provides the details for a single timecard.
      operationId: getMeTimecardsTimecard
      x-api-path-slug: metimecardstimecard-id-get
      parameters:
      - in: path
        name: timecard_id
        description: The timecards ID
      responses:
        200:
          description: OK
      tags:
      - Me
      - Timecards
    put:
      summary: Put Me Timecards
      description: Modifies a timecard's details. This creates an API_EDIT event for
        the timecard. You can view a timecard's event history with the List Timecard
        Events endpoint.
      operationId: putMeTimecardsTimecard
      x-api-path-slug: metimecardstimecard-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: timecard_id
        description: TThe ID of the timecard to modify
      responses:
        200:
          description: OK
      tags:
      - Me
      - Timecards
    delete:
      summary: Delete Me Timecards
      description: Deletes a timecard. Deleted timecards are still accessible from
        Connect API endpoints, but the value of their deleted field is set to true.
        See Handling deleted timecards for more information.
      operationId: deleteMeTimecardsTimecard
      x-api-path-slug: metimecardstimecard-id-delete
      parameters:
      - in: path
        name: timecard_id
        description: The ID of the timecard to delete
      responses:
        200:
          description: OK
      tags:
      - Me
      - Timecards
  /me/timecards/{timecard_id}/events:
    get:
      summary: Get Me Timecards Events
      description: Provides summary information for all events associated with a particular
        timecard.
      operationId: getMeTimecardsTimecardEvents
      x-api-path-slug: metimecardstimecard-idevents-get
      parameters:
      - in: path
        name: timecard_id
        description: The ID of the timecard to list events for
      responses:
        200:
          description: OK
      tags:
      - Me
      - Timecards
      - Events
  /{location_id}/cash-drawer-shifts:
    get:
      summary: Get Location Cash Drawer Shifts
      description: Provides the details for all of a location's cash drawer shifts
        during a date range. The date range you specify cannot exceed 90 days.
      operationId: getLocationCashDrawerShifts
      x-api-path-slug: location-idcashdrawershifts-get
      parameters:
      - in: query
        name: begin_time
        description: The beginning of the requested reporting period, in ISO 8601
          format
      - in: query
        name: end_time
        description: The beginning of the requested reporting period, in ISO 8601
          format
      - in: path
        name: location_id
        description: The ID of the location to list cash drawer shifts for
      - in: query
        name: order
        description: The order in which cash drawer shifts are listed in the response,
          based on their created_at field
      responses:
        200:
          description: OK
      tags:
      - Location
      - Cash-drawer-shifts
  /{location_id}/cash-drawer-shifts/{shift_id}:
    get:
      summary: Get Location Cash Drawer Shifts Shift
      description: Provides the details for a single cash drawer shift, including
        all events that occurred during the shift.
      operationId: getLocationCashDrawerShiftsShift
      x-api-path-slug: location-idcashdrawershiftsshift-id-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the location to list cash drawer shifts for
      - in: path
        name: shift_id
        description: The shifts ID
      responses:
        200:
          description: OK
      tags:
      - Location
      - Cash-drawer-shifts
      - Shift
  /{location_id}/payments:
    get:
      summary: Get Location Payments
      description: Provides summary information for all payments taken by a merchant
        or any of the merchant's mobile staff during a date range. Date ranges cannot
        exceed one year in length. See Date ranges for details of inclusive and exclusive
        dates.
      operationId: getLocationPayments
      x-api-path-slug: location-idpayments-get
      parameters:
      - in: query
        name: batch_token
        description: A pagination cursor to retrieve the next set of results for youroriginal
          query to the endpoint
      - in: query
        name: begin_time
        description: The beginning of the requested reporting period, in ISO 8601
          format
      - in: query
        name: end_time
        description: The end of the requested reporting period, in ISO 8601 format
      - in: query
        name: limit
        description: The maximum number of payments to return in a single response
      - in: path
        name: location_id
        description: The ID of the location to list payments for
      - in: query
        name: order
        description: The order in which payments are listed in the response
      responses:
        200:
          description: OK
      tags:
      - Location
      - Payments
  /{location_id}/payments/{payment_id}:
    get:
      summary: Get Location Payments Payment
      description: Provides comprehensive information for a single payment.
      operationId: getLocationPaymentsPayment
      x-api-path-slug: location-idpaymentspayment-id-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the payments associated location
      - in: path
        name: payment_id
        description: The Square-issued payment ID
      responses:
        200:
          description: OK
      tags:
      - Location
      - Payments
      - Payment
  /{location_id}/settlements:
    get:
      summary: Get Location Settlements
      description: Provides summary information for all deposits and withdrawals initiated
        by Square to a merchant's bank account during a date range. Date ranges cannot
        exceed one year in length.
      operationId: getLocationSettlements
      x-api-path-slug: location-idsettlements-get
      parameters:
      - in: query
        name: batch_token
        description: A pagination cursor to retrieve the next set of results for youroriginal
          query to the endpoint
      - in: query
        name: begin_time
        description: The beginning of the requested reporting period, in ISO 8601
          format
      - in: query
        name: end_time
        description: The end of the requested reporting period, in ISO 8601 format
      - in: query
        name: limit
        description: The maximum number of payments to return in a single response
      - in: path
        name: location_id
        description: The ID of the location to list settlements for
      - in: query
        name: order
        description: TThe order in which payments are listed in the response
      - in: query
        name: status
        description: Provide this parameter to retrieve only settlements with a particular
          status (SENT or FAILED)
      responses:
        200:
          description: OK
      tags:
      - Location
      - Settlements
  /{location_id}/settlements/{settlement_id}:
    get:
      summary: Get Location Settlements Settlement
      description: Provides comprehensive information for a single settlement, including
        the entries that contribute to the settlement's total.
      operationId: getLocationSettlementsSettlement
      x-api-path-slug: location-idsettlementssettlement-id-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the settlementss associated location
      - in: path
        name: settlement_id
        description: The settlements Square-issued ID
      responses:
        200:
          description: OK
      tags:
      - Location
      - Settlements
      - Settlement
  /{location_id}/refunds:
    get:
      summary: Get Location Refunds
      description: Provides the details for all refunds initiated by a merchant or
        any of the merchant's mobile staff during a date range. Date ranges cannot
        exceed one year in length.
      operationId: getLocationRefunds
      x-api-path-slug: location-idrefunds-get
      parameters:
      - in: query
        name: batch_token
        description: A pagination cursor to retrieve the next set of results for youroriginal
          query to the endpoint
      - in: query
        name: begin_time
        description: The beginning of the requested reporting period, in ISO 8601
          format
      - in: query
        name: end_time
        description: The end of the requested reporting period, in ISO 8601 format
      - in: query
        name: limit
        description: The approximate number of refunds to return in a single response
      - in: path
        name: location_id
        description: The ID of the location to list refunds for
      - in: query
        name: order
        description: TThe order in which payments are listed in the response
      responses:
        200:
          description: OK
      tags:
      - Location
      - Refunds
    post:
      summary: Post Location Refunds
      description: Issues a refund for a previously processed payment. You must issue
        a refund within 60 days of the associated payment.
      operationId: postLocationRefunds
      x-api-path-slug: location-idrefunds-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the original payments associated location
      responses:
        200:
          description: OK
      tags:
      - Location
      - Refunds
  /{location_id}/orders:
    get:
      summary: Get Location Orders
      description: Provides summary information for a merchant's online store orders.
      operationId: getLocationOrders
      x-api-path-slug: location-idorders-get
      parameters:
      - in: query
        name: batch_token
        description: A pagination cursor to retrieve the next set of results for youroriginal
          query to the endpoint
      - in: query
        name: limit
        description: The maximum number of payments to return in a single response
      - in: path
        name: location_id
        description: The ID of the location to list online store orders for
      - in: query
        name: order
        description: TThe order in which payments are listed in the response
      responses:
        200:
          description: OK
      tags:
      - Location
      - Orders
  /{location_id}/orders/{order_id}:
    get:
      summary: Get Location Orders Order
      description: Provides comprehensive information for a single online store order,
        including the order's history.
      operationId: getLocationOrdersOrder
      x-api-path-slug: location-idordersorder-id-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the orders associated location
      - in: path
        name: order_id
        description: The orders Square-issued ID
      responses:
        200:
          description: OK
      tags:
      - Location
      - Orders
      - Order
    put:
      summary: Put Location Orders Order
      description: 'Updates the details of an online store order. Every update you
        perform on an order corresponds to one of three actions:'
      operationId: putLocationOrdersOrder
      x-api-path-slug: location-idordersorder-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the orders associated location
      - in: path
        name: order_id
        description: The orders Square-issued ID
      responses:
        200:
          description: OK
      tags:
      - Location
      - Orders
      - Order
  /{location_id}/bank-accounts:
    get:
      summary: Get Location Bank Accounts
      description: Provides non-confidential details for all of a location's associated
        bank accounts. This endpoint does not provide full bank account numbers, and
        there is no way to obtain a full bank account number with the Connect API.
      operationId: getLocationBankAccounts
      x-api-path-slug: location-idbankaccounts-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the location to list bank accounts for
      responses:
        200:
          description: OK
      tags:
      - Location
      - Bank-accounts
  /{location_id}/bank-accounts/{bank_account_id}:
    get:
      summary: Get Location Bank Accounts Bank Account
      description: Provides non-confidential details for a merchant's associated bank
        account. This endpoint does not provide full bank account numbers, and there
        is no way to obtain a full bank account number with the Connect API.
      operationId: getLocationBankAccountsBankAccount
      x-api-path-slug: location-idbankaccountsbank-account-id-get
      parameters:
      - in: path
        name: bank_account_id
        description: The bank accounts Square-issued ID
      - in: path
        name: location_id
        description: The ID of the bank accounts associated location
      responses:
        200:
          description: OK
      tags:
      - Location
      - Bank-accounts
      - Bank
      - Account
  /{location_id}/items:
    post:
      summary: Post Location Items
      description: Creates an item and at least one variation for it.
      operationId: postLocationItems
      x-api-path-slug: location-iditems-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the location to create an item for
      responses:
        200:
          description: OK
      tags:
      - Location
      - Items
    get:
      summary: Get Location Items
      description: Provides summary information for all of a location's items.
      operationId: getLocationItems
      x-api-path-slug: location-iditems-get
      parameters:
      - in: query
        name: batch_token
        description: A pagination cursor to retrieve the next set of results for youroriginal
          query to the endpoint
      - in: path
        name: location_id
        description: The ID of the location to list items for
      responses:
        200:
          description: OK
      tags:
      - Location
      - Items
  /{location_id}/items/{item_id}:
    get:
      summary: Get Location Items Item
      description: Provides the details for a single item, including associated modifier
        lists and fees.
      operationId: getLocationItemsItem
      x-api-path-slug: location-iditemsitem-id-get
      parameters:
      - in: path
        name: item_id
        description: The items ID
      - in: path
        name: location_id
        description: The ID of the items associated location
      responses:
        200:
          description: OK
      tags:
      - Location
      - Items
    put:
      summary: Put Location Items Item
      description: Modifies the core details of an existing item.
      operationId: putLocationItemsItem
      x-api-path-slug: location-iditemsitem-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: item_id
        description: The ID of the item to modify
      - in: path
        name: location_id
        description: The ID of the items associated location
      responses:
        200:
          description: OK
      tags:
      - Location
      - Items
    delete:
      summary: Delete Location Items Item
      description: Deletes an existing item and all item variations associated with
        it.
      operationId: deleteLocationItemsItem
      x-api-path-slug: location-iditemsitem-id-delete
      parameters:
      - in: path
        name: item_id
        description: The ID of the item to modify
      - in: path
        name: location_id
        description: The ID of the items associated location
      responses:
        200:
          description: OK
      tags:
      - Location
      - Items
  /{location_id}/items/{item_id}/variations:
    post:
      summary: Post Location Items Item Variations
      description: Creates an item variation for an existing item.
      operationId: postLocationItemsItemVariations
      x-api-path-slug: location-iditemsitem-idvariations-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: item_id
        description: The items ID
      - in: path
        name: location_id
        description: The ID of the items associated location
      responses:
        200:
          description: OK
      tags:
      - Location
      - Items
      - Variations
  /{location_id}/items/{item_id}/variations/{variation_id}:
    put:
      summary: Put Location Items Item Variations Variation
      description: Modifies the details of an existing item variation.
      operationId: putLocationItemsItemVariationsVariation
      x-api-path-slug: location-iditemsitem-idvariationsvariation-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: item_id
        description: The ID of the item to modify
      - in: path
        name: location_id
        description: The ID of the items associated location
      - in: path
        name: variation_id
        description: The ID of the variation to modify
      responses:
        200:
          description: OK
      tags:
      - Location
      - Items
      - Variations
      - Variation
    delete:
      summary: Delete Location Items Item Variations Variation
      description: Deletes an existing item variation from an item.
      operationId: deleteLocationItemsItemVariationsVariation
      x-api-path-slug: location-iditemsitem-idvariationsvariation-id-delete
      parameters:
      - in: path
        name: item_id
        description: The ID of the item to delete
      - in: path
        name: location_id
        description: The ID of the items associated location
      - in: path
        name: variation_id
        description: The ID of the variation to delete
      responses:
        200:
          description: OK
      tags:
      - Location
      - Items
      - Variations
      - Variation
  /{location_id}/inventory:
    get:
      summary: Get Location Inventory
      description: Provides inventory information for all of a merchant's inventory-enabled
        item variations.
      operationId: getLocationInventory
      x-api-path-slug: location-idinventory-get
      parameters:
      - in: query
        name: batch_token
        description: A pagination cursor to retrieve the next set of results for youroriginal
          query to the endpoint
      - in: query
        name: limit
        description: The maximum number of inventory entries to return in a single
          response
      - in: path
        name: location_id
        description: The ID of the items associated location
      responses:
        200:
          description: OK
      tags:
      - Location
      - Inventory
  /{location_id}/inventory/{variation_id}:
    post:
      summary: Post Location Inventory Variation
      description: Adjusts an item variation's current available inventory.
      operationId: postLocationInventoryVariation
      x-api-path-slug: location-idinventoryvariation-id-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the items associated location
      - in: path
        name: variation_id
        description: The ID of the variation to adjust inventory information for
      responses:
        200:
          description: OK
      tags:
      - Location
      - Inventory
      - Variation
  /{location_id}/modifier-lists:
    post:
      summary: Post Location Modifier Lists
      description: Creates an item modifier list and at least one modifier option
        for it.
      operationId: postLocationModifierLists
      x-api-path-slug: location-idmodifierlists-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the location to create a modifier list for
      responses:
        200:
          description: OK
      tags:
      - Location
      - Modifier-lists
    get:
      summary: Get Location Modifier Lists
      description: Lists all of a location's modifier lists.
      operationId: getLocationModifierLists
      x-api-path-slug: location-idmodifierlists-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the location to list modifier lists for
      responses:
        200:
          description: OK
      tags:
      - Location
      - Modifier-lists
  /{location_id}/modifier-lists/{modifier_list_id}:
    get:
      summary: Get Location Modifier Lists Modifier List
      description: Provides the details for a single modifier list.
      operationId: getLocationModifierListsModifierList
      x-api-path-slug: location-idmodifierlistsmodifier-list-id-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the items associated location
      - in: path
        name: modifier_list_id
        description: The modifier lists ID
      responses:
        200:
          description: OK
      tags:
      - Location
      - Modifier-lists
      - Modifier
      - List
    put:
      summary: Put Location Modifier Lists Modifier List
      description: Modifies the details of an existing item modifier list.
      operationId: putLocationModifierListsModifierList
      x-api-path-slug: location-idmodifierlistsmodifier-list-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the items associated location
      - in: path
        name: modifier_list_id
        description: The ID of the modifier list to edit
      responses:
        200:
          description: OK
      tags:
      - Location
      - Modifier-lists
      - Modifier
      - List
    delete:
      summary: Delete Location Modifier Lists Modifier List
      description: Deletes an existing item modifier list and all modifier options
        associated with it.
      operationId: deleteLocationModifierListsModifierList
      x-api-path-slug: location-idmodifierlistsmodifier-list-id-delete
      parameters:
      - in: path
        name: location_id
        description: The ID of the items associated location
      - in: path
        name: modifier_list_id
        description: The ID of the modifier list to delete
      responses:
        200:
          description: OK
      tags:
      - Location
      - Modifier-lists
      - Modifier
      - List
  /{location_id}/items/{item_id}/modifier-lists/{modifier_list_id}:
    put:
      summary: Put Location Items Item Modifier Lists Modifier List
      description: Associates a modifier list with an item, meaning modifier options
        from the list can be applied to the item.
      operationId: putLocationItemsItemModifierListsModifierList
      x-api-path-slug: location-iditemsitem-idmodifierlistsmodifier-list-id-put
      parameters:
      - in: path
        name: item_id
        description: The ID of the item to add the modifier list to
      - in: path
        name: location_id
        description: The ID of the items associated location
      - in: path
        name: modifier_list_id
        description: The ID of the modifier list to apply
      responses:
        200:
          description: OK
      tags:
      - Location
      - Items
      - Modifier-lists
      - Modifier
      - List
    delete:
      summary: Delete Location Items Item Modifier Lists Modifier List
      description: Removes a modifier list association from an item, meaning modifier
        options from the list can no longer be applied to the item.
      operationId: deleteLocationItemsItemModifierListsModifierList
      x-api-path-slug: location-iditemsitem-idmodifierlistsmodifier-list-id-delete
      parameters:
      - in: path
        name: item_id
        description: The ID of the item to remove the modifier list from
      - in: path
        name: location_id
        description: The ID of the items associated location
      - in: path
        name: modifier_list_id
        description: The ID of the modifier list to remove
      responses:
        200:
          description: OK
      tags:
      - Location
      - Items
      - Modifier-lists
      - Modifier
      - List
  /{location_id}/modifier-lists/{modifier_list_id}/modifier-options:
    post:
      summary: Post Location Modifier Lists Modifier List Modifier Options
      description: Creates an item modifier option and adds it to a modifier list.
      operationId: postLocationModifierListsModifierListModifierOptions
      x-api-path-slug: location-idmodifierlistsmodifier-list-idmodifieroptions-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the items associated location
      - in: path
        name: modifier_list_id
        description: The ID of the modifier list to edit
      responses:
        200:
          description: OK
      tags:
      - Location
      - Modifier-lists
      - Modifier
      - List
      - Modifier-options
  /{location_id}/modifier-lists/{modifier_list_id}/modifier-options/{modifier_option_id}:
    put:
      summary: Put Location Modifier Lists Modifier List Modifier Options Modifier
        Option
      description: Put location modifier lists modifier list modifier options modifier
        option.
      operationId: putLocationModifierListsModifierListModifierOptionsModifierOption
      x-api-path-slug: location-idmodifierlistsmodifier-list-idmodifieroptionsmodifier-option-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the items associated location
      - in: path
        name: modifier_list_id
        description: The ID of the modifier list to edit
      - in: path
        name: modifier_option_id
        description: The ID of the modifier list to edit
      responses:
        200:
          description: OK
      tags:
      - Location
      - Modifier-lists
      - Modifier
      - List
      - Modifier-options
      - Modifier
      - Option
    delete:
      summary: Delete Location Modifier Lists Modifier List Modifier Options Modifier
        Option
      description: Delete location modifier lists modifier list modifier options modifier
        option.
      operationId: deleteLocationModifierListsModifierListModifierOptionsModifierOption
      x-api-path-slug: location-idmodifierlistsmodifier-list-idmodifieroptionsmodifier-option-id-delete
      parameters:
      - in: path
        name: location_id
        description: The ID of the items associated location
      - in: path
        name: modifier_list_id
        description: The ID of the modifier list to delete
      - in: path
        name: modifier_option_id
        description: The ID of the modifier list to edit
      responses:
        200:
          description: OK
      tags:
      - Location
      - Modifier-lists
      - Modifier
      - List
      - Modifier-options
      - Modifier
      - Option
  /{location_id}/categories:
    post:
      summary: Post Location Categories
      description: Creates an item category.
      operationId: postLocationCategories
      x-api-path-slug: location-idcategories-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the location to create an item for
      responses:
        200:
          description: OK
      tags:
      - Location
      - Categories
    get:
      summary: Get Location Categories
      description: Lists all of a location's item categories.
      operationId: getLocationCategories
      x-api-path-slug: location-idcategories-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the location to list categories for
      responses:
        200:
          description: OK
      tags:
      - Location
      - Categories
  /{location_id}/categories/{category_id}:
    put:
      summary: Put Location Categories Category
      description: Modifies the details of an existing item category.
      operationId: putLocationCategoriesCategory
      x-api-path-slug: location-idcategoriescategory-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: category_id
        description: The ID of the category to edit
      - in: path
        name: location_id
        description: The ID of the categorys associated location
      responses:
        200:
          description: OK
      tags:
      - Location
      - Categories
      - Category
    delete:
      summary: Delete Location Categories Category
      description: Delete location categories category.
      operationId: deleteLocationCategoriesCategory
      x-api-path-slug: location-idcategoriescategory-id-delete
      parameters:
      - in: path
        name: category_id
        description: The ID of the category to delete
      - in: path
        name: location_id
        description: The ID of the items associated location
      responses:
        200:
          description: OK
      tags:
      - Location
      - Categories
      - Category
  /{location_id}/discounts:
    post:
      summary: Post Location Discounts
      description: Post location discounts.
      operationId: postLocationDiscounts
      x-api-path-slug: location-iddiscounts-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the location to create an item for
      responses:
        200:
          description: OK
      tags:
      - Location
      - Discounts
    get:
      summary: Get Location Discounts
      description: Lists all of a location's discounts.
      operationId: getLocationDiscounts
      x-api-path-slug: location-iddiscounts-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the location to list categories for
      responses:
        200:
          description: OK
      tags:
      - Location
      - Discounts
  /{location_id}/discounts/{discount_id}:
    put:
      summary: Put Location Discounts Discount
      description: Modifies the details of an existing discount.
      operationId: putLocationDiscountsDiscount
      x-api-path-slug: location-iddiscountsdiscount-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: discount_id
        description: The ID of the discount to edit
      - in: path
        name: location_id
        description: The ID of the categorys associated location
      responses:
        200:
          description: OK
      tags:
      - Location
      - Discounts
    delete:
      summary: Delete Location Discounts Discount
      description: Delete location discounts discount.
      operationId: deleteLocationDiscountsDiscount
      x-api-path-slug: location-iddiscountsdiscount-id-delete
      parameters:
      - in: path
        name: discount_id
        description: The ID of the discount to delete
      - in: path
        name: location_id
        description: The ID of the items associated location
      responses:
        200:
          description: OK
      tags:
      - Location
      - Discounts
  /{location_id}/fees:
    post:
      summary: Post Location Fees
      description: Creates a fee (tax).
      operationId: postLocationFees
      x-api-path-slug: location-idfees-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the location to create a fee for
      responses:
        200:
          description: OK
      tags:
      - Location
      - Fees
    get:
      summary: Get Location Fees
      description: Lists all of a location's fees (taxes).
      operationId: getLocationFees
      x-api-path-slug: location-idfees-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the location to list fees for
      responses:
        200:
          description: OK
      tags:
      - Location
      - Fees
  /{location_id}/fees/{fee_id}:
    put:
      summary: Put Location Fees Fee
      description: Modifies the details of an existing fee (tax).
      operationId: putLocationFeesFee
      x-api-path-slug: location-idfeesfee-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: fee_id
        description: The ID of the fee to edit
      - in: path
        name: location_id
        description: The ID of the fees associated location
      responses:
        200:
          description: OK
      tags:
      - Location
      - Fees
      - Fee
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