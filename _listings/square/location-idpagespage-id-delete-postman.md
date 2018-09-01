{
  "info": {
    "name": "Square Connect API Delete Location Pages Page",
    "_postman_id": "386c274d-90c5-4f7f-b27e-1026ef845934",
    "description": "Deletes an existing Favorites page and all of its cells.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "122e43e0-6ede-4f01-bd70-68c903f01c55",
          "name": "deleteLocationPagesPage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/pages/:page_id"
              ],
              "variable": [
                {
                  "id": "location_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "page_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes an existing Favorites page and all of its cells"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1fc59400-647b-4eec-9f80-9011260e8651"
            }
          ]
        }
      ]
    }
  ]
}