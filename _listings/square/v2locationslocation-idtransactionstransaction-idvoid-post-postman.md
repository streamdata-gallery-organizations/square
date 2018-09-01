{
  "info": {
    "name": "Square Connect API Post V2 Locations Location Transactions Transaction Vo",
    "_postman_id": "c2a0b51e-8074-4773-a2e0-dae12c25edd9",
    "description": "Cancels a transaction that was created with the [Charge](#endpoint-charge)\nendpoint with a `delay_capture` value of `true`.\n\nSee [Delayed capture transactions](/articles/delayed-capture-transactions/)\nfor more information.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "locations",
      "item": [
        {
          "id": "6f22cbad-89a1-4b16-a2c2-f918fdbfb59b",
          "name": "postV2LocationsLocationTransactionsTransactionVo",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                "v2/locations/:location_id/transactions/:transaction_id/void"
              ],
              "variable": [
                {
                  "id": "location_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "transaction_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Cancels a transaction that was created with the [Charge](#endpoint-charge)\nendpoint with a `delay_capture` value of `true`"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5f45eecb-a1d3-40ab-92df-9dd3a66f5a0f"
            }
          ]
        }
      ]
    }
  ]
}