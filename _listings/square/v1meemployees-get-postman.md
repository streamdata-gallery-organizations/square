{
  "info": {
    "name": "Square Connect API Provides summary information for all of a business's employees.",
    "_postman_id": "3db62ceb-5820-4804-af37-456e7994d3e6",
    "description": "Provides summary information for all of a business's employees.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Businesss",
      "item": [
        {
          "id": "6bee484d-a1a9-4e89-abb0-52b883331e9d",
          "name": "RetrieveBusiness",
          "request": {
            "url": "http://connect.squareup.com/v1/me",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a business's information."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "673155d2-085b-4d9e-809e-7d2fd899f692"
            }
          ]
        }
      ]
    },
    {
      "name": "Provides",
      "item": [
        {
          "id": "c6dda7fd-d8c0-4ef1-96d9-308633172144",
          "name": "ListEmployees",
          "request": {
            "url": "http://connect.squareup.com/v1/me/employees?batch_token=%7B%7D&begin_created_at=%7B%7D&begin_updated_at=%7B%7D&end_created_at=%7B%7D&end_updated_at=%7B%7D&external_id=%7B%7D&limit=%7B%7D&order=%7B%7D&status=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Provides summary information for all of a business's employees."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7b6b7b7a-2664-4d49-8ee8-fcadc512e3f6"
            }
          ]
        }
      ]
    }
  ]
}