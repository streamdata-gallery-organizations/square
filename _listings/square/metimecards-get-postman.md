{
  "info": {
    "name": "Square Connect API Get Me Timecards",
    "_postman_id": "f27c8ff0-efdf-405f-8b41-6cba414b5514",
    "description": "Provides summary information for all of a business's employee timecards.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "me",
      "item": [
        {
          "id": "be2d88e4-8cc1-472f-bd82-5f7f0aa831cd",
          "name": "getMeTimecards",
          "request": {
            "url": "http://connect.squareup.com/v1/me/timecards?batch_token=%7B%7D&begin_clockin_time=%7B%7D&begin_clockout_time=%7B%7D&begin_updated_at=%7B%7D&deleted=%7B%7D&employee_id=%7B%7D&end_clockin_time=%7B%7D&end_clockout_time=%7B%7D&end_updated_at=%7B%7D&limit=%7B%7D&order=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Provides summary information for all of a business's employee timecards"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "68e11eff-ca9e-49bd-9fea-31bdd89615a7"
            }
          ]
        }
      ]
    }
  ]
}