---
name: Square
x-slug: square
description: Square helps millions of sellers run their business- from secure credit
  card processing to point of sale solutions. Get paid faster with Square and sign
  up today!
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
x-kinRank: "9"
x-alexaRank: "2433"
tags: Square
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/apis.md
specificationVersion: "0.14"
apis:
- name: Square Connect API Get a business's information.
  x-api-slug: square-connect-api
  description: Get a business's information.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me
  tags: Businesss,Information
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1me-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1me-get-openapi.md
- name: Square Connect API Provides summary information for all of a business's employees.
  x-api-slug: square-connect-api
  description: Provides summary information for all of a business's employees.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/employees
  tags: Provides,Summary,Information,Of,Businesss,Employees
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1meemployees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1meemployees-get-openapi.md
- name: Square Connect API Creates an employee for a business.
  x-api-slug: square-connect-api
  description: Creates an employee for a business.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/employees
  tags: Creates,Employeea,Business
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1meemployees-post-openapi.md
- name: Square Connect API Provides the details for a single employee.
  x-api-slug: square-connect-api
  description: Provides the details for a single employee.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/employees/{employee_id}
  tags: Provides,Detailsa,Single,Employee
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1meemployeesemployee-id-get-openapi.md
- name: Square Connect API Update Employee
  x-api-slug: square-connect-api
  description: Update Employee
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/employees/{employee_id}
  tags: Employee
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1meemployeesemployee-id-put-openapi.md
- name: Square Connect API Provides details for a business's locations, including
    their IDs.
  x-api-slug: square-connect-api
  description: Provides details for a business's locations, including their IDs.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/locations
  tags: Provides,Detailsa,Businesss,Locations,,Including,Their,IDs
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1melocations-get-openapi.md
- name: Square Connect API Provides summary information for all of a business's employee
    roles.
  x-api-slug: square-connect-api
  description: Provides summary information for all of a business's employee roles.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/roles
  tags: Provides,Summary,Information,Of,Businesss,Employee,Roles
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1meroles-get-openapi.md
- name: Square Connect API Creates an employee role you can then assign to employees.
  x-api-slug: square-connect-api
  description: Creates an employee role you can then assign to employees.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/roles
  tags: Creates,Employee,Role,You,Can,Then,Assign,To,Employees
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1meroles-post-openapi.md
- name: Square Connect API Provides the details for a single employee role.
  x-api-slug: square-connect-api
  description: Provides the details for a single employee role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/roles/{role_id}
  tags: Provides,Detailsa,Single,Employee,Role
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1merolesrole-id-get-openapi.md
- name: Square Connect API Modifies the details of an employee role.
  x-api-slug: square-connect-api
  description: Modifies the details of an employee role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/roles/{role_id}
  tags: Modifies,Details,Of,Employee,Role
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1merolesrole-id-put-openapi.md
- name: Square Connect API Provides summary information for all of a business's employee
    timecards.
  x-api-slug: square-connect-api
  description: Provides summary information for all of a business's employee timecards.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/timecards
  tags: Provides,Summary,Information,Of,Businesss,Employee,Timecards
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1metimecards-get-openapi.md
- name: Square Connect API Creates a timecard for an employee. Each timecard corresponds
    to a single shift.
  x-api-slug: square-connect-api
  description: Creates a timecard for an employee. Each timecard corresponds to a
    single shift.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/timecards
  tags: Creates,Timecardan,Employee,,Each,Timecard,Corresponds,To,Single,Shift
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1metimecards-post-openapi.md
- name: Square Connect API Deletes a timecard. Deleted timecards are still accessible
    from Connect API endpoints, but the value of their deleted field is set to true.
    See Handling deleted timecards for more information.
  x-api-slug: square-connect-api
  description: Deletes a timecard. Deleted timecards are still accessible from Connect
    API endpoints, but the value of their deleted field is set to true. See Handling
    deleted timecards for more information.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/timecards/{timecard_id}
  tags: S,Timecard,,D,Timecards,Are,Still,Accessible,From,Connect,Endpoints,,But,Value,Of,Their,Deleted,Field,Is,Set,To,True,,See,Handling,Deleted,Timecardsmore,Information
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1metimecardstimecard-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1metimecardstimecard-id-delete-openapi.md
- name: Square Connect API Provides the details for a single timecard.
  x-api-slug: square-connect-api
  description: Provides the details for a single timecard.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/timecards/{timecard_id}
  tags: Provides,Detailsa,Single,Timecard
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1metimecardstimecard-id-get-openapi.md
- name: Square Connect API Modifies a timecard's details. This creates an API_EDIT
    event for the timecard. You can view a timecard's event history with the List
    Timecard Events endpoint.
  x-api-slug: square-connect-api
  description: Modifies a timecard's details. This creates an API_EDIT event for the
    timecard. You can view a timecard's event history with the List Timecard Events
    endpoint.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/timecards/{timecard_id}
  tags: Modifies,Timecards,Details,,This,Creates,EDIT,Eventthe,Timecard,,You,Can,View,Timecards,Event,History,List,Timecard,Events,Endpoint
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1metimecardstimecard-id-put-openapi.md
- name: Square Connect API Provides summary information for all events associated
    with a particular timecard.
  x-api-slug: square-connect-api
  description: Provides summary information for all events associated with a particular
    timecard.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/me/timecards/{timecard_id}/events
  tags: Provides,Summary,Information,Events,Associated,Particular,Timecard
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1metimecardstimecard-idevents-get-openapi.md
- name: Square Connect API Provides non-confidential details for all of a location's
    associated bank accounts. This endpoint does not provide full bank account numbers,
    and there is no way to obtain a full bank account number with the Connect API.
  x-api-slug: square-connect-api
  description: Provides non-confidential details for all of a location's associated
    bank accounts. This endpoint does not provide full bank account numbers, and there
    is no way to obtain a full bank account number with the Connect API.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/bank-accounts
  tags: Provides,Non-confidential,Details,Of,Locations,Associated,Bank,Accounts,,This,Endpoint,Does,Not,Provide,Full,Bank,Account,Numbers,,There,Is,No,Way,To,Obtain,Full,Bank,Account,Number,Connect
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idbankaccounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idbankaccounts-get-openapi.md
- name: Square Connect API Provides non-confidential details for a merchant's associated
    bank account. This endpoint does not provide full bank account numbers, and there
    is no way to obtain a full bank account number with the Connect API.
  x-api-slug: square-connect-api
  description: Provides non-confidential details for a merchant's associated bank
    account. This endpoint does not provide full bank account numbers, and there is
    no way to obtain a full bank account number with the Connect API.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/bank-accounts/{bank_account_id}
  tags: Provides,Non-confidential,Detailsa,Merchants,Associated,Bank,Account,,This,Endpoint,Does,Not,Provide,Full,Bank,Account,Numbers,,There,Is,No,Way,To,Obtain,Full,Bank,Account,Number,Connect
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idbankaccountsbank-account-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idbankaccountsbank-account-id-get-openapi.md
- name: Square Connect API Provides the details for all of a location's cash drawer
    shifts during a date range. The date range you specify cannot exceed 90 days.
  x-api-slug: square-connect-api
  description: Provides the details for all of a location's cash drawer shifts during
    a date range. The date range you specify cannot exceed 90 days.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/cash-drawer-shifts
  tags: Provides,Details,Of,Locations,Cash,Drawer,Shifts,During,Date,Range,,Date,Range,You,Specify,Cannot,Exceed,90,Days
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idcashdrawershifts-get-openapi.md
- name: Square Connect API Provides the details for a single cash drawer shift, including
    all events that occurred during the shift.
  x-api-slug: square-connect-api
  description: Provides the details for a single cash drawer shift, including all
    events that occurred during the shift.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/cash-drawer-shifts/{shift_id}
  tags: Provides,Detailsa,Single,Cash,Drawer,Shift,,Including,,Events,That,Occurred,During,Shift
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idcashdrawershiftsshift-id-get-openapi.md
- name: Square Connect API Lists all of a location's item categories.
  x-api-slug: square-connect-api
  description: Lists all of a location's item categories.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/categories
  tags: Lists,,Of,Locations,Item,Categories
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idcategories-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idcategories-get-openapi.md
- name: Square Connect API Creates an item category.
  x-api-slug: square-connect-api
  description: Creates an item category.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/categories
  tags: Creates,Item,Category
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idcategories-post-openapi.md
- name: Square Connect API Deletes an existing item category.
  x-api-slug: square-connect-api
  description: Deletes an existing item category.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/categories/{category_id}
  tags: S,Existing,Item,Category
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idcategoriescategory-id-delete-openapi.md
- name: Square Connect API Modifies the details of an existing item category.
  x-api-slug: square-connect-api
  description: Modifies the details of an existing item category.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/categories/{category_id}
  tags: Modifies,Details,Of,Existing,Item,Category
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idcategoriescategory-id-put-openapi.md
- name: Square Connect API Lists all of a location's discounts.
  x-api-slug: square-connect-api
  description: Lists all of a location's discounts.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/discounts
  tags: Lists,,Of,Locations,Discounts
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iddiscounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iddiscounts-get-openapi.md
- name: Square Connect API Creates a discount.
  x-api-slug: square-connect-api
  description: Creates a discount.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/discounts
  tags: Creates,Discount
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iddiscounts-post-openapi.md
- name: Square Connect API Deletes an existing discount.
  x-api-slug: square-connect-api
  description: Deletes an existing discount.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/discounts/{discount_id}
  tags: S,Existing,Discount
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iddiscountsdiscount-id-delete-openapi.md
- name: Square Connect API Modifies the details of an existing discount.
  x-api-slug: square-connect-api
  description: Modifies the details of an existing discount.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/discounts/{discount_id}
  tags: Modifies,Details,Of,Existing,Discount
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iddiscountsdiscount-id-put-openapi.md
- name: Square Connect API Lists all of a location's fees (taxes).
  x-api-slug: square-connect-api
  description: Lists all of a location's fees (taxes).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/fees
  tags: Lists,,Of,Locations,Fees,(taxes)
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idfees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idfees-get-openapi.md
- name: Square Connect API Creates a fee (tax).
  x-api-slug: square-connect-api
  description: Creates a fee (tax).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/fees
  tags: Creates,Fee,(tax)
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idfees-post-openapi.md
- name: Square Connect API Deletes an existing fee (tax).
  x-api-slug: square-connect-api
  description: Deletes an existing fee (tax).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/fees/{fee_id}
  tags: S,Existing,Fee,(tax)
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idfeesfee-id-delete-openapi.md
- name: Square Connect API Modifies the details of an existing fee (tax).
  x-api-slug: square-connect-api
  description: Modifies the details of an existing fee (tax).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/fees/{fee_id}
  tags: Modifies,Details,Of,Existing,Fee,(tax)
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idfeesfee-id-put-openapi.md
- name: Square Connect API Provides inventory information for all of a merchant's
    inventory-enabled item variations.
  x-api-slug: square-connect-api
  description: Provides inventory information for all of a merchant's inventory-enabled
    item variations.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/inventory
  tags: Provides,Inventory,Information,Of,Merchants,Inventory-enabled,Item,Variations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idinventory-get-openapi.md
