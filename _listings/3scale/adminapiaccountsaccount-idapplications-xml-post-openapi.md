---
swagger: "2.0"
x-collection-name: 3scale
x-complete: 0
info:
  title: 3Scale Account Management API Application Create
  description: Application create.
  termsOfService: http://www.3scale.net/terms-and-conditions/
  contact:
    name: 3Scale
    url: https://support.3scale.net/
  version: "1"
host: su1.3scale.net
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /admin/api/accounts/{account_id}/applications.xml:
    get:
      summary: Application List
      description: Application list.
      operationId: application
      x-api-path-slug: adminapiaccountsaccount-idapplications-xml-get
      parameters:
      - in: path
        name: account_id
        description: id of the account
      - in: query
        name: provider_key
        description: Your api key with 3scale (also known as provider key)
      responses:
        200:
          description: OK
      tags:
      - Application
      - List
    post:
      summary: Application Create
      description: Application create.
      operationId: application
      x-api-path-slug: adminapiaccountsaccount-idapplications-xml-post
      parameters:
      - in: path
        name: account_id
        description: id of the account
      - in: query
        name: additional_fields
        description: Additional fields have to be name and value i
      - in: query
        name: description
        description: Description of the application to be created
      - in: query
        name: name
        description: Name of the application to be created
      - in: query
        name: plan_id
        description: id of the application plan
      - in: query
        name: provider_key
        description: Your api key with 3scale (also known as provider key)
      responses:
        200:
          description: OK
      tags:
      - Application
      - Create
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