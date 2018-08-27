---
swagger: "2.0"
x-collection-name: Strava
x-complete: 0
info:
  title: Strava Get Athlete Stats
  description: Returns the activity stats of an athlete.
  version: 1.0.0
host: www.strava.com
basePath: /api/v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /athletes/{id}/stats:
    get:
      summary: Get Athlete Stats
      description: Returns the activity stats of an athlete.
      operationId: getStats
      x-api-path-slug: athletesidstats-get
      parameters:
      - in: path
        name: id
        description: The identifier of the athlete
      - in: query
        name: No Name
      responses:
        200:
          description: Successful response
      tags:
      - Sports
      - Athlete
      - Stats
  /athlete:
    get:
      summary: Get Authenticated Athlete
      description: Returns the currently authenticated athlete.
      operationId: getLoggedInAthlete
      x-api-path-slug: athlete-get
      responses:
        200:
          description: Successful response
      tags:
      - Sports
      - Authenticated
      - Athlete
    put:
      summary: Update Athlete
      description: Update the currently authenticated athlete.
      operationId: updateLoggedInAthlete
      x-api-path-slug: athlete-put
      parameters:
      - in: body
        name: body
        description: The athlete entity to update
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - Sports
      - Athlete
  /athlete/activities:
    get:
      summary: List Athlete Activities
      description: Returns the activities of an athlete for a specific identifier.
      operationId: getLoggedInAthleteActivities
      x-api-path-slug: athleteactivities-get
      parameters:
      - in: query
        name: after
        description: An epoch timestamp to use for filtering activities that have
          taken place after a certain time
      - in: query
        name: before
        description: An epoch timestamp to use for filtering activities that have
          taken place before a certain time
      - in: query
        name: No Name
      responses:
        200:
          description: Successful response
      tags:
      - Sports
      - List
      - Athlete
      - Activities
  /athlete/clubs:
    get:
      summary: List Athlete Clubs
      description: Returns a list of the clubs whose membership includes the authenticated
        athlete.
      operationId: getLoggedInAthleteClubs
      x-api-path-slug: athleteclubs-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: Successful response
      tags:
      - Sports
      - List
      - Athlete
      - Clubs
  /athletes/{id}/routes:
    get:
      summary: List Athlete Routes
      description: Returns a list of the routes created by the authenticated athlete
        using their athlete ID.
      operationId: getRoutesByAthleteId
      x-api-path-slug: athletesidroutes-get
      parameters:
      - in: path
        name: id
        description: The identifier of the athlete
      - in: query
        name: No Name
      responses:
        200:
          description: Successful response
      tags:
      - Sports
      - List
      - Athlete
      - Routes
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---