{
  "info": {
    "name": "Square Connect API Delete Me Timecards",
    "_postman_id": "de4c4716-eeb3-4edf-8ddc-2c5d367fc8f8",
    "description": "Deletes a timecard. Deleted timecards are still accessible from Connect API endpoints, but the value of their deleted field is set to true. See Handling deleted timecards for more information.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "me",
      "item": [
        {
          "id": "c720ed5b-bb75-4d7e-ba6e-c41220ce3c81",
          "name": "deleteMeTimecardsTimecard",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a timecard"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c0970831-1017-426a-8cc8-dcaa3cad96ba"
            }
          ]
        }
      ]
    }
  ]
}