---
swagger: "2.0"
x-collection-name: Google Play
x-complete: 0
info:
  title: Google Play Update App Detail
  version: 1.0.0
  description: Updates app details for this edit.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{packageName}/edits:
    post:
      summary: Create App Edit
      description: Creates a new edit for an app, populated with the app's current
        state.
      operationId: androidpublisher.edits.insert
      x-api-path-slug: packagenameedits-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Application
  /{packageName}/edits/{editId}:
    delete:
      summary: Delete App Edit
      description: Deletes an edit for an app. Creating a new edit will automatically
        delete any of your previous edits so this method need only be called if you
        want to preemptively abandon an edit.
      operationId: androidpublisher.edits.delete
      x-api-path-slug: packagenameeditseditid-delete
      parameters:
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Application
    get:
      summary: DGetelete App Edit
      description: Returns information about the edit specified. Calls will fail if
        the edit is no long active (e.g. has been deleted, superseded or expired).
      operationId: androidpublisher.edits.get
      x-api-path-slug: packagenameeditseditid-get
      parameters:
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Application
  /{packageName}/edits/{editId}/apks/externallyHosted:
    post:
      summary: Create APK
      description: Creates a new APK without uploading the APK itself to Google Play,
        instead hosting the APK at a specified URL. This function is only available
        to enterprises using Google Play for Work whose application is configured
        to restrict distribution to the enterprise domain.
      operationId: androidpublisher.edits.apks.addexternallyhosted
      x-api-path-slug: packagenameeditseditidapksexternallyhosted-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Application
  /{packageName}/edits/{editId}/details:
    get:
      summary: Get App Detail
      description: Fetches app details for this edit. This includes the default language
        and developer support contact information.
      operationId: androidpublisher.edits.details.get
      x-api-path-slug: packagenameeditseditiddetails-get
      parameters:
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Application
    patch:
      summary: Update App Detail
      description: Updates app details for this edit. This method supports patch semantics.
      operationId: androidpublisher.edits.details.patch
      x-api-path-slug: packagenameeditseditiddetails-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Application
    put:
      summary: Update App Detail
      description: Updates app details for this edit.
      operationId: androidpublisher.edits.details.update
      x-api-path-slug: packagenameeditseditiddetails-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Application
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