{
  "info": {
    "name": "Square Connect API Lists all of a location's discounts.",
    "_postman_id": "6b15aa25-debb-4399-968f-b0eb63e775e4",
    "description": "Lists all of a location's discounts.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Provides",
      "item": [
        {
          "id": "4cd236ac-40ac-439e-ab6e-6701cf050881",
          "name": "ListBankAccounts",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1/:location_id/bank-accounts"
              ],
              "variable": [
                {
                  "id": "location_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Provides non-confidential details for all of a location's associated bank accounts. This endpoint does not provide full bank account numbers, and there is no way to obtain a full bank account number with the Connect API."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "998df8dd-7ac8-4f4b-ad18-23befea2e420"
            }
          ]
        },
        {
          "id": "2e069a7b-270d-4767-81e1-9299b4c29ae5",
          "name": "RetrieveBankAccount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1/:location_id/bank-accounts/:bank_account_id"
              ],
              "variable": [
                {
                  "id": "bank_account_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "location_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Provides non-confidential details for a merchant's associated bank account. This endpoint does not provide full bank account numbers, and there is no way to obtain a full bank account number with the Connect API."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4261fa9b-009f-4894-9a53-816ad6dc42bc"
            }
          ]
        }
      ]
    },
    {
      "name": "Lists",
      "item": [
        {
          "id": "533ef14b-3e9e-4436-b6c7-752b9813f2df",
          "name": "ListDiscounts",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1/:location_id/discounts"
              ],
              "variable": [
                {
                  "id": "location_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all of a location's discounts."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4af11697-caa1-4382-8ee0-b8f29f762541"
            }
          ]
        }
      ]
    }
  ]
}