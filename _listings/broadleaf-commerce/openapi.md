---
swagger: "2.0"
x-collection-name: Broadleaf Commerce
x-complete: 1
info:
  title: Broadleaf Commerce API
  description: the-default-broadleaf-commerce-apis
  version: 1.0.0
host: demo.broadleafcommerce.org
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /trace:
    get:
      summary: Get Trace
      description: Get trace.
      operationId: getTrace
      x-api-path-slug: trace-get
      responses:
        200:
          description: OK
      tags:
      - Trace
  /trace.json:
    get:
      summary: Get Trace
      description: Get trace.
      operationId: getTrace.json
      x-api-path-slug: trace-json-get
      responses:
        200:
          description: OK
      tags:
      - Trace
---