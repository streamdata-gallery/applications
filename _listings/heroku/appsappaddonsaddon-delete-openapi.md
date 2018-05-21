---
swagger: "2.0"
x-collection-name: Heroku
x-complete: 0
info:
  title: Heroku Delete Applications Addons
  description: Uninstall an addon from an app.
  version: "1"
host: api.heroku.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /apps/{app}/addons/{addon}:
    parameters:
      summary: Parameters Applications Addons
      description: Parameters applications addons.
      operationId: parametersAppsAppAddonsAddon
      x-api-path-slug: appsappaddonsaddon-parameters
      responses:
        200:
          description: OK
      tags:
      - Parameters
      - Applications
      - ons
    delete:
      summary: Delete Applications Addons
      description: Uninstall an addon from an app.
      operationId: deleteAppsAppAddonsAddon
      x-api-path-slug: appsappaddonsaddon-delete
      parameters:
      - in: header
        name: Accept
        description: Content type
      responses:
        200:
          description: OK
      tags:
      - Applications
      - ons
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