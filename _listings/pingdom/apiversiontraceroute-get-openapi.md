---
swagger: "2.0"
x-collection-name: Pingdom
x-complete: 0
info:
  title: Traceroute API Make A Traceroute
  description: Perform a traceroute to a specified target from a specified Pingdom
    probe.
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
host: api.pingdom.com
basePath: /
paths:
  ? |2-

        /api/{version}/traceroute
  : ? |2-

          get
    : summary: Make A Traceroute
      description: Perform a traceroute to a specified target from a specified Pingdom
        probe.
      operationId: make-a-traceroute
      x-api-path-slug: apiversiontraceroute-get
      parameters:
      - in: query
        name: host
        description: Target host
        type: <td>string</td>
      - in: query
        name: probeid
        description: Probe identifier
        type: <td>integer</td>
      responses:
        "":
          description: ""
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
      tags:
      - Traceroute
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