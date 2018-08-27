---
swagger: "2.0"
x-collection-name: Public Transport Victoria Timetable
x-complete: 1
info:
  title: Public Transport Victoria Timetable
  description: the-ptv-timetable-api-provides-direct-access-to-public-transport-victorias-public-transport-timetable-data--the-api-returns-scheduled-timetable-route-and-stop-data-for-all-metropolitan-and-regional-train-tram-and-bus-services-in-victoria-including-night-networknight-train-and-night-tram-data-are-included-in-metropolitan-train-and-tram-services-data-respectively-whereas-night-bus-is-a-separate-route-type--the-api-also-returns-realtime-data-for-metropolitan-train-tram-and-bus-services-where-this-data-is-made-available-to-ptv-as-well-as-disruption-information-stop-facility-information-and-access-to-myki-ticket-outlet-data-
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
---