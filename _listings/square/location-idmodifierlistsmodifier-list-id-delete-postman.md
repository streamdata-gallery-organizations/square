{
  "info": {
    "name": "Square Connect API Delete Location Modifier Lists Modifier List",
    "_postman_id": "c4c76ca0-237f-4cc7-ab2c-d6ce78e21986",
    "description": "Deletes an existing item modifier list and all modifier options associated with it.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "74823acf-69e9-4665-836a-0a6761460b31",
          "name": "deleteLocationModifierListsModifierList",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes an existing item modifier list and all modifier options associated with it"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9de52048-584c-4496-be4d-dd931984f688"
            }
          ]
        }
      ]
    }
  ]
}