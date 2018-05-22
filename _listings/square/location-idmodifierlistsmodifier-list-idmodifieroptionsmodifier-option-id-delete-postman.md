{
  "info": {
    "name": "Square Connect API Delete Location Modifier Lists Modifier List Modifier Options Modifier Option",
    "_postman_id": "ed361851-e1fb-453e-b8e2-d22046d26fed",
    "description": "Delete location modifier lists modifier list modifier options modifier option.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "838b1439-7960-45e0-8bb7-493f4da57e4b",
          "name": "deleteLocationModifierListsModifierListModifierOptionsModifierOption",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/modifier-lists/:modifier_list_id/modifier-options/:modifier_option_id"
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
                },
                {
                  "id": "modifier_option_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete location modifier lists modifier list modifier options modifier option"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f3d24d51-6d4a-44ac-a319-8582357281c9"
            }
          ]
        }
      ]
    }
  ]
}