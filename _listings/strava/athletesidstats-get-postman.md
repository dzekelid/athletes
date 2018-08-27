{
  "info": {
    "name": "Strava Get Athlete Stats",
    "_postman_id": "44d5523b-bb07-4419-83bd-599a0da4f619",
    "description": "Returns the activity stats of an athlete.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Sports",
      "item": [
        {
          "id": "11042860-ad8a-4de8-8f39-964fa7f8cdd1",
          "name": "getStats",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.strava.com",
              "path": [
                "api",
                "v3",
                "athletes/:id/stats"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the activity stats of an athlete."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "8f2832c9-3285-4d65-a3e6-c669e81697af"
            }
          ]
        }
      ]
    }
  ]
}