{
  "info": {
    "name": "Square Connect API Delete Location Pages Page Cells",
    "_postman_id": "0d10bd64-cb24-48a8-8b82-f6a8191009b4",
    "description": "Deletes a cell from a Favorites page in Square Register.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "f20f9aea-07f5-4c4b-9e0f-2530207e6940",
          "name": "deleteLocationPagesPageCells",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/pages/:page_id/cells"
              ],
              "query": [
                {
                  "key": "column",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "row",
                  "value": "%7B%7D",
                  "disabled": false
                }
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
            "description": "Deletes a cell from a Favorites page in Square Register"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4224e7d1-a77a-4e27-a732-a6e876d8b383"
            }
          ]
        }
      ]
    }
  ]
}