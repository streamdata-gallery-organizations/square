{
  "info": {
    "name": "Square Connect API Get Me Timecards",
    "_postman_id": "b536d657-33eb-4377-b5a1-a9bff1add6ca",
    "description": "Provides the details for a single timecard.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "me",
      "item": [
        {
          "id": "fc54da87-4f98-427d-980c-ec28495b2744",
          "name": "getMeTimecardsTimecard",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                "me/timecards/:timecard_id"
              ],
              "variable": [
                {
                  "id": "timecard_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Provides the details for a single timecard"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6e8326be-65ab-4c94-87b4-3912ce424c1b"
            }
          ]
        }
      ]
    }
  ]
}