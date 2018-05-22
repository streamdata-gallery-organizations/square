{
  "info": {
    "name": "Square Connect API Get Location Categories",
    "_postman_id": "8e00772f-db44-463f-b17f-3ae615c2b0b5",
    "description": "Lists all of a location's item categories.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "c3b51665-081f-4013-956f-873776cde09d",
          "name": "getLocationCategories",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/categories"
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
            "description": "Lists all of a location's item categories"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e0190848-2722-40df-9cf7-bdeaaff0879f"
            }
          ]
        }
      ]
    }
  ]
}