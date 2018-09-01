{
  "info": {
    "name": "Square Connect API Post V2 Locations Location Transactions Transaction Capture",
    "_postman_id": "9a829bd9-93fa-49e0-83d2-9db442559c00",
    "description": "Captures a transaction that was created with the [Charge](#endpoint-charge)\nendpoint with a `delay_capture` value of `true`.\n\nSee [Delayed capture transactions](/articles/delayed-capture-transactions/)\nfor more information.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "locations",
      "item": [
        {
          "id": "5edfe9cc-2291-4f51-b2a4-5fc0c2d90841",
          "name": "postV2LocationsLocationTransactionsTransactionCapture",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                "v2/locations/:location_id/transactions/:transaction_id/capture"
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
            "description": "Captures a transaction that was created with the [Charge](#endpoint-charge)\nendpoint with a `delay_capture` value of `true`"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "15103c08-4e2b-474b-bca4-3ae60da595e2"
            }
          ]
        }
      ]
    }
  ]
}