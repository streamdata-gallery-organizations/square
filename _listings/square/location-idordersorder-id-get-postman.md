{
  "info": {
    "name": "Square Connect API Get Location Orders Order",
    "_postman_id": "557a6af7-6086-4b13-b285-febe7946d4c3",
    "description": "Provides comprehensive information for a single online store order, including the order's history.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "77c7d79f-8997-4382-bcca-49bd235ddf1f",
          "name": "getLocationOrdersOrder",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/orders/:order_id"
              ],
              "variable": [
                {
                  "id": "location_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "order_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Provides comprehensive information for a single online store order, including the order's history"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e6fb38d9-f509-4bdd-a254-042ebbeae12b"
            }
          ]
        }
      ]
    }
  ]
}