- name: Square Connect API Adjusts an item variation's current available inventory.
  x-api-slug: square-connect-api
  description: Adjusts an item variation's current available inventory.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/inventory/{variation_id}
  tags: Adjusts,Item,Variations,Current,Available,Inventory
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idinventoryvariation-id-post-openapi.md
- name: Square Connect API Provides summary information for all of a location's items.
  x-api-slug: square-connect-api
  description: Provides summary information for all of a location's items.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/items
  tags: Provides,Summary,Information,Of,Locations,Items
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditems-get-openapi.md
- name: Square Connect API Creates an item and at least one variation for it.
  x-api-slug: square-connect-api
  description: Creates an item and at least one variation for it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/items
  tags: Creates,Item,At,Least,Variationit
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditems-post-openapi.md
- name: Square Connect API Deletes an existing item and all item variations associated
    with it.
  x-api-slug: square-connect-api
  description: Deletes an existing item and all item variations associated with it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/items/{item_id}
  tags: S,Existing,Item,,Item,Variations,Associated,It
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditemsitem-id-delete-openapi.md
- name: Square Connect API Provides the details for a single item, including associated
    modifier lists and fees.
  x-api-slug: square-connect-api
  description: Provides the details for a single item, including associated modifier
    lists and fees.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/items/{item_id}
  tags: Provides,Detailsa,Single,Item,,Including,Associated,Modifier,Lists,Fees
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditemsitem-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditemsitem-id-get-openapi.md
- name: Square Connect API Modifies the core details of an existing item.
  x-api-slug: square-connect-api
  description: Modifies the core details of an existing item.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/items/{item_id}
  tags: Modifies,Core,Details,Of,Existing,Item
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditemsitem-id-put-openapi.md
- name: Square Connect API Removes a fee assocation from an item, meaning the fee
    is no longer automatically applied to the item in Square Register.
  x-api-slug: square-connect-api
  description: Removes a fee assocation from an item, meaning the fee is no longer
    automatically applied to the item in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/items/{item_id}/fees/{fee_id}
  tags: Removes,Fee,Assocation,From,Item,,Meaning,Fee,Is,No,Longer,Automatically,Applied,To,Item,In,Square,Register
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditemsitem-idfeesfee-id-delete-openapi.md
- name: Square Connect API Associates a fee with an item, meaning the fee is automatically
    applied to the item in Square Register.
  x-api-slug: square-connect-api
  description: Associates a fee with an item, meaning the fee is automatically applied
    to the item in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/items/{item_id}/fees/{fee_id}
  tags: Associates,Fee,Item,,Meaning,Fee,Is,Automatically,Applied,To,Item,In,Square,Register
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditemsitem-idfeesfee-id-put-openapi.md
- name: Square Connect API Removes a modifier list association from an item, meaning
    modifier options from the list can no longer be applied to the item.
  x-api-slug: square-connect-api
  description: Removes a modifier list association from an item, meaning modifier
    options from the list can no longer be applied to the item.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/items/{item_id}/modifier-lists/{modifier_list_id}
  tags: Removes,Modifier,List,Association,From,Item,,Meaning,Modifier,Options,From,List,Can,No,Longer,Be,Applied,To,Item
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditemsitem-idmodifierlistsmodifier-list-id-delete-openapi.md
- name: Square Connect API Associates a modifier list with an item, meaning modifier
    options from the list can be applied to the item.
  x-api-slug: square-connect-api
  description: Associates a modifier list with an item, meaning modifier options from
    the list can be applied to the item.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/items/{item_id}/modifier-lists/{modifier_list_id}
  tags: Associates,Modifier,List,Item,,Meaning,Modifier,Options,From,List,Can,Be,Applied,To,Item
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditemsitem-idmodifierlistsmodifier-list-id-put-openapi.md
- name: Square Connect API Creates an item variation for an existing item.
  x-api-slug: square-connect-api
  description: Creates an item variation for an existing item.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/items/{item_id}/variations
  tags: Creates,Item,Variationan,Existing,Item
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditemsitem-idvariations-post-openapi.md
- name: Square Connect API Deletes an existing item variation from an item.
  x-api-slug: square-connect-api
  description: Deletes an existing item variation from an item.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/items/{item_id}/variations/{variation_id}
  tags: S,Existing,Item,Variation,From,Item
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditemsitem-idvariationsvariation-id-delete-openapi.md
- name: Square Connect API Modifies the details of an existing item variation.
  x-api-slug: square-connect-api
  description: Modifies the details of an existing item variation.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/items/{item_id}/variations/{variation_id}
  tags: Modifies,Details,Of,Existing,Item,Variation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-iditemsitem-idvariationsvariation-id-put-openapi.md
