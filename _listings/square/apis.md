---
name: Square
x-slug: square
description: Starting with a free credit card reader for the iPhone, iPad, and Android
  devices, Square Reader allows anyone to accept credit cards anywhere, anytime, for
  a low transaction rate of 2.75 percent per swipe, with no hidden fees. Square Register
  serves as a full point-of-sale system for businesses to accept payments, manage
  items, and share menu and location information. Square Wallet, available in the
  US, is the most seamless way to pay, enabling individuals to pay at their favorite
  local businesses, discover new ones nearby, explore menu listings, and store receipts.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
x-kinRank: "9"
x-alexaRank: ""
tags: Square
created: "2018-05-22"
modified: "2018-05-22"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/apis.md
specificationVersion: "0.14"
apis:
- name: Square Connect API Post V2 Apple Pay Domains
  x-api-slug: square-connect-api
  description: |-
    Activates a domain for use with Web Apple Pay and Square. A validation
    will be performed on this domain by Apple to ensure is it properly set up as
    an Apple Pay enabled domain.

    This endpoint provides an easy way for platform developers to bulk activate
    Web Apple Pay with Square for merchants using their platform.

    To learn more about Apple Pay on Web see the Apple Pay section in the [Embedding the Square Payment Form](https://docs.connect.squareup.com/articles/adding-payment-form) guide.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/apple-pay/domains
  tags: Apple-pay,Domains
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2applepaydomains-post-openapi.md
- name: Square Connect API Post V2 Catalog Batch Delete
  x-api-slug: square-connect-api
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/catalog/batch-delete
  tags: Catalog,Batch-delete
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogbatchdelete-post-openapi.md
- name: Square Connect API Post V2 Catalog Batch Retrieve
  x-api-slug: square-connect-api
  description: |-
    Returns a set of objects based on the provided ID.
    Each [CatalogItem](#type-catalogitem) returned in the set includes all of its
    child information including: all of its
    [CatalogItemVariation](#type-catalogitemvariation) objects, references to
    its [CatalogModifierList](#type-catalogmodifierlist) objects, and the ids of
    any [CatalogTax](#type-catalogtax) objects that apply to it.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/catalog/batch-retrieve
  tags: Catalog,Batch-retrieve
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogbatchretrieve-post-openapi.md
- name: Square Connect API Post V2 Catalog Batch Upsert
  x-api-slug: square-connect-api
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/catalog/batch-upsert
  tags: Catalog,Batch-upsert
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogbatchupsert-post-openapi.md
- name: Square Connect API Get V2 Catalog Info
  x-api-slug: square-connect-api
  description: |-
    Returns information about the Square Catalog API, such as batch size
    limits for `BatchUpsertCatalogObjects`.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/catalog/info
  tags: Catalog,Info
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2cataloginfo-get-openapi.md
- name: Square Connect API Get V2 Catalog List
  x-api-slug: square-connect-api
  description: |-
    Returns a list of [CatalogObject](#type-catalogobject)s that includes
    all objects of a set of desired types (for example, all [CatalogItem](#type-catalogitem)
    and [CatalogTax](#type-catalogtax) objects) in the catalog. The types parameter
    is specified as a comma-separated list of valid [CatalogObject](#type-catalogobject) types:
    `ITEM`, `ITEM_VARIATION`, `MODIFIER`, `MODIFIER_LIST`, `CATEGORY`, `DISCOUNT`, `TAX`.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/catalog/list
  tags: Catalog,List
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2cataloglist-get-openapi.md
- name: Square Connect API Post V2 Catalog Object
  x-api-slug: square-connect-api
  description: Creates or updates the target [CatalogObject](#type-catalogobject).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/catalog/object
  tags: Catalog,Object
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogobject-post-openapi.md
- name: Square Connect API Delete V2 Catalog Object Object
  x-api-slug: square-connect-api
  description: |-
    Deletes a single [CatalogObject](#type-catalogobject) based on the
    provided ID and returns the set of successfully deleted IDs in the response.
    Deletion is a cascading event such that all children of the targeted object
    are also deleted. For example, deleting a [CatalogItem](#type-catalogitem)
    will also delete all of its
    [CatalogItemVariation](#type-catalogitemvariation) children.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/catalog/object/{object_id}
  tags: Catalog,Object,Object
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogobjectobject-id-delete-openapi.md
- name: Square Connect API Get V2 Catalog Object Object
  x-api-slug: square-connect-api
  description: |-
    Returns a single [CatalogItem](#type-catalogitem) as a
    [CatalogObject](#type-catalogobject) based on the provided ID. The returned
    object includes all of the relevant [CatalogItem](#type-catalogitem)
    information including: [CatalogItemVariation](#type-catalogitemvariation)
    children, references to its
    [CatalogModifierList](#type-catalogmodifierlist) objects, and the ids of
    any [CatalogTax](#type-catalogtax) objects that apply to it.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/catalog/object/{object_id}
  tags: Catalog,Object,Object
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogobjectobject-id-get-openapi.md
- name: Square Connect API Post V2 Catalog Search
  x-api-slug: square-connect-api
  description: |-
    Queries the targeted catalog using a variety of query types:
    [CatalogQuerySortedAttribute](#type-catalogquerysortedattribute),
    [CatalogQueryExact](#type-catalogqueryexact),
    [CatalogQueryRange](#type-catalogqueryrange),
    [CatalogQueryText](#type-catalogquerytext),
    [CatalogQueryItemsForTax](#type-catalogqueryitemsfortax), and
    [CatalogQueryItemsForModifierList](#type-catalogqueryitemsformodifierlist).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/catalog/search
  tags: Catalog,Search
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogsearch-post-openapi.md
- name: Square Connect API Post V2 Catalog Update Item Modifier Lists
  x-api-slug: square-connect-api
  description: |-
    Updates the [CatalogModifierList](#type-catalogmodifierlist) objects
    that apply to the targeted [CatalogItem](#type-catalogitem) without having
    to perform an upsert on the entire item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/catalog/update-item-modifier-lists
  tags: Catalog,Update-item-modifier-lists
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogupdateitemmodifierlists-post-openapi.md
- name: Square Connect API Post V2 Catalog Update Item Taxes
  x-api-slug: square-connect-api
  description: |-
    Updates the [CatalogTax](#type-catalogtax) objects that apply to the
    targeted [CatalogItem](#type-catalogitem) without having to perform an
    upsert on the entire item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/catalog/update-item-taxes
  tags: Catalog,Update-item-taxes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogupdateitemtaxes-post-openapi.md
- name: Square Connect API Get V2 Customers
  x-api-slug: square-connect-api
  description: Lists a business's customers.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/customers
  tags: Customers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customers-get-openapi.md
- name: Square Connect API Post V2 Customers
  x-api-slug: square-connect-api
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/customers
  tags: Customers
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customers-post-openapi.md
- name: Square Connect API Delete V2 Customers Customer
  x-api-slug: square-connect-api
  description: Deletes a customer from a business, along with any linked cards on
    file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/customers/{customer_id}
  tags: Customers,Customer
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-id-delete-openapi.md
- name: Square Connect API Get V2 Customers Customer
  x-api-slug: square-connect-api
  description: Returns details for a single customer.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/customers/{customer_id}
  tags: Customers,Customer
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-id-get-openapi.md
- name: Square Connect API Put V2 Customers Customer
  x-api-slug: square-connect-api
  description: |-
    Updates the details of an existing customer.
    The ID of the customer may change if the customer has been merged into another customer.

    You cannot edit a customer's cards on file with this endpoint. To make changes
    to a card on file, you must delete the existing card on file with the
    [DeleteCustomerCard](#endpoint-deletecustomercard) endpoint, then create a new one with the
    [CreateCustomerCard](#endpoint-createcustomercard) endpoint.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/customers/{customer_id}
  tags: Customers,Customer
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-id-put-openapi.md
- name: Square Connect API Post V2 Customers Customer Cards
  x-api-slug: square-connect-api
  description: |-
    Adds a card on file to an existing customer. In the United States
    Square takes care of automatically updating any cards on file that might
    have expired since you first attached them to a customer.

    As with charges, calls to `CreateCustomerCard` are idempotent. Multiple
    calls with the same card nonce return the same card record that was created
    with the provided nonce during the _first_ call.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/customers/{customer_id}/cards
  tags: Customers,Customer,Cards
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-idcards-post-openapi.md
- name: Square Connect API Delete V2 Customers Customer Cards Card
  x-api-slug: square-connect-api
  description: Delete v2 customers customer cards card.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/customers/{customer_id}/cards/{card_id}
  tags: Customers,Customer,Cards,Card
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-idcardscard-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-idcardscard-id-delete-openapi.md
- name: Square Connect API Get V2 Locations
  x-api-slug: square-connect-api
  description: |-
    Provides the details for all of a business's locations.

    Most other Connect API endpoints have a required `location_id` path parameter.
    The `id` field of the [`Location`](#type-location) objects returned by this
    endpoint correspond to that `location_id` parameter.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations
  tags: Locations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locations-get-openapi.md
- name: Square Connect API Get V2 Locations Location Additional Recipient Receivable
    Refunds
  x-api-slug: square-connect-api
  description: |-
    Returns a list of refunded transactions (across all possible originating locations) relating to monies
    credited to the provided location ID by another Square account using the `additional_recipients` field in a transaction.

    Max results per [page](#paginatingresults): 50
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations/{location_id}/additional-recipient-receivable-refunds
  tags: Locations,Location,Additional-recipient-receivable-refunds
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idadditionalrecipientreceivablerefunds-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idadditionalrecipientreceivablerefunds-get-openapi.md
- name: Square Connect API Get V2 Locations Location Additional Recipient Receivables
  x-api-slug: square-connect-api
  description: |-
    Returns a list of receivables (across all possible sending locations) representing monies credited
    to the provided location ID by another Square account using the `additional_recipients` field in a transaction.

    Max results per [page](#paginatingresults): 50
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations/{location_id}/additional-recipient-receivables
  tags: Locations,Location,Additional-recipient-receivables
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idadditionalrecipientreceivables-get-openapi.md
- name: Square Connect API Post V2 Locations Location Checkouts
  x-api-slug: square-connect-api
  description: |-
    Creates a [Checkout](#type-checkout) response that links a
    `checkoutId` and `checkout_page_url` that customers can be directed to in
    order to provide their payment information using a payment processing
    workflow hosted on connect.squareup.com.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations/{location_id}/checkouts
  tags: Locations,Location,Checkouts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idcheckouts-post-openapi.md
- name: Square Connect API Post V2 Locations Location Orders
  x-api-slug: square-connect-api
  description: |-
    Creates an [Order](#type-order) that can then be referenced as `order_id` in a
    request to the [Charge](#endpoint-charge) endpoint. Orders specify products for
    purchase, along with discounts, taxes, and other settings to apply to the purchase.

    To associate a created order with a request to the Charge endpoint, provide the
    order's `id` in the `order_id` field of your request.

    You cannot modify an order after you create it. If you need to modify an order,
    instead create a new order with modified details.

    To learn more about the Orders API, see the [Orders API Overview](https://docs.connect.squareup.com/articles/orders-api-overview).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations/{location_id}/orders
  tags: Locations,Location,Orders
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idorders-post-openapi.md
- name: Square Connect API Post V2 Locations Location Orders Batch Retrieve
  x-api-slug: square-connect-api
  description: |-
    Retrieves a set of [Order](#type-order)s by their IDs.

    If a given Order ID does not exist, the ID is ignored instead of generating an error.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations/{location_id}/orders/batch-retrieve
  tags: Locations,Location,Orders,Batch-retrieve
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idordersbatchretrieve-post-openapi.md
- name: Square Connect API Get V2 Locations Location Refunds
  x-api-slug: square-connect-api
  description: |-
    Lists refunds for one of a business's locations.

    In addition to full or partial tender refunds processed through Square APIs,
    refunds may result from itemized returns or exchanges through Square's
    Point of Sale applications.

    Refunds with a `status` of `PENDING` are not currently included in this
    endpoint's response.

    Max results per [page](#paginatingresults): 50
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations/{location_id}/refunds
  tags: Locations,Location,Refunds
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idrefunds-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idrefunds-get-openapi.md
- name: Square Connect API Get V2 Locations Location Transactions
  x-api-slug: square-connect-api
  description: |-
    Lists transactions for a particular location.

    Transactions include payment information from sales and exchanges and refund
    information from returns and exchanges.

    Max results per [page](#paginatingresults): 50
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations/{location_id}/transactions
  tags: Locations,Location,Transactions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactions-get-openapi.md
- name: Square Connect API Post V2 Locations Location Transactions
  x-api-slug: square-connect-api
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations/{location_id}/transactions
  tags: Locations,Location,Transactions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactions-post-openapi.md
- name: Square Connect API Get V2 Locations Location Transactions Transaction
  x-api-slug: square-connect-api
  description: Get v2 locations location transactions transaction.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations/{location_id}/transactions/{transaction_id}
  tags: Locations,Location,Transactions,Transaction
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactionstransaction-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactionstransaction-id-get-openapi.md
- name: Square Connect API Post V2 Locations Location Transactions Transaction Capture
  x-api-slug: square-connect-api
  description: |-
    Captures a transaction that was created with the [Charge](#endpoint-charge)
    endpoint with a `delay_capture` value of `true`.

    See [Delayed capture transactions](/articles/delayed-capture-transactions/)
    for more information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations/{location_id}/transactions/{transaction_id}/capture
  tags: Locations,Location,Transactions,Transaction,Capture
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactionstransaction-idcapture-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactionstransaction-idcapture-post-openapi.md
- name: Square Connect API Post V2 Locations Location Transactions Transaction Refund
  x-api-slug: square-connect-api
  description: |-
    Initiates a refund for a previously charged tender.

    You must issue a refund within 120 days of the associated payment. See
    [this article](https://squareup.com/help/us/en/article/5060) for more information
    on refund behavior.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations/{location_id}/transactions/{transaction_id}/refund
  tags: Locations,Location,Transactions,Transaction,Refund
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactionstransaction-idrefund-post-openapi.md
- name: Square Connect API Post V2 Locations Location Transactions Transaction Vo
  x-api-slug: square-connect-api
  description: |-
    Cancels a transaction that was created with the [Charge](#endpoint-charge)
    endpoint with a `delay_capture` value of `true`.

    See [Delayed capture transactions](/articles/delayed-capture-transactions/)
    for more information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///v2/locations/{location_id}/transactions/{transaction_id}/void
  tags: Locations,Location,Transactions,Transaction,Void
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactionstransaction-idvoid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactionstransaction-idvoid-post-openapi.md
- name: Square Connect API Get Me
  x-api-slug: square-connect-api
  description: Get a business's information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me
  tags: Me
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/me-get-openapi.md
- name: Square Connect API Get Me Locations
  x-api-slug: square-connect-api
  description: Provides details for a business's locations, including their IDs.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/locations
  tags: Me,Locations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/melocations-get-openapi.md
- name: Square Connect API Post Me Employees
  x-api-slug: square-connect-api
  description: Creates an employee for a business.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/employees
  tags: Me,Employees
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/meemployees-post-openapi.md
- name: Square Connect API Get Me Employees
  x-api-slug: square-connect-api
  description: Provides summary information for all of a business's employees.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/employees
  tags: Me,Employees
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/meemployees-get-openapi.md
- name: Square Connect API Get Me Employees Employee
  x-api-slug: square-connect-api
  description: Provides the details for a single employee.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/employees/{employee_id}
  tags: Me,Employees
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/meemployeesemployee-id-get-openapi.md
- name: Square Connect API Put Me Employees Employee
  x-api-slug: square-connect-api
  description: Put me employees employee.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/employees/{employee_id}
  tags: Me,Employees
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/meemployeesemployee-id-put-openapi.md
- name: Square Connect API Post Me Roles
  x-api-slug: square-connect-api
  description: Creates an employee role you can then assign to employees.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/roles
  tags: Me,Roles
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/meroles-post-openapi.md
- name: Square Connect API Get Me Roles
  x-api-slug: square-connect-api
  description: Provides summary information for all of a business's employee roles.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/roles
  tags: Me,Roles
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/meroles-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/meroles-get-openapi.md
- name: Square Connect API Get Me Roles Role
  x-api-slug: square-connect-api
  description: Provides the details for a single employee role.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/roles/{role_id}
  tags: Me,Roles
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/merolesrole-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/merolesrole-id-get-openapi.md
- name: Square Connect API Put Me Roles Role
  x-api-slug: square-connect-api
  description: Modifies the details of an employee role.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/roles/{role_id}
  tags: Me,Roles
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/merolesrole-id-put-openapi.md
- name: Square Connect API Post Me Timecards
  x-api-slug: square-connect-api
  description: Creates a timecard for an employee. Each timecard corresponds to a
    single shift.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/timecards
  tags: Me,Timecards
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/metimecards-post-openapi.md
- name: Square Connect API Get Me Timecards
  x-api-slug: square-connect-api
  description: Provides summary information for all of a business's employee timecards.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/timecards
  tags: Me,Timecards
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/metimecards-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/metimecards-get-openapi.md
- name: Square Connect API Get Me Timecards
  x-api-slug: square-connect-api
  description: Provides the details for a single timecard.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/timecards/{timecard_id}
  tags: Me,Timecards
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/metimecardstimecard-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/metimecardstimecard-id-get-openapi.md
- name: Square Connect API Put Me Timecards
  x-api-slug: square-connect-api
  description: Modifies a timecard's details. This creates an API_EDIT event for the
    timecard. You can view a timecard's event history with the List Timecard Events
    endpoint.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/timecards/{timecard_id}
  tags: Me,Timecards
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/metimecardstimecard-id-put-openapi.md
- name: Square Connect API Delete Me Timecards
  x-api-slug: square-connect-api
  description: Deletes a timecard. Deleted timecards are still accessible from Connect
    API endpoints, but the value of their deleted field is set to true. See Handling
    deleted timecards for more information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/timecards/{timecard_id}
  tags: Me,Timecards
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/metimecardstimecard-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/metimecardstimecard-id-delete-openapi.md
- name: Square Connect API Get Me Timecards Events
  x-api-slug: square-connect-api
  description: Provides summary information for all events associated with a particular
    timecard.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///me/timecards/{timecard_id}/events
  tags: Me,Timecards,Events
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/metimecardstimecard-idevents-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/metimecardstimecard-idevents-get-openapi.md
- name: Square Connect API Get Location Cash Drawer Shifts
  x-api-slug: square-connect-api
  description: Provides the details for all of a location's cash drawer shifts during
    a date range. The date range you specify cannot exceed 90 days.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/cash-drawer-shifts
  tags: Location,Cash-drawer-shifts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idcashdrawershifts-get-openapi.md
- name: Square Connect API Get Location Cash Drawer Shifts Shift
  x-api-slug: square-connect-api
  description: Provides the details for a single cash drawer shift, including all
    events that occurred during the shift.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/cash-drawer-shifts/{shift_id}
  tags: Location,Cash-drawer-shifts,Shift
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idcashdrawershiftsshift-id-get-openapi.md
- name: Square Connect API Get Location Payments
  x-api-slug: square-connect-api
  description: Provides summary information for all payments taken by a merchant or
    any of the merchant's mobile staff during a date range. Date ranges cannot exceed
    one year in length. See Date ranges for details of inclusive and exclusive dates.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/payments
  tags: Location,Payments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpayments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpayments-get-openapi.md
- name: Square Connect API Get Location Payments Payment
  x-api-slug: square-connect-api
  description: Provides comprehensive information for a single payment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/payments/{payment_id}
  tags: Location,Payments,Payment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpaymentspayment-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpaymentspayment-id-get-openapi.md
- name: Square Connect API Get Location Settlements
  x-api-slug: square-connect-api
  description: Provides summary information for all deposits and withdrawals initiated
    by Square to a merchant's bank account during a date range. Date ranges cannot
    exceed one year in length.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/settlements
  tags: Location,Settlements
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idsettlements-get-openapi.md
- name: Square Connect API Get Location Settlements Settlement
  x-api-slug: square-connect-api
  description: Provides comprehensive information for a single settlement, including
    the entries that contribute to the settlement's total.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/settlements/{settlement_id}
  tags: Location,Settlements,Settlement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idsettlementssettlement-id-get-openapi.md
- name: Square Connect API Get Location Refunds
  x-api-slug: square-connect-api
  description: Provides the details for all refunds initiated by a merchant or any
    of the merchant's mobile staff during a date range. Date ranges cannot exceed
    one year in length.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/refunds
  tags: Location,Refunds
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idrefunds-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idrefunds-get-openapi.md
- name: Square Connect API Post Location Refunds
  x-api-slug: square-connect-api
  description: Issues a refund for a previously processed payment. You must issue
    a refund within 60 days of the associated payment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/refunds
  tags: Location,Refunds
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idrefunds-post-openapi.md
- name: Square Connect API Get Location Orders
  x-api-slug: square-connect-api
  description: Provides summary information for a merchant's online store orders.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/orders
  tags: Location,Orders
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idorders-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idorders-get-openapi.md
- name: Square Connect API Get Location Orders Order
  x-api-slug: square-connect-api
  description: Provides comprehensive information for a single online store order,
    including the order's history.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/orders/{order_id}
  tags: Location,Orders,Order
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idordersorder-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idordersorder-id-get-openapi.md
- name: Square Connect API Put Location Orders Order
  x-api-slug: square-connect-api
  description: 'Updates the details of an online store order. Every update you perform
    on an order corresponds to one of three actions:'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/orders/{order_id}
  tags: Location,Orders,Order
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idordersorder-id-put-openapi.md
- name: Square Connect API Get Location Bank Accounts
  x-api-slug: square-connect-api
  description: Provides non-confidential details for all of a location's associated
    bank accounts. This endpoint does not provide full bank account numbers, and there
    is no way to obtain a full bank account number with the Connect API.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/bank-accounts
  tags: Location,Bank-accounts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idbankaccounts-get-openapi.md
- name: Square Connect API Get Location Bank Accounts Bank Account
  x-api-slug: square-connect-api
  description: Provides non-confidential details for a merchant's associated bank
    account. This endpoint does not provide full bank account numbers, and there is
    no way to obtain a full bank account number with the Connect API.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/bank-accounts/{bank_account_id}
  tags: Location,Bank-accounts,Bank,Account
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idbankaccountsbank-account-id-get-openapi.md
- name: Square Connect API Post Location Items
  x-api-slug: square-connect-api
  description: Creates an item and at least one variation for it.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/items
  tags: Location,Items
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditems-post-openapi.md
- name: Square Connect API Get Location Items
  x-api-slug: square-connect-api
  description: Provides summary information for all of a location's items.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/items
  tags: Location,Items
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditems-get-openapi.md
- name: Square Connect API Get Location Items Item
  x-api-slug: square-connect-api
  description: Provides the details for a single item, including associated modifier
    lists and fees.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/items/{item_id}
  tags: Location,Items
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-id-get-openapi.md
- name: Square Connect API Put Location Items Item
  x-api-slug: square-connect-api
  description: Modifies the core details of an existing item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/items/{item_id}
  tags: Location,Items
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-id-put-openapi.md
- name: Square Connect API Delete Location Items Item
  x-api-slug: square-connect-api
  description: Deletes an existing item and all item variations associated with it.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/items/{item_id}
  tags: Location,Items
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-id-delete-openapi.md
- name: Square Connect API Post Location Items Item Variations
  x-api-slug: square-connect-api
  description: Creates an item variation for an existing item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/items/{item_id}/variations
  tags: Location,Items,Variations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-idvariations-post-openapi.md
- name: Square Connect API Put Location Items Item Variations Variation
  x-api-slug: square-connect-api
  description: Modifies the details of an existing item variation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/items/{item_id}/variations/{variation_id}
  tags: Location,Items,Variations,Variation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-idvariationsvariation-id-put-openapi.md
- name: Square Connect API Delete Location Items Item Variations Variation
  x-api-slug: square-connect-api
  description: Deletes an existing item variation from an item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/items/{item_id}/variations/{variation_id}
  tags: Location,Items,Variations,Variation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-idvariationsvariation-id-delete-openapi.md
- name: Square Connect API Get Location Inventory
  x-api-slug: square-connect-api
  description: Provides inventory information for all of a merchant's inventory-enabled
    item variations.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/inventory
  tags: Location,Inventory
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idinventory-get-openapi.md
- name: Square Connect API Post Location Inventory Variation
  x-api-slug: square-connect-api
  description: Adjusts an item variation's current available inventory.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/inventory/{variation_id}
  tags: Location,Inventory,Variation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idinventoryvariation-id-post-openapi.md
- name: Square Connect API Post Location Modifier Lists
  x-api-slug: square-connect-api
  description: Creates an item modifier list and at least one modifier option for
    it.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/modifier-lists
  tags: Location,Modifier-lists
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idmodifierlists-post-openapi.md
- name: Square Connect API Get Location Modifier Lists
  x-api-slug: square-connect-api
  description: Lists all of a location's modifier lists.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/modifier-lists
  tags: Location,Modifier-lists
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idmodifierlists-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idmodifierlists-get-openapi.md
- name: Square Connect API Get Location Modifier Lists Modifier List
  x-api-slug: square-connect-api
  description: Provides the details for a single modifier list.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/modifier-lists/{modifier_list_id}
  tags: Location,Modifier-lists,Modifier,List
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idmodifierlistsmodifier-list-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idmodifierlistsmodifier-list-id-get-openapi.md
- name: Square Connect API Put Location Modifier Lists Modifier List
  x-api-slug: square-connect-api
  description: Modifies the details of an existing item modifier list.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/modifier-lists/{modifier_list_id}
  tags: Location,Modifier-lists,Modifier,List
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idmodifierlistsmodifier-list-id-put-openapi.md
- name: Square Connect API Delete Location Modifier Lists Modifier List
  x-api-slug: square-connect-api
  description: Deletes an existing item modifier list and all modifier options associated
    with it.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/modifier-lists/{modifier_list_id}
  tags: Location,Modifier-lists,Modifier,List
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idmodifierlistsmodifier-list-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idmodifierlistsmodifier-list-id-delete-openapi.md
- name: Square Connect API Put Location Items Item Modifier Lists Modifier List
  x-api-slug: square-connect-api
  description: Associates a modifier list with an item, meaning modifier options from
    the list can be applied to the item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/items/{item_id}/modifier-lists/{modifier_list_id}
  tags: Location,Items,Modifier-lists,Modifier,List
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-idmodifierlistsmodifier-list-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-idmodifierlistsmodifier-list-id-put-openapi.md
- name: Square Connect API Delete Location Items Item Modifier Lists Modifier List
  x-api-slug: square-connect-api
  description: Removes a modifier list association from an item, meaning modifier
    options from the list can no longer be applied to the item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/items/{item_id}/modifier-lists/{modifier_list_id}
  tags: Location,Items,Modifier-lists,Modifier,List
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-idmodifierlistsmodifier-list-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-idmodifierlistsmodifier-list-id-delete-openapi.md
- name: Square Connect API Post Location Modifier Lists Modifier List Modifier Options
  x-api-slug: square-connect-api
  description: Creates an item modifier option and adds it to a modifier list.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/modifier-lists/{modifier_list_id}/modifier-options
  tags: Location,Modifier-lists,Modifier,List,Modifier-options
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idmodifierlistsmodifier-list-idmodifieroptions-post-openapi.md
- name: Square Connect API Put Location Modifier Lists Modifier List Modifier Options
    Modifier Option
  x-api-slug: square-connect-api
  description: Put location modifier lists modifier list modifier options modifier
    option.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/modifier-lists/{modifier_list_id}/modifier-options/{modifier_option_id}
  tags: Location,Modifier-lists,Modifier,List,Modifier-options,Modifier,Option
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idmodifierlistsmodifier-list-idmodifieroptionsmodifier-option-id-put-openapi.md
- name: Square Connect API Delete Location Modifier Lists Modifier List Modifier Options
    Modifier Option
  x-api-slug: square-connect-api
  description: Delete location modifier lists modifier list modifier options modifier
    option.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/modifier-lists/{modifier_list_id}/modifier-options/{modifier_option_id}
  tags: Location,Modifier-lists,Modifier,List,Modifier-options,Modifier,Option
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idmodifierlistsmodifier-list-idmodifieroptionsmodifier-option-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idmodifierlistsmodifier-list-idmodifieroptionsmodifier-option-id-delete-openapi.md
- name: Square Connect API Post Location Categories
  x-api-slug: square-connect-api
  description: Creates an item category.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/categories
  tags: Location,Categories
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idcategories-post-openapi.md
- name: Square Connect API Get Location Categories
  x-api-slug: square-connect-api
  description: Lists all of a location's item categories.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/categories
  tags: Location,Categories
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idcategories-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idcategories-get-openapi.md
- name: Square Connect API Put Location Categories Category
  x-api-slug: square-connect-api
  description: Modifies the details of an existing item category.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/categories/{category_id}
  tags: Location,Categories,Category
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idcategoriescategory-id-put-openapi.md
- name: Square Connect API Delete Location Categories Category
  x-api-slug: square-connect-api
  description: Delete location categories category.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/categories/{category_id}
  tags: Location,Categories,Category
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idcategoriescategory-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idcategoriescategory-id-delete-openapi.md
- name: Square Connect API Post Location Discounts
  x-api-slug: square-connect-api
  description: Post location discounts.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/discounts
  tags: Location,Discounts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iddiscounts-post-openapi.md
- name: Square Connect API Get Location Discounts
  x-api-slug: square-connect-api
  description: Lists all of a location's discounts.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/discounts
  tags: Location,Discounts
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iddiscounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iddiscounts-get-openapi.md
- name: Square Connect API Put Location Discounts Discount
  x-api-slug: square-connect-api
  description: Modifies the details of an existing discount.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/discounts/{discount_id}
  tags: Location,Discounts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iddiscountsdiscount-id-put-openapi.md
- name: Square Connect API Delete Location Discounts Discount
  x-api-slug: square-connect-api
  description: Delete location discounts discount.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/discounts/{discount_id}
  tags: Location,Discounts
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iddiscountsdiscount-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iddiscountsdiscount-id-delete-openapi.md
- name: Square Connect API Post Location Fees
  x-api-slug: square-connect-api
  description: Creates a fee (tax).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/fees
  tags: Location,Fees
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idfees-post-openapi.md
- name: Square Connect API Get Location Fees
  x-api-slug: square-connect-api
  description: Lists all of a location's fees (taxes).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/fees
  tags: Location,Fees
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idfees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idfees-get-openapi.md
- name: Square Connect API Put Location Fees Fee
  x-api-slug: square-connect-api
  description: Modifies the details of an existing fee (tax).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/fees/{fee_id}
  tags: Location,Fees,Fee
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idfeesfee-id-put-openapi.md
- name: Square Connect API Delete Location Fees Fee
  x-api-slug: square-connect-api
  description: Deletes an existing fee (tax).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/fees/{fee_id}
  tags: Location,Fees,Fee
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idfeesfee-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idfeesfee-id-delete-openapi.md
- name: Square Connect API Put Location Items Item Fees Fee
  x-api-slug: square-connect-api
  description: Associates a fee with an item, meaning the fee is automatically applied
    to the item in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/items/{item_id}/fees/{fee_id}
  tags: Location,Items,Fees,Fee
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-idfeesfee-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-idfeesfee-id-put-openapi.md
- name: Square Connect API Delete Location Items Item Fees Fee
  x-api-slug: square-connect-api
  description: Removes a fee assocation from an item, meaning the fee is no longer
    automatically applied to the item in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/items/{item_id}/fees/{fee_id}
  tags: Location,Items,Fees,Fee
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-idfeesfee-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-iditemsitem-idfeesfee-id-delete-openapi.md
- name: Square Connect API Post Location Pages
  x-api-slug: square-connect-api
  description: Creates a Favorites page in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/pages
  tags: Location,Pages
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpages-post-openapi.md
- name: Square Connect API Get Location Pages
  x-api-slug: square-connect-api
  description: Lists all of a location's Favorites pages in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/pages
  tags: Location,Pages
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpages-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpages-get-openapi.md
- name: Square Connect API Put Location Pages Page
  x-api-slug: square-connect-api
  description: Modifies the details of a Favorites page in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/pages/{page_id}
  tags: Location,Pages,Page
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpagespage-id-put-openapi.md
- name: Square Connect API Delete Location Pages Page
  x-api-slug: square-connect-api
  description: Deletes an existing Favorites page and all of its cells.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/pages/{page_id}
  tags: Location,Pages,Page
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpagespage-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpagespage-id-delete-openapi.md
- name: Square Connect API Put Location Pages Page Cells
  x-api-slug: square-connect-api
  description: Modifies a cell of a Favorites page in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/pages/{page_id}/cells
  tags: Location,Pages,Page,Cells
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpagespage-idcells-put-openapi.md
- name: Square Connect API Delete Location Pages Page Cells
  x-api-slug: square-connect-api
  description: Deletes a cell from a Favorites page in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1///{location_id}/pages/{page_id}/cells
  tags: Location,Pages,Page,Cells
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpagespage-idcells-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/location-idpagespage-idcells-delete-openapi.md
- name: Square Connect API
  x-api-slug: square-connect-api
  description: Starting with a free credit card reader for the iPhone, iPad, and Android
    devices, Square Reader allows anyone to accept credit cards anywhere, anytime,
    for a low transaction rate of 2.75 percent per swipe, with no hidden fees. Square
    Register serves as a full point-of-sale system for businesses to accept payments,
    manage items, and share menu and location information. Square Wallet, available
    in the US, is the most seamless way to pay, enabling individuals to pay at their
    favorite local businesses, discover new ones nearby, explore menu listings, and
    store receipts.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/square-logo.png
  humanURL: https://squareup.com
  baseURL: https://connect.squareup.com/v1/
  tags: Square
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/openapi.md
x-common:
- type: x-base
  url: https://connect.squareup.com
- type: x-crunchbase
  url: http://www.crunchbase.com/company/square
- type: x-developer
  url: https://connect.squareup.com/
- type: x-github
  url: https://github.com/square
- type: x-twitter
  url: https://twitter.com/Square
- type: x-website
  url: https://squareup.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---