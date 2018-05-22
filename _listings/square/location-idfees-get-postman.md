{
  "info": {
    "name": "Square Connect API Get Location Fees",
    "_postman_id": "e8fcdc6c-e7dd-4505-88fe-47f4f75aac40",
    "description": "Lists all of a location's fees (taxes).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "52e5099e-fe69-4af5-bf94-e943069d93c7",
          "name": "getLocationFees",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/fees"
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
            "description": "Lists all of a location's fees (taxes)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "14ca4358-78e0-4f09-8137-37605b3339ba"
            }
          ]
        }
      ]
    }
  ]
}