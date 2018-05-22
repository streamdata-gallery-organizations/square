{
  "info": {
    "name": "Square Connect API Get Location Payments",
    "_postman_id": "1ef21b9c-cf0b-432b-abf5-ee83f244fde5",
    "description": "Provides summary information for all payments taken by a merchant or any of the merchant's mobile staff during a date range. Date ranges cannot exceed one year in length. See Date ranges for details of inclusive and exclusive dates.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "257753bd-77f2-4576-a9aa-fb9271709acf",
          "name": "getLocationPayments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/payments"
              ],
              "query": [
                {
                  "key": "batch_token",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "begin_time",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "end_time",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "order",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "location_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Provides summary information for all payments taken by a merchant or any of the merchant's mobile staff during a date range"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d7a95653-c68b-404e-a97d-fdc9ab8595ed"
            }
          ]
        }
      ]
    }
  ]
}