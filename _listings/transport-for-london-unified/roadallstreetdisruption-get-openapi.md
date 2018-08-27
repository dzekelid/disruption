---
swagger: "2.0"
x-collection-name: Transport for London Unified
x-complete: 0
info:
  title: Transport for London Unified Road all  Street  Disruption
  description: Gets a list of disrupted streets. if no date filters are provided,
    current disruptions are returned..
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