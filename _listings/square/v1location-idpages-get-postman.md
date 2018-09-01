{
  "info": {
    "name": "Square Connect API Lists all of a location's Favorites pages in Square Register.",
    "_postman_id": "85d606d8-15c8-41ea-8ef3-d458fa512289",
    "description": "Lists all of a location's Favorites pages in Square Register.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Lists",
      "item": [
        {
          "id": "a75b19b8-cb39-4eef-8145-156f59e6bf22",
          "name": "ListPages",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1/:location_id/pages"
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
            "description": "Lists all of a location's Favorites pages in Square Register."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3a7cce01-f2aa-44d3-b6a7-d332cb27d07d"
            }
          ]
        }
      ]
    }
  ]
}