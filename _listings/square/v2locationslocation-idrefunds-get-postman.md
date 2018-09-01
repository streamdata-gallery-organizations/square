{
  "info": {
    "name": "Square Connect API Get V2 Locations Location Refunds",
    "_postman_id": "3e3840cc-120d-40eb-b8ee-c3b96612c65a",
    "description": "Lists refunds for one of a business's locations.\n\nIn addition to full or partial tender refunds processed through Square APIs,\nrefunds may result from itemized returns or exchanges through Square's\nPoint of Sale applications.\n\nRefunds with a `status` of `PENDING` are not currently included in this\nendpoint's response.\n\nMax results per [page](#paginatingresults): 50",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "locations",
      "item": [
        {
          "id": "e9b6a18b-848d-4223-9ac4-259fc50b07ee",
          "name": "getV2LocationsLocationRefunds",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                "v2/locations/:location_id/refunds"
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
            "description": "Lists refunds for one of a business's locations"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2aab1c81-730d-47ce-bb15-2c229ee647e5"
            }
          ]
        }
      ]
    }
  ]
}