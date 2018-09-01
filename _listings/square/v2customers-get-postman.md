{
  "info": {
    "name": "Square Connect API ListCustomers",
    "_postman_id": "142b064e-6fc1-41a2-9d25-de70b7a8330b",
    "description": "Lists a business's customers.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "ListCustomers",
      "item": [
        {
          "id": "f3975f5e-0fe0-4e9b-be00-91d24b76a2d9",
          "name": "ListCustomers",
          "request": {
            "url": "http://connect.squareup.com/v2/customers?cursor=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "The value to provide in the Authorization header ofyour request",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Lists a business's customers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ad03edf9-75f5-4b10-85c0-c206f9200dde"
            }
          ]
        }
      ]
    }
  ]
}