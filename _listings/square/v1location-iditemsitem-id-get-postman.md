{
  "info": {
    "name": "Square Connect API Provides the details for a single item, including associated modifier lists and fees.",
    "_postman_id": "c502e8c3-e0e0-4cb9-8096-4d46a4862c7c",
    "description": "Provides the details for a single item, including associated modifier lists and fees.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Lists",
      "item": [
        {
          "id": "b6e31f84-be4b-4aeb-a6fc-cd59d933fc5f",
          "name": "ListFees",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1/:location_id/fees"
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
            "description": "Lists all of a location's fees (taxes)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "33c31510-0de0-4cea-bc90-17620abdcf3b"
            }
          ]
        }
      ]
    },
    {
      "name": "Provides",
      "item": [
        {
          "id": "c625a136-a098-4000-903e-e6fcb3c06006",
          "name": "RetrieveItem",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1/:location_id/items/:item_id"
              ],
              "variable": [
                {
                  "id": "item_id",
                  "value": "{}",
                  "type": "string"
                },
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
            "description": "Provides the details for a single item, including associated modifier lists and fees."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "de6dda7e-5fa4-49ef-a050-20f6aad68e45"
            }
          ]
        }
      ]
    }
  ]
}