---
name: Coord
x-slug: coord
description: Coord is a mobility company that creates seamless mobility and self-driving
  experiences today through deep integrations. The company offers bike-share API,
  Curbs API, Tolls API, Routing API and etc.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
x-kinRank: "7"
x-alexaRank: "1035226"
tags: Tracing
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/tracing/master/_listings/coord/apis.md
specificationVersion: "0.14"
apis:
- name: Tolls API - Get toll rates corresponding to a sequence of timestamped GPS
    locations
  x-api-slug: gps-trace-post
  description: |-
    Returns information about the toll cost of a route given the GPS trace along the route.

    Below is an example of a request:
    ```json
    {
      "locations": [
        {
          "timestamp": "2017-07-28T17:39:00.000Z",
          "lat": 47.28348,
          "lng": -122.56066
        },
        {
          "timestamp": "2017-07-28T17:39:30.000Z",
          "lat": 47.28154,
          "lng": -122.56069
        },
        {
          "timestamp": "2017-07-28T17:40:00.000Z",
          "lat": 47.28000,
          "lng": -122.56075
        },
        {
          "timestamp": "2017-07-28T17:40:30.000Z",
          "lat": 47.27901,
          "lng": -122.56081
        },
        {
          "timestamp": "2017-07-28T17:41:00.000Z",
          "lat": 47.27900,
          "lng": -122.56081
        },
        {
          "timestamp": "2017-07-28T17:41:30.000Z",
          "lat": 47.27831,
          "lng": -122.56082
        },
        {
          "timestamp": "2017-07-28T17:42:00.000Z",
          "lat": 47.27823,
          "lng": -122.56082
        },
        {
          "timestamp": "2017-07-28T17:42:30.000Z",
          "lat": 47.27798,
          "lng": -122.56082
        }
      ],
      "vehicle": {
        "axles": 2
      }
    }
    ```

    The order of the `coordinates` and `timestamps` matters. Also, `coordinates` are
    one-to-one mapped to `timestamps`. The response would look like:
      ```json
      [
        {
          "checkpoints": [
              {
                  "end": {
                      "lat": 42.348327,
                      "lng": -71.103810
                  },
                  "start": {
                      "lat": 42.348411,
                      "lng": -71.104341
                  }
              }
          ],
          "estimated_cross_time": "2014-11-06T17:08:36.000Z",
          "id": 1467,
          "name": "Allston (EB)",
          "prices": [...],
          "roadway_name": "Massachusetts Turnpike"
        }
      ]
      ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/search/tolling
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/tracing/master/_listings/coord/gps-trace-post-openapi.md
- name: Tolls API - Get toll rates corresponding to a sequence of timestamped GPS
    locations
  x-api-slug: gps-trace-post
  description: |-
    Returns information about the toll cost of a route given the GPS trace along the route.

    Below is an example of a request:
    ```json
    {
      "locations": [
        {
          "timestamp": "2017-07-28T17:39:00.000Z",
          "lat": 47.28348,
          "lng": -122.56066
        },
        {
          "timestamp": "2017-07-28T17:39:30.000Z",
          "lat": 47.28154,
          "lng": -122.56069
        },
        {
          "timestamp": "2017-07-28T17:40:00.000Z",
          "lat": 47.28000,
          "lng": -122.56075
        },
        {
          "timestamp": "2017-07-28T17:40:30.000Z",
          "lat": 47.27901,
          "lng": -122.56081
        },
        {
          "timestamp": "2017-07-28T17:41:00.000Z",
          "lat": 47.27900,
          "lng": -122.56081
        },
        {
          "timestamp": "2017-07-28T17:41:30.000Z",
          "lat": 47.27831,
          "lng": -122.56082
        },
        {
          "timestamp": "2017-07-28T17:42:00.000Z",
          "lat": 47.27823,
          "lng": -122.56082
        },
        {
          "timestamp": "2017-07-28T17:42:30.000Z",
          "lat": 47.27798,
          "lng": -122.56082
        }
      ],
      "vehicle": {
        "axles": 2
      }
    }
    ```

    The order of the `coordinates` and `timestamps` matters. Also, `coordinates` are
    one-to-one mapped to `timestamps`. The response would look like:
      ```json
      [
        {
          "checkpoints": [
              {
                  "end": {
                      "lat": 42.348327,
                      "lng": -71.103810
                  },
                  "start": {
                      "lat": 42.348411,
                      "lng": -71.104341
                  }
              }
          ],
          "estimated_cross_time": "2014-11-06T17:08:36.000Z",
          "id": 1467,
          "name": "Allston (EB)",
          "prices": [...],
          "roadway_name": "Massachusetts Turnpike"
        }
      ]
      ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/search/tolling
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/tracing/master/_listings/coord/gps-trace-post-openapi.md
- name: Tolls API - Get toll rates corresponding to a sequence of timestamped GPS
    locations
  x-api-slug: gps-trace-post
  description: |-
    Returns information about the toll cost of a route given the GPS trace along the route.

    Below is an example of a request:
    ```json
    {
      "locations": [
        {
          "timestamp": "2017-07-28T17:39:00.000Z",
          "lat": 47.28348,
          "lng": -122.56066
        },
        {
          "timestamp": "2017-07-28T17:39:30.000Z",
          "lat": 47.28154,
          "lng": -122.56069
        },
        {
          "timestamp": "2017-07-28T17:40:00.000Z",
          "lat": 47.28000,
          "lng": -122.56075
        },
        {
          "timestamp": "2017-07-28T17:40:30.000Z",
          "lat": 47.27901,
          "lng": -122.56081
        },
        {
          "timestamp": "2017-07-28T17:41:00.000Z",
          "lat": 47.27900,
          "lng": -122.56081
        },
        {
          "timestamp": "2017-07-28T17:41:30.000Z",
          "lat": 47.27831,
          "lng": -122.56082
        },
        {
          "timestamp": "2017-07-28T17:42:00.000Z",
          "lat": 47.27823,
          "lng": -122.56082
        },
        {
          "timestamp": "2017-07-28T17:42:30.000Z",
          "lat": 47.27798,
          "lng": -122.56082
        }
      ],
      "vehicle": {
        "axles": 2
      }
    }
    ```

    The order of the `coordinates` and `timestamps` matters. Also, `coordinates` are
    one-to-one mapped to `timestamps`. The response would look like:
      ```json
      [
        {
          "checkpoints": [
              {
                  "end": {
                      "lat": 42.348327,
                      "lng": -71.103810
                  },
                  "start": {
                      "lat": 42.348411,
                      "lng": -71.104341
                  }
              }
          ],
          "estimated_cross_time": "2014-11-06T17:08:36.000Z",
          "id": 1467,
          "name": "Allston (EB)",
          "prices": [...],
          "roadway_name": "Massachusetts Turnpike"
        }
      ]
      ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/search/tolling
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/tracing/master/_listings/coord/gps-trace-post-openapi.md
x-common:
- type: x-blog
  url: https://medium.com/coord
- type: x-blog-rss
  url: https://medium.com/feed/coord
- type: x-openapi
  url: https://jsapi.apiary.io/apis/coordprodsearchtolls.source
- type: x-api-gallery
  url: http://convertapi.api.gallery.streamdata.io
- type: x-api-stack
  url: http://coord.stack.network
- type: x-developer
  url: https://coord.co/docs/
- type: x-pricing
  url: https://coord.co/#pricing
- type: x-twitter
  url: https://twitter.com/coordcity
- type: x-website
  url: https://coord.co
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---