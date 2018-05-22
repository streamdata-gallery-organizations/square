{
  "info": {
    "name": "Square Connect API Put Location Items Item Modifier Lists Modifier List",
    "_postman_id": "bf15d1d9-c106-4609-96c6-a4d50e954fac",
    "description": "Associates a modifier list with an item, meaning modifier options from the list can be applied to the item.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "48071be4-ca78-4a7c-a4a3-6fd2c8bdfe5a",
          "name": "putLocationItemsItemModifierListsModifierList",
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
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Associates a modifier list with an item, meaning modifier options from the list can be applied to the item"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dcb62580-e3a1-469a-8318-0da9200b8027"
            }
          ]
        }
      ]
    }
  ]
}