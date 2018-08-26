---
swagger: "2.0"
x-collection-name: AWS X-Ray
x-complete: 1
info:
  title: AWS X-Ray API
  version: 1.0.0
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
  /?Action=PutTraceSegments:
    get:
      summary: Put Trace Segments
      description: Uploads segment documents to AWS X-Ray.
      operationId: putTraceSegments
      x-api-path-slug: actionputtracesegments-get
      parameters:
      - in: query
        name: TraceSegmentDocuments
        description: A JSON document defining one or more segments or subsegments
        type: string
      responses:
        200:
          description: OK
      tags:
      - Trace Segments
---