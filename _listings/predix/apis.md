---
name: Predix
x-slug: predix
description: Predix (IoT PaaS) helps you develop apps that connect people with industrial
  machines through analytics and data for better business outcomes.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
x-kinRank: "7"
x-alexaRank: "264121"
tags: Applications
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apis.md
specificationVersion: "0.14"
apis:
- name: Access Control - Retrieves the resource for the given zone. The resourceIdentifier
    must be URL encoded in application/x-www-form-urlencoded format with UTF-8.
  x-api-slug: v1resourceresourceidentifier-get
  description: Retrieves the resource for the given zone. the resourceidentifier must
    be url encoded in application/x-www-form-urlencoded format with utf-8..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-acs.run.aws-usw02-pr.ice.predix.io//
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/v1resourceresourceidentifier-get-openapi.md
- name: Access Control - Creates/Updates a given resource for a given zone. The resourceIdentifier
    must be URL encoded in application/x-www-form-urlencoded format with UTF-8.
  x-api-slug: v1resourceresourceidentifier-put
  description: Creates/updates a given resource for a given zone. the resourceidentifier
    must be url encoded in application/x-www-form-urlencoded format with utf-8..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-acs.run.aws-usw02-pr.ice.predix.io//
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/v1resourceresourceidentifier-put-openapi.md
- name: Access Control - Deletes the resource for a given zone. The resourceIdentifier
    must be URL encoded in application/x-www-form-urlencoded format with UTF-8.
  x-api-slug: v1resourceresourceidentifier-delete
  description: Deletes the resource for a given zone. the resourceidentifier must
    be url encoded in application/x-www-form-urlencoded format with utf-8..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-acs.run.aws-usw02-pr.ice.predix.io//
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/v1resourceresourceidentifier-delete-openapi.md
- name: Access Control - Retrieves the subject for the given zone. The subjectIdentifier
    must be URL encoded in application/x-www-form-urlencoded format with UTF-8.
  x-api-slug: v1subjectsubjectidentifier-get
  description: Retrieves the subject for the given zone. the subjectidentifier must
    be url encoded in application/x-www-form-urlencoded format with utf-8..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-acs.run.aws-usw02-pr.ice.predix.io//
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/v1subjectsubjectidentifier-get-openapi.md
- name: Access Control - Deletes the subject for a given zone. The subjectIdentifier
    must be URL encoded in application/x-www-form-urlencoded format with UTF-8.
  x-api-slug: v1subjectsubjectidentifier-delete
  description: Deletes the subject for a given zone. the subjectidentifier must be
    url encoded in application/x-www-form-urlencoded format with utf-8..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-acs.run.aws-usw02-pr.ice.predix.io//
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/v1subjectsubjectidentifier-delete-openapi.md
- name: Predix AppHub ARCS - Get all the registered microapps
  x-api-slug: apps-get
  description: Get the registered microapps for the given tenant
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apps-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apps-get-openapi.md
- name: Predix AppHub ARCS - Register the microapp
  x-api-slug: apps-post
  description: Register the microapps
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apps-post-openapi.md
- name: Predix AppHub ARCS - Update the microapp
  x-api-slug: apps-put
  description: Update the microapps
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apps-put-openapi.md
- name: Predix AppHub ARCS - Get the registered microapp
  x-api-slug: appsuuid-get
  description: Get the registered microapp for the given uri
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/appsuuid-get-openapi.md
- name: Predix AppHub ARCS - Unregister the microapp
  x-api-slug: appsuuid-delete
  description: Unregister the microapp
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/appsuuid-delete-openapi.md
- name: Predix AppHub ARCS - Get all the registered microapps
  x-api-slug: apps-get
  description: Get the registered microapps for the given tenant
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apps-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apps-get-openapi.md
- name: Predix AppHub ARCS - Register the microapp
  x-api-slug: apps-post
  description: Register the microapps
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apps-post-openapi.md
- name: Predix AppHub ARCS - Update the microapp
  x-api-slug: apps-put
  description: Update the microapps
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apps-put-openapi.md
- name: Predix AppHub ARCS - Get the registered microapp
  x-api-slug: appsuuid-get
  description: Get the registered microapp for the given uri
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/appsuuid-get-openapi.md
- name: Predix AppHub ARCS - Unregister the microapp
  x-api-slug: appsuuid-delete
  description: Unregister the microapp
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/appsuuid-delete-openapi.md
- name: Predix AppHub ARCS - Unregister the microapp
  x-api-slug: appsuuid-delete
  description: Unregister the microapp
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/appsuuid-delete-openapi.md
- name: Predix AppHub ARCS - Get the registered microapp
  x-api-slug: appsuuid-get
  description: Get the registered microapp for the given uri
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/appsuuid-get-openapi.md
- name: Predix AppHub ARCS - Update the microapp
  x-api-slug: apps-put
  description: Update the microapps
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apps-put-openapi.md
- name: Predix AppHub ARCS - Register the microapp
  x-api-slug: apps-post
  description: Register the microapps
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apps-post-openapi.md
- name: Predix AppHub ARCS - Get all the registered microapps
  x-api-slug: apps-get
  description: Get the registered microapps for the given tenant
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/predix-vector-logo.png
  humanURL: https://www.predix.io
  baseURL: https://predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io//api
  tags: SaaS, Technology, Enterprise, Internet of Things, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apps-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/applications/master/_listings/predix/apps-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://predicthq.api.gallery.streamdata.io
- type: x-api-stack
  url: http://predix.stack.network
- type: x-crunchbase
  url: https://crunchbase.com/organization/predix
- type: x-documentation
  url: https://docs.predix.io/en-US/platform
- type: x-twitter
  url: https://twitter.com/Predix
- type: x-website
  url: https://www.predix.io
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---