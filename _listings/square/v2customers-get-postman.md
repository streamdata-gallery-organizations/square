{
  "info": {
    "name": "Square Connect API Get V2 Customers",
    "_postman_id": "0345e471-0e3c-440b-ad37-b7d81bccddd3",
    "description": "Lists a business's customers.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "customers",
      "item": [
        {
          "id": "a59ad778-26e6-4b83-bf50-cfbdb03c2f59",
          "name": "getV2Customers",
          "request": {
            "url": "http://connect.squareup.com/v1/v2/customers?cursor=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists a business's customers"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "60113606-5c22-437f-9369-9292d3a192f6"
            }
          ]
        }
      ]
    }
  ]
}