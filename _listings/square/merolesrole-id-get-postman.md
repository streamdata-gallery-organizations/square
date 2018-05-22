{
  "info": {
    "name": "Square Connect API Get Me Roles Role",
    "_postman_id": "b25671a6-b633-4d3c-ae90-0904fd3c54e5",
    "description": "Provides the details for a single employee role.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "me",
      "item": [
        {
          "id": "2a3cbfc1-033a-42d5-8b86-f9441b29ea45",
          "name": "getMeRolesRole",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                "me/roles/:role_id"
              ],
              "variable": [
                {
                  "id": "role_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Provides the details for a single employee role"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a6bd0f1e-4541-490b-836b-9b273448a6bb"
            }
          ]
        }
      ]
    }
  ]
}