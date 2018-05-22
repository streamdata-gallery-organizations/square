{
  "info": {
    "name": "Square Connect API Get Location Payments Payment",
    "_postman_id": "661bcc43-770a-4ead-a6aa-99a20abe5ce6",
    "description": "Provides comprehensive information for a single payment.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "location",
      "item": [
        {
          "id": "31e6b1f6-b179-4782-ba41-5620f1e07963",
          "name": "getLocationPaymentsPayment",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                ":location_id/payments/:payment_id"
              ],
              "variable": [
                {
                  "id": "location_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "payment_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Provides comprehensive information for a single payment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "01d02241-de8d-4ca7-adf1-19eefdb15bba"
            }
          ]
        }
      ]
    }
  ]
}