{
  "info": {
    "name": "Square Connect API Get Location Modifier Lists Modifier List",
    "_postman_id": "fa2a3418-05de-415d-9dfd-2fc9578c51bd",
    "description": "Provides the details for a single modifier list.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "6c05ddf9-58ef-4da4-9635-2c4339a0943c",
          "name": "getLocationModifierListsModifierList",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/modifier-lists/:modifier_list_id"
              ],
              "variable": [
                {
                  "id": "location_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "modifier_list_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Provides the details for a single modifier list"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c99d8f76-9205-4619-acf1-e102159ac54b"
            }
          ]
        }
      ]
    }
  ]
}