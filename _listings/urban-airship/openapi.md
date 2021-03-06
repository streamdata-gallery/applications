swagger: "2.0"
x-collection-name: Urban Airship
x-complete: 1
info:
  title: Urban Airship
  description: the-urban-airships-api-powers-mobile-applications-with-push-rich-push-inapp-purchases-and-subscription-services-
  version: v3
host: go.urbanairship.com
basePath: /api/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /app/content:
    get:
      summary: Get App Content
      description: Gets the store inventory.
      operationId: app.content.get
      x-api-path-slug: appcontent-get
      parameters:
      - in: query
        name: Content-Type
        description: Content type
      - in: query
        name: user_id
        description: The user ID
      responses:
        200:
          description: OK
      tags:
      - App
      - Content
  /app/content/{product_id}/download:
    post:
      summary: Post App Content Product Download
      description: Returns a temporary URL where the client can download the content.
        In the payload, the receipt string is the receipt data from the purchase.
        It should be unaltered from how Apple delivers it to your application.udid
        is an optional field to help identify a particular user???s purchases, which
        can aid debugging. It should always be a hash of the UDID, not the actual
        UDID, to ensure compliance with Apple???s TOS. The optional version field
        should be the StoreFront library version, or custom if you???re building your
        own.
      operationId: app.content.product_id.download.post
      x-api-path-slug: appcontentproduct-iddownload-post
      parameters:
      - in: header
        name: Content-Type
        description: Content type
      - in: query
        name: Content-Type
        description: Content type
      - in: query
        name: product_id
        description: The product ID
      - in: path
        name: product_id
      responses:
        200:
          description: OK
      tags:
      - App
      - Content
      - Product
      - Id
      - Download
  /app/updates:
    post:
      summary: Post App Updates
      description: Checks for updates. It can be useful on application launch to compare
        a list of installed updates with our server to see if there are any updates
        to be had for the content.
      operationId: app.updates.post
      x-api-path-slug: appupdates-post
      parameters:
      - in: header
        name: Content-Type
        description: Content type
      - in: query
        name: Content-Type
        description: Content type
      - in: query
        name: product_id
        description: The product ID
      responses:
        200:
          description: OK
      tags:
      - App
      - Updates
  /partner/apps/{app_id}:
    put:
      summary: Put Partner Apps App
      description: Updates an application.
      operationId: partner.apps.app_id.put
      x-api-path-slug: partnerappsapp-id-put
      parameters:
      - in: query
        name: app_id
        description: A specific application
      - in: path
        name: app_id
      - in: header
        name: Content-Type
        description: Content type
      - in: query
        name: Content-Type
        description: Content type
      responses:
        200:
          description: OK
      tags:
      - Partner
      - Apps
      - App
      - Id
  /partner/apps:
    get:
      summary: Get Partner Apps
      description: List applications.
      operationId: partner.apps.get
      x-api-path-slug: partnerapps-get
      parameters:
      - in: query
        name: device_token
        description: A specific device token
      - in: query
        name: tag
        description: Tags can be of any format you wish, but we recommend that they
          be URL-safe in order to make less work for you
      responses:
        200:
          description: OK
      tags:
      - Partner
      - Apps
    post:
      summary: Post Partner Apps
      description: Adds a new application.
      operationId: partner.apps.post
      x-api-path-slug: partnerapps-post
      parameters:
      - in: header
        name: Content-Type
        description: Content type
      - in: query
        name: Content-Type
        description: Content type
      responses:
        200:
          description: OK
      tags:
      - Partner
      - Apps