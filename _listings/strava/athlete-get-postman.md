{
  "info": {
    "name": "Strava Get Authenticated Athlete",
    "_postman_id": "bb7d5e47-7a6b-43bf-b297-ba8a615d5474",
    "description": "Returns the currently authenticated athlete.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Sports",
      "item": [
        {
          "id": "943cfa53-28e0-4aad-bbad-49e1ad99c057",
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
              "id": "f268424a-3076-4aa4-8db1-4f6998167e6f"
            }
          ]
        },
        {
          "id": "c778c885-b763-4bf2-91ce-9ed1142371d8",
          "name": "getLoggedInAthlete",
          "request": {
            "url": "http://www.strava.com/api/v3/athlete",
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
            "description": "Returns the currently authenticated athlete."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "ef407d35-11a9-4171-bba5-f10d43c687ee"
            }
          ]
        }
      ]
    }
  ]
}