- name: Square Connect API Lists all of a location's modifier lists.
  x-api-slug: square-connect-api
  description: Lists all of a location's modifier lists.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/modifier-lists
  tags: Lists,,Of,Locations,Modifier,Lists
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idmodifierlists-get-openapi.md
- name: Square Connect API Creates an item modifier list and at least one modifier
    option for it.
  x-api-slug: square-connect-api
  description: Creates an item modifier list and at least one modifier option for
    it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/modifier-lists
  tags: Creates,Item,Modifier,List,At,Least,Modifier,Optionit
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idmodifierlists-post-openapi.md
- name: Square Connect API Deletes an existing item modifier list and all modifier
    options associated with it.
  x-api-slug: square-connect-api
  description: Deletes an existing item modifier list and all modifier options associated
    with it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/modifier-lists/{modifier_list_id}
  tags: S,Existing,Item,Modifier,List,,Modifier,Options,Associated,It
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idmodifierlistsmodifier-list-id-delete-openapi.md
- name: Square Connect API Provides the details for a single modifier list.
  x-api-slug: square-connect-api
  description: Provides the details for a single modifier list.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/modifier-lists/{modifier_list_id}
  tags: Provides,Detailsa,Single,Modifier,List
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idmodifierlistsmodifier-list-id-get-openapi.md
- name: Square Connect API Modifies the details of an existing item modifier list.
  x-api-slug: square-connect-api
  description: Modifies the details of an existing item modifier list.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/modifier-lists/{modifier_list_id}
  tags: Modifies,Details,Of,Existing,Item,Modifier,List
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idmodifierlistsmodifier-list-id-put-openapi.md
- name: Square Connect API Creates an item modifier option and adds it to a modifier
    list.
  x-api-slug: square-connect-api
  description: Creates an item modifier option and adds it to a modifier list.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/modifier-lists/{modifier_list_id}/modifier-options
  tags: Creates,Item,Modifier,Option,Adds,It,To,Modifier,List
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idmodifierlistsmodifier-list-idmodifieroptions-post-openapi.md
- name: Square Connect API Deletes an existing item modifier option from a modifier
    list.
  x-api-slug: square-connect-api
  description: Deletes an existing item modifier option from a modifier list.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/modifier-lists/{modifier_list_id}/modifier-options/{modifier_option_id}
  tags: S,Existing,Item,Modifier,Option,From,Modifier,List
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idmodifierlistsmodifier-list-idmodifieroptionsmodifier-option-id-delete-openapi.md
- name: Square Connect API Modifies the details of an existing item modifier option.
  x-api-slug: square-connect-api
  description: Modifies the details of an existing item modifier option.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/modifier-lists/{modifier_list_id}/modifier-options/{modifier_option_id}
  tags: Modifies,Details,Of,Existing,Item,Modifier,Option
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idmodifierlistsmodifier-list-idmodifieroptionsmodifier-option-id-put-openapi.md
- name: Square Connect API Provides summary information for a merchant's online store
    orders.
  x-api-slug: square-connect-api
  description: Provides summary information for a merchant's online store orders.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/orders
  tags: Provides,Summary,Informationa,Merchants,Online,Store,Orders
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idorders-get-openapi.md
- name: Square Connect API Provides comprehensive information for a single online
    store order, including the order's history.
  x-api-slug: square-connect-api
  description: Provides comprehensive information for a single online store order,
    including the order's history.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/orders/{order_id}
  tags: Provides,Comprehensive,Informationa,Single,Online,Store,Order,,Including,Orders,History
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idordersorder-id-get-openapi.md
- name: 'Square Connect API Updates the details of an online store order. Every update
    you perform on an order corresponds to one of three actions:'
  x-api-slug: square-connect-api
  description: 'Updates the details of an online store order. Every update you perform
    on an order corresponds to one of three actions:'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/orders/{order_id}
  tags: 'S,Details,Of,Online,Store,Order,,Every,Update,You,Perform,On,Order,Corresponds,To,Of,Three,Actions:'
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idordersorder-id-put-openapi.md
- name: Square Connect API Lists all of a location's Favorites pages in Square Register.
  x-api-slug: square-connect-api
  description: Lists all of a location's Favorites pages in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/pages
  tags: Lists,,Of,Locations,Favorites,Pages,In,Square,Register
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idpages-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idpages-get-openapi.md
- name: Square Connect API Creates a Favorites page in Square Register.
  x-api-slug: square-connect-api
  description: Creates a Favorites page in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/pages
  tags: Creates,Favorites,Page,In,Square,Register
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idpages-post-openapi.md
- name: Square Connect API Deletes an existing Favorites page and all of its cells.
  x-api-slug: square-connect-api
  description: Deletes an existing Favorites page and all of its cells.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/pages/{page_id}
  tags: S,Existing,Favorites,Page,,Of,Its,Cells
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idpagespage-id-delete-openapi.md
- name: Square Connect API Modifies the details of a Favorites page in Square Register.
  x-api-slug: square-connect-api
  description: Modifies the details of a Favorites page in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/pages/{page_id}
  tags: Modifies,Details,Of,Favorites,Page,In,Square,Register
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idpagespage-id-put-openapi.md
- name: Square Connect API Deletes a cell from a Favorites page in Square Register.
  x-api-slug: square-connect-api
  description: Deletes a cell from a Favorites page in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/pages/{page_id}/cells
  tags: S,Cell,From,Favorites,Page,In,Square,Register
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idpagespage-idcells-delete-openapi.md
- name: Square Connect API Modifies a cell of a Favorites page in Square Register.
  x-api-slug: square-connect-api
  description: Modifies a cell of a Favorites page in Square Register.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/pages/{page_id}/cells
  tags: Modifies,Cell,Of,Favorites,Page,In,Square,Register
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idpagespage-idcells-put-openapi.md
- name: Square Connect API Provides summary information for all payments taken by
    a merchant or any of the merchant's mobile staff during a date range. Date ranges
    cannot exceed one year in length. See Date ranges for details of inclusive and
    exclusive dates.
  x-api-slug: square-connect-api
  description: Provides summary information for all payments taken by a merchant or
    any of the merchant's mobile staff during a date range. Date ranges cannot exceed
    one year in length. See Date ranges for details of inclusive and exclusive dates.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/payments
  tags: Provides,Summary,Information,Payments,Taken,By,Merchant,Any,Of,Merchants,Mobile,Staff,During,Date,Range,,Date,Ranges,Cannot,Exceed,Year,In,Length,,See,Date,Rangesdetails,Of,Inclusive,Exclusive,Dates
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idpayments-get-openapi.md
- name: Square Connect API Provides comprehensive information for a single payment.
  x-api-slug: square-connect-api
  description: Provides comprehensive information for a single payment.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/payments/{payment_id}
  tags: Provides,Comprehensive,Informationa,Single,Payment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idpaymentspayment-id-get-openapi.md
