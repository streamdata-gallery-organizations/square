{
  "info": {
    "name": "Square Connect API Delete Location Discounts Discount",
    "_postman_id": "df66f6e5-a715-424b-a856-bba5cf6524a2",
    "description": "Delete location discounts discount.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "7a36af9b-a091-4bd5-8293-1204f8cc6195",
          "name": "deleteLocationDiscountsDiscount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/discounts/:discount_id"
              ],
              "variable": [
                {
                  "id": "discount_id",
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
            "description": "Delete location discounts discount"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "866ecf69-bea1-4237-bd97-b0851f4723e6"
            }
          ]
        }
      ]
    }
  ]
}