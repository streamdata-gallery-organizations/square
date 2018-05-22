{
  "info": {
    "name": "Square Connect API Delete Location Fees Fee",
    "_postman_id": "64acda73-e141-48cf-86a0-c7f9d4a2c460",
    "description": "Deletes an existing fee (tax).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "9ef4a87b-51f1-42b1-82ed-0e1b9e0d3ccc",
          "name": "deleteLocationFeesFee",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/fees/:fee_id"
              ],
              "variable": [
                {
                  "id": "fee_id",
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
            "description": "Deletes an existing fee (tax)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d520d4cb-da7f-4848-beee-42d0b6ce0b30"
            }
          ]
        }
      ]
    }
  ]
}