- name: Square Connect API Provides the details for all refunds initiated by a merchant
    or any of the merchant's mobile staff during a date range. Date ranges cannot
    exceed one year in length.
  x-api-slug: square-connect-api
  description: Provides the details for all refunds initiated by a merchant or any
    of the merchant's mobile staff during a date range. Date ranges cannot exceed
    one year in length.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/refunds
  tags: Provides,Details,Refunds,Initiated,By,Merchant,Any,Of,Merchants,Mobile,Staff,During,Date,Range,,Date,Ranges,Cannot,Exceed,Year,In,Length
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idrefunds-get-openapi.md
- name: Square Connect API Issues a refund for a previously processed payment. You
    must issue a refund within 60 days of the associated payment.
  x-api-slug: square-connect-api
  description: Issues a refund for a previously processed payment. You must issue
    a refund within 60 days of the associated payment.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/refunds
  tags: Issues,Refunda,Previously,Processed,Payment,,You,Must,Issue,Refund,Within,60,Days,Of,Associated,Payment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idrefunds-post-openapi.md
- name: Square Connect API Provides summary information for all deposits and withdrawals
    initiated by Square to a merchant's bank account during a date range. Date ranges
    cannot exceed one year in length.
  x-api-slug: square-connect-api
  description: Provides summary information for all deposits and withdrawals initiated
    by Square to a merchant's bank account during a date range. Date ranges cannot
    exceed one year in length.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/settlements
  tags: Provides,Summary,Information,Deposits,Withdrawals,Initiated,By,Square,To,Merchants,Bank,Account,During,Date,Range,,Date,Ranges,Cannot,Exceed,Year,In,Length
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idsettlements-get-openapi.md
- name: Square Connect API Provides comprehensive information for a single settlement,
    including the entries that contribute to the settlement's total.
  x-api-slug: square-connect-api
  description: Provides comprehensive information for a single settlement, including
    the entries that contribute to the settlement's total.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v1/{location_id}/settlements/{settlement_id}
  tags: Provides,Comprehensive,Informationa,Single,Settlement,,Including,Entries,That,Contribute,To,Settlements,Total
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v1location-idsettlementssettlement-id-get-openapi.md
- name: Square Connect API BatchDeleteCatalogObjects
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/catalog/batch-delete
  tags: BatchCatalogObjects
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogbatchdelete-post-openapi.md
- name: Square Connect API BatchRetrieveCatalogObjects
  x-api-slug: square-connect-api
  description: |-
    Returns a set of objects based on the provided ID.
    Each [CatalogItem](#type-catalogitem) returned in the set includes all of its
    child information including: all of its
    [CatalogItemVariation](#type-catalogitemvariation) objects, references to
    its [CatalogModifierList](#type-catalogmodifierlist) objects, and the ids of
    any [CatalogTax](#type-catalogtax) objects that apply to it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/catalog/batch-retrieve
  tags: BatchRetrieveCatalogObjects
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogbatchretrieve-post-openapi.md
- name: Square Connect API BatchUpsertCatalogObjects
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/catalog/batch-upsert
  tags: BatchUpsertCatalogObjects
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogbatchupsert-post-openapi.md
- name: Square Connect API CatalogInfo
  x-api-slug: square-connect-api
  description: |-
    Returns information about the Square Catalog API, such as batch size
    limits for `BatchUpsertCatalogObjects`.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/catalog/info
  tags: CatalogInfo
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2cataloginfo-get-openapi.md
- name: Square Connect API ListCatalog
  x-api-slug: square-connect-api
  description: |-
    Returns a list of [CatalogObject](#type-catalogobject)s that includes
    all objects of a set of desired types (for example, all [CatalogItem](#type-catalogitem)
    and [CatalogTax](#type-catalogtax) objects) in the catalog. The types parameter
    is specified as a comma-separated list of valid [CatalogObject](#type-catalogobject) types:
    `ITEM`, `ITEM_VARIATION`, `MODIFIER`, `MODIFIER_LIST`, `CATEGORY`, `DISCOUNT`, `TAX`.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/catalog/list
  tags: ListCatalog
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2cataloglist-get-openapi.md
- name: Square Connect API UpsertCatalogObject
  x-api-slug: square-connect-api
  description: Creates or updates the target [CatalogObject](#type-catalogobject).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/catalog/object
  tags: UpsertCatalogObject
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogobject-post-openapi.md
- name: Square Connect API DeleteCatalogObject
  x-api-slug: square-connect-api
  description: |-
    Deletes a single [CatalogObject](#type-catalogobject) based on the
    provided ID and returns the set of successfully deleted IDs in the response.
    Deletion is a cascading event such that all children of the targeted object
    are also deleted. For example, deleting a [CatalogItem](#type-catalogitem)
    will also delete all of its
    [CatalogItemVariation](#type-catalogitemvariation) children.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/catalog/object/{object_id}
  tags: CatalogObject
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogobjectobject-id-delete-openapi.md
- name: Square Connect API RetrieveCatalogObject
  x-api-slug: square-connect-api
  description: |-
    Returns a single [CatalogItem](#type-catalogitem) as a
    [CatalogObject](#type-catalogobject) based on the provided ID. The returned
    object includes all of the relevant [CatalogItem](#type-catalogitem)
    information including: [CatalogItemVariation](#type-catalogitemvariation)
    children, references to its
    [CatalogModifierList](#type-catalogmodifierlist) objects, and the ids of
    any [CatalogTax](#type-catalogtax) objects that apply to it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/catalog/object/{object_id}
  tags: RetrieveCatalogObject
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogobjectobject-id-get-openapi.md
- name: Square Connect API SearchCatalogObjects
  x-api-slug: square-connect-api
  description: |-
    Queries the targeted catalog using a variety of query types
    ([CatalogQuerySortedAttribute](#type-catalogquerysortedattribute),
    ([CatalogQueryExact](#type-catalogqueryexact),
    ([CatalogQueryRange](#type-catalogqueryrange),
    ([CatalogQueryText](#type-catalogquerytext),
    ([CatalogQueryItemsForTax](#type-catalogqueryitemsfortax),
    ([CatalogQueryItemsForModifierList](#type-catalogqueryitemsformodifierlist)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/catalog/search
  tags: SearchCatalogObjects
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogsearch-post-openapi.md
- name: Square Connect API UpdateItemModifierLists
  x-api-slug: square-connect-api
  description: |-
    Updates the [CatalogModifierList](#type-catalogmodifierlist) objects
    that apply to the targeted [CatalogItem](#type-catalogitem) without having
    to perform an upsert on the entire item.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/catalog/update-item-modifier-lists
  tags: ItemModifierLists
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogupdateitemmodifierlists-post-openapi.md
- name: Square Connect API UpdateItemTaxes
  x-api-slug: square-connect-api
  description: |-
    Updates the [CatalogTax](#type-catalogtax) objects that apply to the
    targeted [CatalogItem](#type-catalogitem) without having to perform an
    upsert on the entire item.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/catalog/update-item-taxes
  tags: ItemTaxes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2catalogupdateitemtaxes-post-openapi.md
- name: Square Connect API ListCustomers
  x-api-slug: square-connect-api
  description: Lists a business's customers.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/customers
  tags: ListCustomers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customers-get-openapi.md
- name: Square Connect API CreateCustomer
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/customers
  tags: CreateCustomer
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customers-post-openapi.md
- name: Square Connect API DeleteCustomer
  x-api-slug: square-connect-api
  description: Deletes a customer from a business, along with any linked cards on
    file.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/customers/{customer_id}
  tags: Customer
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-id-delete-openapi.md
- name: Square Connect API RetrieveCustomer
  x-api-slug: square-connect-api
  description: Returns details for a single customer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/customers/{customer_id}
  tags: RetrieveCustomer
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-id-get-openapi.md
- name: Square Connect API UpdateCustomer
  x-api-slug: square-connect-api
  description: |-
    Updates the details of an existing customer.
    The ID of the customer may change if the customer has been merged into another customer.

    You cannot edit a customer's cards on file with this endpoint. To make changes
    to a card on file, you must delete the existing card on file with the
    [DeleteCustomerCard](#endpoint-deletecustomercard) endpoint, then create a new one with the
    [CreateCustomerCard](#endpoint-createcustomercard) endpoint.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/customers/{customer_id}
  tags: Customer
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-id-put-openapi.md
- name: Square Connect API CreateCustomerCard
  x-api-slug: square-connect-api
  description: |-
    Adds a card on file to an existing customer. In the United States
    Square takes care of automatically updating any cards on file that might
    have expired since you first attached them to a customer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/customers/{customer_id}/cards
  tags: CreateCustomerCard
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-idcards-post-openapi.md
- name: Square Connect API DeleteCustomerCard
  x-api-slug: square-connect-api
  description: Removes a card on file from a customer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/customers/{customer_id}/cards/{card_id}
  tags: CustomerCard
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2customerscustomer-idcardscard-id-delete-openapi.md
- name: Square Connect API ListLocations
  x-api-slug: square-connect-api
  description: |-
    Provides the details for all of a business's locations.

    Most other Connect API endpoints have a required `location_id` path parameter.
    The `id` field of the [`Location`](#type-location) objects returned by this
    endpoint correspond to that `location_id` parameter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/locations
  tags: ListLocations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locations-get-openapi.md
- name: Square Connect API CreateCheckout
  x-api-slug: square-connect-api
  description: |-
    Creates a [Checkout](#type-checkout) response that links a
    `checkoutId` and `checkout_page_url` that customers can be directed to in
    order to provide their payment information using a payment processing
    workflow hosted on connect.squareup.com.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/locations/{location_id}/checkouts
  tags: CreateCheckout
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idcheckouts-post-openapi.md
- name: Square Connect API ListRefunds
  x-api-slug: square-connect-api
  description: |-
    Lists refunds for one of a business's locations.

    Refunds with a `status` of `PENDING` are not currently included in this
    endpoint's response.

    Max results per [page](#paginatingresults): 50
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/locations/{location_id}/refunds
  tags: ListRefunds
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idrefunds-get-openapi.md
- name: Square Connect API ListTransactions
  x-api-slug: square-connect-api
  description: |-
    Lists transactions for a particular location.

    Max results per [page](#paginatingresults): 50
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/locations/{location_id}/transactions
  tags: ListTransactions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactions-get-openapi.md
- name: Square Connect API Charge
  x-api-slug: square-connect-api
  description: |-
    Charges a card represented by a card nonce or a customer's card on file.

    Your request to this endpoint must include _either_:

    - A value for the `card_nonce` parameter (to charge a card nonce generated
    with the `SqPaymentForm`)
    - Values for the `customer_card_id` and `customer_id` parameters (to charge
    a customer's card on file)

    In order for an e-commerce payment to potentially qualify for
    [Square chargeback protection](https://squareup.com/help/article/5394), you
    _must_ provide values for the following parameters in your request:

    - `buyer_email_address`
    - At least one of `billing_address` or `shipping_address`

    When this response is returned, the amount of Square's processing fee might not yet be
    calculated. To obtain the processing fee, wait about ten seconds and call
    [RetrieveTransaction](#endpoint-retrievetransaction). See the `processing_fee_money`
    field of each [Tender included](#type-tender) in the transaction.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/locations/{location_id}/transactions
  tags: Charge
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactions-post-openapi.md
- name: Square Connect API RetrieveTransaction
  x-api-slug: square-connect-api
  description: Retrieves details for a single transaction.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/locations/{location_id}/transactions/{transaction_id}
  tags: RetrieveTransaction
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactionstransaction-id-get-openapi.md
- name: Square Connect API CaptureTransaction
  x-api-slug: square-connect-api
  description: |-
    Captures a transaction that was created with the [Charge](#endpoint-charge)
    endpoint with a `delay_capture` value of `true`.

    See [Delayed capture transactions](/articles/delayed-capture-transactions/)
    for more information.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/locations/{location_id}/transactions/{transaction_id}/capture
  tags: CaptureTransaction
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactionstransaction-idcapture-post-openapi.md
- name: Square Connect API CreateRefund
  x-api-slug: square-connect-api
  description: |-
    Initiates a refund for a previously charged tender.

    You must issue a refund within 120 days of the associated payment. See
    (this article)[https://squareup.com/help/us/en/article/5060] for more information
    on refund behavior.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/locations/{location_id}/transactions/{transaction_id}/refund
  tags: CreateRefund
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactionstransaction-idrefund-post-openapi.md
- name: Square Connect API VoidTransaction
  x-api-slug: square-connect-api
  description: |-
    Cancels a transaction that was created with the [Charge](#endpoint-charge)
    endpoint with a `delay_capture` value of `true`.

    See [Delayed capture transactions](/articles/delayed-capture-transactions/)
    for more information.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com////v2/locations/{location_id}/transactions/{transaction_id}/void
  tags: VoidTransaction
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/v2locationslocation-idtransactionstransaction-idvoid-post-openapi.md
- name: Square Connect API
  x-api-slug: square-connect-api
  description: Square helps millions of sellers run their business- from secure credit
    card processing to point of sale solutions. Get paid faster with Square and sign
    up today!
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2176-square.jpg
  humanURL: http://square.com
  baseURL: https://connect.squareup.com//
  tags: Square
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/square/master/_listings/square/openapi.md
x-common:
- type: x-website
  url: http://square.com
- type: x-base
  url: https://connect.squareup.com
- type: x-crunchbase
  url: http://www.crunchbase.com/company/square
- type: x-crunchbase
  url: https://crunchbase.com/organization/square
- type: x-developer
  url: https://connect.squareup.com/
- type: x-email
  url: press@squareup.com
- type: x-email
  url: security@squareup.com
- type: x-email
  url: lawenforcement@squareup.com
- type: x-email
  url: redemption@squareup.com
- type: x-email
  url: privacy@squareup.com
- type: x-email
  url: community@squareup.com
- type: x-email
  url: noreply@messaging.squareup.com
- type: x-email
  url: ir@squareup.com
- type: x-email
  url: takedowns@squareup.com
- type: x-github
  url: https://github.com/square
- type: x-linkedin
  url: https://www.linkedin.com/company/square--/
- type: x-twitter
  url: https://twitter.com/Square
- type: x-website
  url: http://squareup.com
- type: x-website
  url: https://squareup.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---