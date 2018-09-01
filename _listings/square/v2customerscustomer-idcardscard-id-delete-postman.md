{
  "info": {
    "name": "Square Connect API Delete V2 Customers Customer Cards Card",
    "_postman_id": "d91b1c4c-069a-4e69-b26c-411b849b548d",
    "description": "Delete v2 customers customer cards card.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "customers",
      "item": [
        {
          "id": "d68f2b48-7613-411e-8583-13ec39fca151",
          "name": "deleteV2CustomersCustomerCardsCard",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                "v2/customers/:customer_id/cards/:card_id"
              ],
              "variable": [
                {
                  "id": "card_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "customer_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete v2 customers customer cards card"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ffa8983c-d769-4e25-a681-e54e7923988f"
            }
          ]
        }
      ]
    }
  ]
}