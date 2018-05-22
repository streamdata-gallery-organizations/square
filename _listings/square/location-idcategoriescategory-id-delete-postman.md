{
  "info": {
    "name": "Square Connect API Delete Location Categories Category",
    "_postman_id": "7bde8dd3-5bbe-49f2-ad0d-0e6e427f25d5",
    "description": "Delete location categories category.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "3df92ffc-19da-4fb0-9eaa-405250b1f94f",
          "name": "deleteLocationCategoriesCategory",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/categories/:category_id"
              ],
              "variable": [
                {
                  "id": "category_id",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete location categories category"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "371d1c8d-6708-4c23-8898-2e6aef99bd5d"
            }
          ]
        }
      ]
    }
  ]
}