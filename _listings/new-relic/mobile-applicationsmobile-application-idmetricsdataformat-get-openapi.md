---
swagger: "2.0"
x-collection-name: New Relic
x-complete: 0
info:
  title: New Relic Get Mobile Applications Mobile Application  Metrics Data. Format
  version: 1.0.0
  description: "This API endpoint returns a list of values for each of the requested
    metrics. The list of available metrics\ncan be returned using the Metric Name
    API endpoint.\n\nMetric data can be filtered by a number of parameters, including
    multiple names and values, and by time range.\nMetric names and values will be
    matched intelligently in the background.\n\nYou can also retrieve a summarized
    data point across the entire time range selected by using the summarize\nparameter.\n\nSee
    our documentation for a discussion on \noutput pagination,  time range \nrelated
    considerations, and for examples of requesting and using metric values."
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
  /applications/{application_id}/hosts/{host_id}/metrics/data.{format}:
    get:
      summary: Get Applications Application  Hosts Host  Metrics Data. Format
      description: "This API endpoint returns a list of values for each of the requested
        metrics. The list of available metrics\ncan be returned using the Metric Name
        API endpoint.\n\nMetric data can be filtered by a number of parameters, including
        multiple names and values, and by time range.\nMetric names and values will
        be matched intelligently in the background.\n\nYou can also retrieve a summarized
        data point across the entire time range selected by using the summarize\nparameter.\n\nSee
        our documentation for a discussion on \noutput pagination,  time range \nrelated
        considerations, and for examples of requesting and using metric values."
      operationId: getApplicationsApplicationHostsHostMetricsData.Format
      x-api-path-slug: applicationsapplication-idhostshost-idmetricsdataformat-get
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: query
        name: from
        description: Retrieve metrics after this time
        type: time
      - in: path
        name: host_id
        description: Application Host ID
        type: integer
      - in: query
        name: names
        description: Retrieve specific metrics by name
        type: array
      - in: query
        name: period
        description: Period of timeslices in seconds
        type: integer
      - in: query
        name: raw
        description: Return unformatted raw values
        type: boolean
      - in: query
        name: summarize
        description: Summarize the data
        type: boolean
      - in: query
        name: to
        description: Retrieve metrics before this time
        type: time
      - in: query
        name: values
        description: Retrieve specific metric values
        type: array
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
      - Metrics
      - Data.
      - Format
  /applications/{application_id}/instances.{format}:
    get:
      summary: Get Applications Application  Instances. Format
      description: "This API endpoint returns a \npaginated list of instances associated
        with the given application. The time range for summary data is the last 10
        minutes.\n\nApplication instances can be filtered by hostname, or the list
        of application instance IDs.\n\nSee our documentation for a discussion and
        examples of\nusing  filters \nand summary data output."
      operationId: getApplicationsApplicationInstances.Format
      x-api-path-slug: applicationsapplication-idinstancesformat-get
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
        description: Filter by application instance ids
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
      - Instances.
      - Format
  /applications/{application_id}/instances/{id}.{format}:
    get:
      summary: Get Applications Application  Instances  . Format
      description: |-
        This API endpoint returns a single application instance, identified by ID. The time range for summary data is the last 10 minutes.

        See our documentation for a discussion of
         summary data output.
      operationId: getApplicationsApplicationInstances.Format
      x-api-path-slug: applicationsapplication-idinstancesidformat-get
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: path
        name: id
        description: Application instance ID
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Application
      - ""
      - Instances
      - ""
      - .
      - Format
  /applications/{application_id}/instances/{instance_id}/metrics.{format}:
    get:
      summary: Get Applications Application  Instances Instance  Metrics. Format
      description: |-
        Return a list of known metrics and their value names for the given resource.

        See our documentation for a discussion
        on  output pagination
        and for examples of requesting and using metric values.
      operationId: getApplicationsApplicationInstancesInstanceMetrics.Format
      x-api-path-slug: applicationsapplication-idinstancesinstance-idmetricsformat-get
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
        name: instance_id
        description: Application Instance ID
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
      - Instances
      - Instance
      - ""
      - Metrics.
      - Format
  /applications/{application_id}/instances/{instance_id}/metrics/data.{format}:
    get:
      summary: Get Applications Application  Instances Instance  Metrics Data. Format
      description: "This API endpoint returns a list of values for each of the requested
        metrics. The list of available metrics\ncan be returned using the Metric Name
        API endpoint.\n\nMetric data can be filtered by a number of parameters, including
        multiple names and values, and by time range.\nMetric names and values will
        be matched intelligently in the background.\n\nYou can also retrieve a summarized
        data point across the entire time range selected by using the summarize\nparameter.\n\nSee
        our documentation for a discussion on \noutput pagination,  time range \nrelated
        considerations, and for examples of requesting and using metric values."
      operationId: getApplicationsApplicationInstancesInstanceMetricsData.Format
      x-api-path-slug: applicationsapplication-idinstancesinstance-idmetricsdataformat-get
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: query
        name: from
        description: Retrieve metrics after this time
        type: time
      - in: path
        name: instance_id
        description: Application Instance ID
        type: integer
      - in: query
        name: names
        description: Retrieve specific metrics by name
        type: array
      - in: query
        name: period
        description: Period of timeslices in seconds
        type: integer
      - in: query
        name: raw
        description: Return unformatted raw values
        type: boolean
      - in: query
        name: summarize
        description: Summarize the data
        type: boolean
      - in: query
        name: to
        description: Retrieve metrics before this time
        type: time
      - in: query
        name: values
        description: Retrieve specific metric values
        type: array
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Application
      - ""
      - Instances
      - Instance
      - ""
      - Metrics
      - Data.
      - Format
  /applications.{format}:
    get:
      summary: Get Applications. Format
      description: "This API endpoint returns a paginated\nlist of the Applications
        associated with your New Relic account. The time range for summary data is
        the last 10 minutes.\n\nApplications can be filtered by their name, hosts,
        the list of application IDs or the application language as\nreported by the
        agents.\n\nSee our documentation for a discussion and examples of\nusing  filters
        \nand summary data output."
      operationId: getApplications.Format
      x-api-path-slug: applicationsformat-get
      parameters:
      - in: query
        name: filter[host]
        description: Filter by application host
        type: string
      - in: query
        name: filter[ids]
        description: Filter by application ids
        type: list
      - in: query
        name: filter[language]
        description: Filter by application language
        type: string
      - in: query
        name: filter[name]
        description: Filter by application name
        type: string
      - in: query
        name: page
        description: Pagination index
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Applications.
      - Format
  /applications/{id}.{format}:
    get:
      summary: Get Applications  . Format
      description: |-
        This API endpoint returns a single Application, identified by ID. The time range for summary data is the last 10 minutes.

        See our documentation for a discussion of the
         summary data output.
      operationId: getApplications.Format
      x-api-path-slug: applicationsidformat-get
      parameters:
      - in: path
        name: id
        description: Application ID
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Applications
      - ""
      - .
      - Format
    put:
      summary: Put Applications  . Format
      description: |-
        This API endpoint allows you to update certain parameters of your application.

        The input is expected to be in JSON or XML format in the body parameter of the PUT request. The exact
        schema is defined below. Any extra parameters passed in the body will be ignored.

        See our documentation for a discussion and simple example of
         updating
        an application.
      operationId: putApplications.Format
      x-api-path-slug: applicationsidformat-put
      parameters:
      - in: body
        name: application
        description: Application schema
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: Application ID
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Applications
      - ""
      - .
      - Format
    delete:
      summary: Delete Applications  . Format
      description: |-
        This API endpoint deletes an application and all of its reported data.

        WARNING: Only applications that have stopped reporting can be deleted. This is an irreversible process
        which will delete all reported data for this application.
      operationId: deleteApplications.Format
      x-api-path-slug: applicationsidformat-delete
      parameters:
      - in: path
        name: id
        description: Application ID
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Applications
      - ""
      - .
      - Format
  /applications/{application_id}/metrics.{format}:
    get:
      summary: Get Applications Application  Metrics. Format
      description: |-
        Return a list of known metrics and their value names for the given resource.

        See our documentation for a discussion
        on  output pagination
        and for examples of requesting and using metric values.
      operationId: getApplicationsApplicationMetrics.Format
      x-api-path-slug: applicationsapplication-idmetricsformat-get
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: query
        name: cursor
        description: Cursor for next page (replacing page param)
        type: string
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
      - Metrics.
      - Format
  /applications/{application_id}/metrics/data.{format}:
    get:
      summary: Get Applications Application  Metrics Data. Format
      description: "This API endpoint returns a list of values for each of the requested
        metrics. The list of available metrics\ncan be returned using the Metric Name
        API endpoint.\n\nMetric data can be filtered by a number of parameters, including
        multiple names and values, and by time range.\nMetric names and values will
        be matched intelligently in the background.\n\nYou can also retrieve a summarized
        data point across the entire time range selected by using the summarize\nparameter.\n\nSee
        our documentation for a discussion on \noutput pagination,  time range \nrelated
        considerations, and for examples of requesting and using metric values."
      operationId: getApplicationsApplicationMetricsData.Format
      x-api-path-slug: applicationsapplication-idmetricsdataformat-get
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: query
        name: from
        description: Retrieve metrics after this time
        type: time
      - in: query
        name: names
        description: Retrieve specific metrics by name
        type: array
      - in: query
        name: period
        description: Period of timeslices in seconds
        type: integer
      - in: query
        name: raw
        description: Return unformatted raw values
        type: boolean
      - in: query
        name: summarize
        description: Summarize the data
        type: boolean
      - in: query
        name: to
        description: Retrieve metrics before this time
        type: time
      - in: query
        name: values
        description: Retrieve specific metric values
        type: array
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Application
      - ""
      - Metrics
      - Data.
      - Format
  /browser_applications.{format}:
    get:
      summary: Get Browser Applications. Format
      description: |-
        This API endpoint returns a list of the Browser Applications associated with your New Relic account.

        Browser Applications can be filtered by their name, or by the application IDs.
      operationId: getBrowserApplications.Format
      x-api-path-slug: browser-applicationsformat-get
      parameters:
      - in: query
        name: filter[ids]
        description: Filter by application ids
        type: list
      - in: query
        name: filter[name]
        description: Filter by application name
        type: string
      - in: query
        name: page
        description: Pagination index
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Browser
      - Applications.
      - Format
    post:
      summary: Add Browser Applications. Format
      description: This API endpoint allows you to create a standalone Browser Application.
      operationId: postBrowserApplications.Format
      x-api-path-slug: browser-applicationsformat-post
      parameters:
      - in: body
        name: browser_application
        description: Browser Application Schema
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Browser
      - Applications.
      - Format
  /mobile_applications.{format}:
    get:
      summary: Get Mobile Applications. Format
      description: |-
        This API endpoint returns a list of the Mobile Applications associated with your New Relic account.

        MobileApplications can be filtered by their name, or by the application IDs.
      operationId: getMobileApplications.Format
      x-api-path-slug: mobile-applicationsformat-get
      responses:
        200:
          description: OK
      tags:
      - Mobile
      - Applications.
      - Format
  /mobile_applications/{id}.{format}:
    get:
      summary: Get Mobile Applications  . Format
      description: This API endpoint returns a single Mobile Application, identified
        by ID. The time range for summary data is the last 30 minutes.
      operationId: getMobileApplications.Format
      x-api-path-slug: mobile-applicationsidformat-get
      parameters:
      - in: path
        name: id
        description: Mobile Application ID
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Mobile
      - Applications
      - ""
      - .
      - Format
  /mobile_applications/{mobile_application_id}/metrics.{format}:
    get:
      summary: Get Mobile Applications Mobile Application  Metrics. Format
      description: |-
        Return a list of known metrics and their value names for the given resource.

        See our documentation for a discussion
        on  output pagination
        and for examples of requesting and using metric values.
      operationId: getMobileApplicationsMobileApplicationMetrics.Format
      x-api-path-slug: mobile-applicationsmobile-application-idmetricsformat-get
      parameters:
      - in: query
        name: cursor
        description: Cursor for next page (replacing page param)
        type: string
      - in: path
        name: mobile_application_id
        description: Mobile application ID
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
      - Mobile
      - Applications
      - Mobile
      - Application
      - ""
      - Metrics.
      - Format
  /mobile_applications/{mobile_application_id}/metrics/data.{format}:
    get:
      summary: Get Mobile Applications Mobile Application  Metrics Data. Format
      description: "This API endpoint returns a list of values for each of the requested
        metrics. The list of available metrics\ncan be returned using the Metric Name
        API endpoint.\n\nMetric data can be filtered by a number of parameters, including
        multiple names and values, and by time range.\nMetric names and values will
        be matched intelligently in the background.\n\nYou can also retrieve a summarized
        data point across the entire time range selected by using the summarize\nparameter.\n\nSee
        our documentation for a discussion on \noutput pagination,  time range \nrelated
        considerations, and for examples of requesting and using metric values."
      operationId: getMobileApplicationsMobileApplicationMetricsData.Format
      x-api-path-slug: mobile-applicationsmobile-application-idmetricsdataformat-get
      parameters:
      - in: query
        name: from
        description: Retrieve metrics after this time
        type: time
      - in: path
        name: mobile_application_id
        description: Mobile application ID
        type: integer
      - in: query
        name: names
        description: Retrieve specific metrics by name
        type: array
      - in: query
        name: period
        description: Period of timeslices in seconds
        type: integer
      - in: query
        name: raw
        description: Return unformatted raw values
        type: boolean
      - in: query
        name: summarize
        description: Summarize the data
        type: boolean
      - in: query
        name: to
        description: Retrieve metrics before this time
        type: time
      - in: query
        name: values
        description: Retrieve specific metric values
        type: array
      responses:
        200:
          description: OK
      tags:
      - Mobile
      - Applications
      - Mobile
      - Application
      - ""
      - Metrics
      - Data.
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