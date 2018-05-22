{
  "info": {
    "name": "Square Connect API Get Location Modifier Lists",
    "_postman_id": "0823e77e-c8c2-4e09-a06f-8275af139b57",
    "description": "Lists all of a location's modifier lists.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "e330ed40-e718-48cf-8d6e-272532057bef",
          "name": "getLocationModifierLists",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/modifier-lists"
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
            "description": "Lists all of a location's modifier lists"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f7e0df83-ed14-4dc9-bce3-f9f39bb376c0"
            }
          ]
        }
      ]
    }
  ]
}