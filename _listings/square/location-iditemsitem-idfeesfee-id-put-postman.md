{
  "info": {
    "name": "Square Connect API Put Location Items Item Fees Fee",
    "_postman_id": "4f117f46-ceb5-46c2-a1b7-d0388e8a9b1d",
    "description": "Associates a fee with an item, meaning the fee is automatically applied to the item in Square Register.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "ffa66cd5-9cd4-4735-9805-d4b0e24ad797",
          "name": "putLocationItemsItemFeesFee",
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
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Associates a fee with an item, meaning the fee is automatically applied to the item in Square Register"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cac0046b-515c-4f3f-95c2-245388c9a62d"
            }
          ]
        }
      ]
    }
  ]
}