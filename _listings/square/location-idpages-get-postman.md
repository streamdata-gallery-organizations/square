{
  "info": {
    "name": "Square Connect API Get Location Pages",
    "_postman_id": "21a3fe10-2622-47ed-8658-4cba448cfc41",
    "description": "Lists all of a location's Favorites pages in Square Register.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "d74daa5e-cfb7-4b60-ac9c-677e63490256",
          "name": "getLocationPages",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/pages"
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
            "description": "Lists all of a location's Favorites pages in Square Register"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a1200cc6-93cd-455d-b905-3a25a1e57932"
            }
          ]
        }
      ]
    }
  ]
}