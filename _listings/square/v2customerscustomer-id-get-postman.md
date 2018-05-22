{
  "info": {
    "name": "Square Connect API Get V2 Customers Customer",
    "_postman_id": "0f826eb7-40f4-4d34-960c-93c452e6d191",
    "description": "Returns details for a single customer.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "customers",
      "item": [
        {
          "id": "b250f817-52d7-4671-8f1e-568b5c8ae2a3",
          "name": "getV2CustomersCustomer",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                "v2/customers/:customer_id"
              ],
              "variable": [
                {
                  "id": "customer_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns details for a single customer"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "069e1ce6-fce3-42a6-be7d-ca82b1814e17"
            }
          ]
        }
      ]
    }
  ]
}