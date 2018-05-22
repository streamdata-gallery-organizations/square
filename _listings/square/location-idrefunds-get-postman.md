{
  "info": {
    "name": "Square Connect API Get Location Refunds",
    "_postman_id": "5af645fc-a5a5-4b09-8fab-a1a2da6c6183",
    "description": "Provides the details for all refunds initiated by a merchant or any of the merchant's mobile staff during a date range. Date ranges cannot exceed one year in length.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "1943b35a-a083-40a1-89a1-8fb22ef55cb1",
          "name": "getLocationRefunds",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/refunds"
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
            "description": "Provides the details for all refunds initiated by a merchant or any of the merchant's mobile staff during a date range"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5b696660-9221-4a0c-ba6d-3449001023c3"
            }
          ]
        }
      ]
    }
  ]
}