{
  "info": {
    "name": "Square Connect API Get Location Orders",
    "_postman_id": "2f51308f-5741-4b46-a109-91f4623c2d40",
    "description": "Provides summary information for a merchant's online store orders.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "10b80d28-041b-4cfc-902b-47651c8ed229",
          "name": "getLocationOrders",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/orders"
              ],
              "query": [
                {
                  "key": "batch_token",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "order",
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
            "description": "Provides summary information for a merchant's online store orders"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "41b9841c-b876-4061-9b97-375a578e1803"
            }
          ]
        }
      ]
    }
  ]
}