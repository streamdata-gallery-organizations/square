{
  "info": {
    "name": "Square Connect API Lists all of a location's item categories.",
    "_postman_id": "debe3d61-8b3c-4291-990b-17f030fb47ae",
    "description": "Lists all of a location's item categories.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Lists",
      "item": [
        {
          "id": "f01bb80c-237b-4c61-a342-885fc4365c51",
          "name": "ListCategories",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1/:location_id/categories"
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
            "description": "Lists all of a location's item categories."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b51d8a95-5373-4709-9678-b35a9493dd2a"
            }
          ]
        }
      ]
    }
  ]
}