{
  "info": {
    "name": "Square Connect API Delete Location Items Item Fees Fee",
    "_postman_id": "b1db3d3b-48d5-4e6f-9888-a7b76c25ae4d",
    "description": "Removes a fee assocation from an item, meaning the fee is no longer automatically applied to the item in Square Register.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "493fb3b6-a0e9-4fba-b032-49be80d79818",
          "name": "deleteLocationItemsItemFeesFee",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/items/:item_id/fees/:fee_id"
              ],
              "variable": [
                {
                  "id": "fee_id",
                  "value": "{}",
                  "type": "string"
                },
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Removes a fee assocation from an item, meaning the fee is no longer automatically applied to the item in Square Register"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ae7909c9-2761-4e79-8a73-e653e8355cf2"
            }
          ]
        }
      ]
    }
  ]
}