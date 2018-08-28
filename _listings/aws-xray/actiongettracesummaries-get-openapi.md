---
swagger: "2.0"
x-collection-name: AWS X-Ray
x-complete: 0
info:
  title: AWS X-Ray API Get Trace Summaries
  version: 1.0.0
  description: |-
    Retrieves IDs and metadata for traces available for a specified time frame using an
          optional filter.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=BatchGetTraces:
    get:
      summary: Batch Get Traces
      description: Retrieves a list of traces specified by ID.
      operationId: batchGetTraces
      x-api-path-slug: actionbatchgettraces-get
      parameters:
      - in: query
        name: NextToken
        description: Pagination token
        type: string
      - in: query
        name: TraceIds
        description: Specify the trace IDs of requests for which to retrieve segments
        type: string
      responses:
        200:
          description: OK
      tags:
      - Traces
  /?Action=GetTraceGraph:
    get:
      summary: Get Trace Graph
      description: Retrieves a service graph for one or more specific trace IDs.
      operationId: getTraceGraph
      x-api-path-slug: actiongettracegraph-get
      parameters:
      - in: query
        name: NextToken
        description: Pagination token
        type: string
      - in: query
        name: TraceIds
        description: Trace IDs of requests for which to generate a service graph
        type: string
      responses:
        200:
          description: OK
      tags:
      - Trace Graph
  /?Action=GetTraceSummaries:
    get:
      summary: Get Trace Summaries
      description: |-
        Retrieves IDs and metadata for traces available for a specified time frame using an
              optional filter.
      operationId: getTraceSummaries
      x-api-path-slug: actiongettracesummaries-get
      parameters:
      - in: query
        name: EndTime
        description: The end of the time frame for which to retrieve traces
        type: string
      - in: query
        name: FilterExpression
        description: Specify a filter expression to retrieve trace summaries for services
          or requests that      meet certain requirements
        type: string
      - in: query
        name: NextToken
        description: Specify the pagination token returned by a previous request to
          retrieve the next page      of results
        type: string
      - in: query
        name: Sampling
        description: Set to true to get summaries for only a subset of available      traces
        type: string
      - in: query
        name: StartTime
        description: The start of the time frame for which to retrieve traces
        type: string
      responses:
        200:
          description: OK
      tags:
      - Trace Summaries
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