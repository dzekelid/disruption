---
swagger: "2.0"
x-collection-name: Public Transport Victoria Timetable
x-complete: 0
info:
  title: PTV Timetable API - Version 3 Get V3 Disruptions Disruption
  description: View a specific disruption.
  termsOfService: http://ptv.vic.gov.au/ptv-timetable-api/
  contact:
    name: Public Transport Victoria
    url: http://ptv.vic.gov.au/digital
  version: v3
host: timetableapi.ptv.vic.gov.au
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/disruptions/{disruption_id}:
    get:
      summary: Get V3 Disruptions Disruption
      description: View a specific disruption.
      operationId: Disruptions_GetDisruptionById
      x-api-path-slug: v3disruptionsdisruption-id-get
      parameters:
      - in: query
        name: devid
        description: Your developer id
      - in: path
        name: disruption_id
        description: Identifier of disruption; values returned by Disruptions API
          - /v3/disruptions OR /v3/disruptions/route/{route_id}
      - in: query
        name: signature
        description: Authentication signature for request
      - in: query
        name: token
        description: Please ignore
      responses:
        200:
          description: OK
      tags:
      - Disruptions
      - Disruption
      - Id
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