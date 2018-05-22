{
  "info": {
    "name": "Square Connect API Get Me Roles",
    "_postman_id": "a6c9e313-ff3b-4276-8956-689cb1a035cd",
    "description": "Provides summary information for all of a business's employee roles.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "me",
      "item": [
        {
          "id": "7ff443c3-0655-47d4-8810-b29d45643c65",
          "name": "getMeRoles",
          "request": {
            "url": "http://connect.squareup.com/v1/me/roles?batch_token=%7B%7D&limit=%7B%7D&order=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Provides summary information for all of a business's employee roles"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f4c550e6-8531-4642-8957-300e772485a3"
            }
          ]
        }
      ]
    }
  ]
}