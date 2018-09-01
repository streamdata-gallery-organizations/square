{
  "info": {
    "name": "Square Connect API Get Location Discounts",
    "_postman_id": "59d346fc-3c21-4fcd-b187-72096568575a",
    "description": "Lists all of a location's discounts.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "12cef7d7-5445-4b18-ad67-c3affc770684",
          "name": "getLocationDiscounts",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/discounts"
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
            "description": "Lists all of a location's discounts"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d4f5585d-0910-45a7-b8dd-422e0820af1c"
            }
          ]
        }
      ]
    }
  ]
}