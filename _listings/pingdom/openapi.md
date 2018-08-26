---
swagger: "2.0"
x-collection-name: Pingdom
x-complete: 1
info:
  title: Traceroute API
  description: the-traceroute-api-
  version: 1.0.0
host: api.pingdom.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
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
---