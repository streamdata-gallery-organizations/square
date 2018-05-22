{
  "info": {
    "name": "Square Connect API Delete V2 Customers Customer",
    "_postman_id": "7c0d48f2-7d31-46b3-b8b0-1fa7ec247276",
    "description": "Deletes a customer from a business, along with any linked cards on file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "customers",
      "item": [
        {
          "id": "e967f934-2209-4bef-a607-8533d75532a3",
          "name": "deleteV2CustomersCustomer",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a customer from a business, along with any linked cards on file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e108c1fd-51d5-4b5d-af89-c8872d91b708"
            }
          ]
        }
      ]
    }
  ]
}