{
  "info": {
    "name": "Square Connect API Delete Location Items Item Modifier Lists Modifier List",
    "_postman_id": "a1d7ec38-405a-4025-865a-c7a63023859c",
    "description": "Removes a modifier list association from an item, meaning modifier options from the list can no longer be applied to the item.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "741a2681-5dea-440b-a489-c182ca1539e2",
          "name": "deleteLocationItemsItemModifierListsModifierList",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/items/:item_id/modifier-lists/:modifier_list_id"
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
            "description": "Removes a modifier list association from an item, meaning modifier options from the list can no longer be applied to the item"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6981fa41-8940-4827-9540-ba3a383ae4d1"
            }
          ]
        }
      ]
    }
  ]
}