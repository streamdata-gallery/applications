---
swagger: "2.0"
x-collection-name: Twilio
x-complete: 0
info:
  title: Twilio Get Authorized Connected App
  description: Get the properties of the authorized application.
  termsOfService: https://www.twilio.com/legal/tos
  version: v1
host: api.twilio.com
basePath: /2010-04-01/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Accounts/{AccountSid}/Applications/{ApplicationSid}.{format}:
    delete:
      summary: Delete Application
      description: Delete Application
      operationId: delete-this-application
      x-api-path-slug: accountsaccountsidapplicationsapplicationsid-format-delete
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: ApplicationSid
        description: The ID for the Twilio application
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Applications
    get:
      summary: Get Application
      description: Get application instance resource.
      operationId: get-application-instance-resource
      x-api-path-slug: accountsaccountsidapplicationsapplicationsid-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: ApplicationSid
        description: The ID for the Twilio application
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Applications
    post:
      summary: Add Application
      description: Tries to update the applications properties, and returns the updatednresource
        representation if successful. The returned response is identicalnto that returned
        above when making a GET request.n
      operationId: tries-to-update-the-applications-properties-and-returns-the-updatedresource-representation-if-succes
      x-api-path-slug: accountsaccountsidapplicationsapplicationsid-format-post
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: ApplicationSid
        description: The ID for the Twilio application
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /Accounts/{AccountSid}/Applications.{format}:
    get:
      summary: Get Applications
      description: Get Applications
      operationId: returns-a-list-of-application-resource-representations-each-representingan-application-within-your-a
      x-api-path-slug: accountsaccountsidapplications-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Applications
    post:
      summary: Add Applications
      description: Add Applications
      operationId: creates-a-new-application-within-your-account
      x-api-path-slug: accountsaccountsidapplications-format-post
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /Accounts/{AccountSid}/AuthorizedConnectApps/{ConnectAppSid}.{format}:
    get:
      summary: Get Authorized Connected App
      description: Get the properties of the authorized application.
      operationId: get-the-properties-of-the-authorized-application
      x-api-path-slug: accountsaccountsidauthorizedconnectappsconnectappsid-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: ConnectAppSid
        description: A 34 character string that uniquely identifies the connected
          app
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /Accounts/{AccountSid}/AuthorizedConnectApps.{format}:
    get:
      summary: Get Authorized Connected Apps
      description: Returns a list of Connect App resource representations, each representing
        anConnect App youve authorized to access your account. The list includesnpaging
        information.n
      operationId: returns-a-list-of-connect-app-resource-representations-each-representing-aconnect-app-youve-authoriz
      x-api-path-slug: accountsaccountsidauthorizedconnectapps-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /Accounts/{AccountSid}/ConnectApps/{ConnectAppSid}.{format}:
    get:
      summary: Get Connected App
      description: Get the properties of a Connect App.
      operationId: get-the-properties-of-a-connect-app
      x-api-path-slug: accountsaccountsidconnectappsconnectappsid-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: ConnectAppSid
        description: A 34 character string that uniquely identifies the connected
          app
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Applications
    post:
      summary: Add Connected App
      description: Tries to update the Connect Apps properties, and returns the updatednresource
        representation if successful. The returned response is identicalnto that returned
        above when making a GET request.n
      operationId: tries-to-update-the-connect-apps-properties-and-returns-the-updatedresource-representation-if-succes
      x-api-path-slug: accountsaccountsidconnectappsconnectappsid-format-post
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: ConnectAppSid
        description: A 34 character string that uniquely identifies the connected
          app
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /Accounts/{AccountSid}/ConnectApps.{format}:
    get:
      summary: Get Connected Apps
      description: Returns a list of Connect App resource representations, each representingna
        Connect App in your account. The list includes paging information.n
      operationId: returns-a-list-of-connect-app-resource-representations-each-representinga-connect-app-in-your-accoun
      x-api-path-slug: accountsaccountsidconnectapps-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Applications
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