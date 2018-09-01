{
  "info": {
    "name": "Square Connect API Get V2 Locations Location Transactions Transaction",
    "_postman_id": "d943bdf9-79fb-44f6-a2eb-2970ee3cc7eb",
    "description": "Get v2 locations location transactions transaction.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "locations",
      "item": [
        {
          "id": "c0f22bb2-958f-4156-855a-af621e6ad930",
          "name": "getV2LocationsLocationTransactionsTransaction",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                "v2/locations/:location_id/transactions/:transaction_id"
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get v2 locations location transactions transaction"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "79c3af1e-5009-4d65-9e19-bf5c3db30780"
            }
          ]
        }
      ]
    }
  ]
}