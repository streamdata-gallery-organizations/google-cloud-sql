---
swagger: "2.0"
x-collection-name: Google Cloud SQL
x-complete: 0
info:
  title: Google Cloud SQL API Get Projects Project Instances
  description: Lists instances under a given project in the alphabetical order of
    the instance name.
  contact:
    name: Google
    url: https://google.com
  version: v1beta4
host: www.googleapis.com
basePath: /sql/v1beta4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /flags:
    get:
      summary: Get Flags
      description: List all available database flags for Google Cloud SQL instances.
      operationId: sql.flags.list
      x-api-path-slug: flags-get
      parameters:
      - in: query
        name: databaseVersion
        description: Database version for flag retrieval
      responses:
        200:
          description: OK
      tags:
      - Flags
  /projects/{project}/instances:
    get:
      summary: Get Projects Project Instances
      description: Lists instances under a given project in the alphabetical order
        of the instance name.
      operationId: sql.instances.list
      x-api-path-slug: projectsprojectinstances-get
      parameters:
      - in: query
        name: filter
        description: A filter expression for filtering listed instances
      - in: query
        name: maxResults
        description: The maximum number of results to return per response
      - in: query
        name: pageToken
        description: A previously-returned page token representing part of the larger
          set of results to view
      - in: path
        name: project
        description: Project ID of the project for which to list Cloud SQL instances
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Project
      - Instances
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