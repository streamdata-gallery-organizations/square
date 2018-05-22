{
  "info": {
    "name": "Square Connect API Get V2 Locations Location Transactions",
    "_postman_id": "72f7c001-86a4-43b7-9335-c78bf9117a54",
    "description": "Lists transactions for a particular location.\n\nTransactions include payment information from sales and exchanges and refund\ninformation from returns and exchanges.\n\nMax results per [page](#paginatingresults): 50",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "locations",
      "item": [
        {
          "id": "25585dc5-b773-47f2-85d8-73aa985176a4",
          "name": "getV2LocationsLocationTransactions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                "v2/locations/:location_id/transactions"
              ],
              "query": [
                {
                  "key": "begin_time",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "cursor",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "end_time",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort_order",
                  "value": "%7B%7D",
                  "disabled": false
                }
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
            "description": "Lists transactions for a particular location"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dba4dde7-7885-4366-929a-5652e929f0ad"
            }
          ]
        }
      ]
    }
  ]
}