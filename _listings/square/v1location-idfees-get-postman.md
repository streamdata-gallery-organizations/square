{
  "info": {
    "name": "Square Connect API Lists all of a location's fees (taxes).",
    "_postman_id": "571322a2-09ab-450f-8362-cf138afce268",
    "description": "Lists all of a location's fees (taxes).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Lists",
      "item": [
        {
          "id": "b7a5c60b-e998-4d6d-ac96-8285796911a4",
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
              "id": "d8641e7a-717d-4388-b96d-7e3817c88254"
            }
          ]
        }
      ]
    }
  ]
}