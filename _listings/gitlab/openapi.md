swagger: "2.0"
x-collection-name: GitLab
x-complete: 1
info:
  title: API title
  version: 1.0.0
host: localhost:3000
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/projects/{id}/builds/{build_id}/trace:
    get:
      summary: Get Projects Builds Build Trace
      description: Get a trace of a specific build of a project
      operationId: getV3ProjectsIdBuildsBuildIdTrace
      x-api-path-slug: v3projectsidbuildsbuild-idtrace-get
      parameters:
      - in: path
        name: build_id
        description: The ID of a build
      - in: path
        name: id
        description: The ID of a project
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Builds
      - Build
      - Trace