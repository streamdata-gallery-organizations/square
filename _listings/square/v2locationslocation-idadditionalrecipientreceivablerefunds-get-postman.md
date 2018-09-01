{
  "info": {
    "name": "Square Connect API Get V2 Locations Location Additional Recipient Receivable Refunds",
    "_postman_id": "15dd7670-00b1-4ff0-87a9-453ea5618fa0",
    "description": "Returns a list of refunded transactions (across all possible originating locations) relating to monies\ncredited to the provided location ID by another Square account using the `additional_recipients` field in a transaction.\n\nMax results per [page](#paginatingresults): 50",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "locations",
      "item": [
        {
          "id": "017c3172-b16c-4950-b883-fca1b7db7b63",
          "name": "getV2LocationsLocationAdditionalRecipientReceivableRefunds",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                "v2/locations/:location_id/additional-recipient-receivable-refunds"
              ],
              "query": [
                {
                  "key": "begin_time",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "cursor",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "end_time",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort_order",
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
            "description": "Returns a list of refunded transactions (across all possible originating locations) relating to monies\ncredited to the provided location ID by another Square account using the `additional_recipients` field in a transaction"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "994501d8-a329-4741-a1b8-5be21d65841c"
            }
          ]
        }
      ]
    }
  ]
}