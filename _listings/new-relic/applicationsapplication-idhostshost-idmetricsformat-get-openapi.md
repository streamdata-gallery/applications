---
swagger: "2.0"
x-collection-name: New Relic
x-complete: 0
info:
  title: New Relic Get Applications Application  Hosts Host  Metrics. Format
  version: 1.0.0
  description: |-
    Return a list of known metrics and their value names for the given resource.

    See our documentation for a discussion
    on  output pagination
    and for examples of requesting and using metric values.
basePath: v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /applications/{application_id}/deployments.{format}:
    get:
      summary: Get Applications Application  Deployments. Format
      description: |-
        This API endpoint returns a paginated list of the deployments associated with a given application.

        See our documentation for a discussion on output pagination.
      operationId: getApplicationsApplicationDeployments.Format
      x-api-path-slug: applicationsapplication-iddeploymentsformat-get
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: query
        name: page
        description: Pagination index
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Application
      - ""
      - Deployments.
      - Format
    post:
      summary: Add Applications Application  Deployments. Format
      description: "This API endpoint creates a deployment record for a given application.\nDeployment
        records are created with the following attributes:\n\nRequired:\n\_\_- Application
        ID\n\_\_- Revision, such as a git SHA\n\nOptional:\n\_\_- Changelog \n\_\_-
        Description \n\_\_- User posting the deployment\n\nNote that the time of your
        deployment will be recorded as the current time in UTC."
      operationId: postApplicationsApplicationDeployments.Format
      x-api-path-slug: applicationsapplication-iddeploymentsformat-post
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: body
        name: deployment
        description: Deployment schema
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Application
      - ""
      - Deployments.
      - Format
  /applications/{application_id}/deployments/{id}.{format}:
    delete:
      summary: Delete Applications Application  Deployments  . Format
      description: "This API endpoint deletes the specified deployment record.\n\nNote:
        Admin User\u2019s API Key is required."
      operationId: deleteApplicationsApplicationDeployments.Format
      x-api-path-slug: applicationsapplication-iddeploymentsidformat-delete
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: path
        name: id
        description: Deployment ID
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Application
      - ""
      - Deployments
      - ""
      - .
      - Format
  /applications/{application_id}/hosts.{format}:
    get:
      summary: Get Applications Application  Hosts. Format
      description: "This API endpoint returns a \npaginated list of hosts associated
        with the given application. The time range for summary data is the last 10
        minutes.\n\nApplication hosts can be filtered by hostname, or the list of
        application host IDs.\n\nSee our documentation for a discussion and examples
        of\nusing  filters \nand summary data output."
      operationId: getApplicationsApplicationHosts.Format
      x-api-path-slug: applicationsapplication-idhostsformat-get
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: query
        name: filter[hostname]
        description: Filter by server hostname
        type: string
      - in: query
        name: filter[ids]
        description: Filter by application host ids
        type: list
      - in: query
        name: page
        description: Pagination index
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Application
      - ""
      - Hosts.
      - Format
  /applications/{application_id}/hosts/{id}.{format}:
    get:
      summary: Get Applications Application  Hosts  . Format
      description: |-
        This API endpoint returns a single application host, identified by ID. The time range for summary data is the last 10 minutes.

        See our documentation for a discussion of
        summary data output.
      operationId: getApplicationsApplicationHosts.Format
      x-api-path-slug: applicationsapplication-idhostsidformat-get
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: path
        name: id
        description: Application host ID
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Application
      - ""
      - Hosts
      - ""
      - .
      - Format
  /applications/{application_id}/hosts/{host_id}/metrics.{format}:
    get:
      summary: Get Applications Application  Hosts Host  Metrics. Format
      description: |-
        Return a list of known metrics and their value names for the given resource.

        See our documentation for a discussion
        on  output pagination
        and for examples of requesting and using metric values.
      operationId: getApplicationsApplicationHostsHostMetrics.Format
      x-api-path-slug: applicationsapplication-idhostshost-idmetricsformat-get
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: query
        name: cursor
        description: Cursor for next page (replacing page param)
        type: string
      - in: path
        name: host_id
        description: Application Host ID
        type: integer
      - in: query
        name: name
        description: Filter metrics by name
        type: string
      - in: query
        name: page
        description: Pagination index (will be deprecated)
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Application
      - ""
      - Hosts
      - Host
      - ""
      - Metrics.
      - Format
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