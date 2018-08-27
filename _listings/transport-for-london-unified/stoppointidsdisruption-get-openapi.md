---
swagger: "2.0"
x-collection-name: Transport for London Unified
x-complete: 0
info:
  title: Transport for London Unified Stop Point s  Disruption
  description: Gets all disruptions for the specified stoppointid, plus disruptions
    for any child naptan records it may have..
  version: v1
host: api.tfl.gov.uk
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Line/Meta/DisruptionCategories:
    get:
      summary: Line  Meta  Disruption Categories
      description: Gets a list of valid disruption categories.
      operationId: Line_MetaDisruptionCategories
      x-api-path-slug: linemetadisruptioncategories-get
      responses:
        200:
          description: OK
      tags:
      - Line
      - ""
      - Meta
      - ""
      - Disruption
      - Categories
  /Line/Mode/{modes}/Disruption:
    get:
      summary: Line  Mode modes  Disruption
      description: Get disruptions for all lines of the given modes..
      operationId: Line_DisruptionByMode
      x-api-path-slug: linemodemodesdisruption-get
      parameters:
      - in: path
        name: modes
        description: A comma-separated list of modes e
      responses:
        200:
          description: OK
      tags:
      - Line
      - ""
      - Mode
      - Modes
      - ""
      - Disruption
  /Line/{ids}/Disruption:
    get:
      summary: Line s  Disruption
      description: Get disruptions for the given line ids.
      operationId: Line_Disruption
      x-api-path-slug: lineidsdisruption-get
      parameters:
      - in: path
        name: ids
        description: A comma-separated list of line ids e
      responses:
        200:
          description: OK
      tags:
      - Line
      - S
      - ""
      - Disruption
  /Road/all/Disruption/{disruptionIds}:
    get:
      summary: Road all  Disruption disruption Ids
      description: Gets a list of active disruptions filtered by disruption ids..
      operationId: Road_DisruptionById
      x-api-path-slug: roadalldisruptiondisruptionids-get
      parameters:
      - in: path
        name: disruptionIds
        description: Comma-separated list of disruption identifiers to filter by
      - in: query
        name: stripContent
        description: Optional, defaults to false
      responses:
        200:
          description: OK
      tags:
      - Road
      - ""
      - ""
      - Disruption
      - Disruption
      - Ids
  /Road/all/Street/Disruption:
    get:
      summary: Road all  Street  Disruption
      description: Gets a list of disrupted streets. if no date filters are provided,
        current disruptions are returned..
      operationId: Road_DisruptedStreets
      x-api-path-slug: roadallstreetdisruption-get
      parameters:
      - in: query
        name: endDate
        description: Optional, The end time to filter on
      - in: query
        name: startDate
        description: Optional, the start time to filter on
      responses:
        200:
          description: OK
      tags:
      - Road
      - ""
      - ""
      - Street
      - ""
      - Disruption
  /Road/{ids}/Disruption:
    get:
      summary: Road s  Disruption
      description: Get active disruptions, filtered by road ids.
      operationId: Road_Disruption
      x-api-path-slug: roadidsdisruption-get
      parameters:
      - in: query
        name: categories
        description: an optional list of category names to filter on (a valid list
          of categories can be obtained from the /Road/Meta/categories endpoint)
      - in: query
        name: closures
        description: Optional, defaults to true
      - in: path
        name: ids
        description: Comma-separated list of road identifiers e
      - in: query
        name: severities
        description: an optional list of Severity names to filter on (a valid list
          of severities can be obtained from the /Road/Meta/severities endpoint)
      - in: query
        name: stripContent
        description: Optional, defaults to false
      responses:
        200:
          description: OK
      tags:
      - Road
      - S
      - ""
      - Disruption
  /StopPoint/Mode/{modes}/Disruption:
    get:
      summary: Stop Point  Mode modes  Disruption
      description: Gets a distinct list of disrupted stop points for the given modes.
      operationId: StopPoint_DisruptionByMode
      x-api-path-slug: stoppointmodemodesdisruption-get
      parameters:
      - in: query
        name: includeRouteBlockedStops
      - in: path
        name: modes
        description: A comma-seperated list of modes e
      responses:
        200:
          description: OK
      tags:
      - Stop
      - Point
      - ""
      - Mode
      - Modes
      - ""
      - Disruption
  /StopPoint/{ids}/Disruption:
    get:
      summary: Stop Point s  Disruption
      description: Gets all disruptions for the specified stoppointid, plus disruptions
        for any child naptan records it may have..
      operationId: StopPoint_Disruption
      x-api-path-slug: stoppointidsdisruption-get
      parameters:
      - in: query
        name: flattenResponse
        description: Specify true to associate all disruptions with parent stop point
      - in: query
        name: getFamily
        description: Specify true to return disruptions for entire family, or false
          to return disruptions for just this stop point
      - in: path
        name: ids
        description: A comma-seperated list of stop point ids
      - in: query
        name: includeRouteBlockedStops
      responses:
        200:
          description: OK
      tags:
      - Stop
      - Point
      - S
      - ""
      - Disruption
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