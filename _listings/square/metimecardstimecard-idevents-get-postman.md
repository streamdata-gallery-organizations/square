{
  "info": {
    "name": "Square Connect API Get Me Timecards Events",
    "_postman_id": "51e639c4-c557-4b84-8220-e4f5ae9a7f34",
    "description": "Provides summary information for all events associated with a particular timecard.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "me",
      "item": [
        {
          "id": "934e8b20-b39d-47bd-b9e2-2bd6da16f836",
          "name": "getMeTimecardsTimecardEvents",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1",
                "me/timecards/:timecard_id/events"
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
            "description": "Provides summary information for all events associated with a particular timecard"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "846fc6fd-c938-4438-a7f2-275f806ba3aa"
            }
          ]
        }
      ]
    }
  ]
}