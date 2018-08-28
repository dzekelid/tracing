swagger: "2.0"
x-collection-name: Coord
x-complete: 1
info:
  title: Users API
  description: the-users-api-allows-you-to-manage-user-data-on-the-coord-platform--sending-user-data-to-coordallows-you-to-perform-transactions-with-mobility-systems-like-renting-a-bike-parking-ina-parking-lot-or-booking-a-ridehail-trip-on-behalf-of-that-user-using-the-coord-platform-the-requirements-for-performing-a-transaction-for-a-given-user-vary-depending-on-the-systemyoure-connecting-with--some-systems-require-particular-data-about-a-user-in-order-for-thetransaction-to-take-place-and-some-systems-require-you-to-link-a-users-account--alltransactions-require-you-to-authenticate-the-user-using-a-jwt-every-coord-api-that-supports-transactions-has-an-endpoint-for-getting-information-aboutthat-apis-systems-along-with-what-you-need-to-provide-for-a-user-in-order-to-perform-atransaction-for-them--the-users-api-provides-tools-that-help-you-enable-users-to-performtransactions-as-well-as-tools-for-learning-about-the-transactions-that-a-user-can-alreadyperform-read-on-for-more-information-about-authenticating-users-linking-accounts-and-managing-userdata--authenticating-users-with-jwtsall-coord-api-endpoints-that-either-manipulate-data-or-perform-a-transaction-on-behalf-of-alogged-in-user-require-http-calls-to-include-an-authorization-bearer-jwt-token-so-thatthe-current-user-can-be-identified--all-endpoints-in-the-users-api-fall-into-this-categoryexcept-for-the-test-jwt-creation-endpoint-which-is-designed-to-allow-you-to-create-test-tokensfor-use-in-such-requests-for-information-on-how-to-create-nontest-user-authorization-tokensplease-contact-a-hrefmailtosalescoord-co-target-blanksalescoord-coaas-this-is-available-only-for-transaction-enabled-partners-see-post-v1userstestinguser-and-jwtreference0testjwtcreation-for-information-onhow-to-create-jwts-for-testing--linking-accountsmany-systems-require-you-to-link-a-user-in-order-to-perform-a-transaction--you-can-do-this-byredirecting-the-users-browser-or-webview-to-theget-v1userslink-accountreference0linkauseraccounttoenabletransactions-endpoint-this-will-allow-the-user-to-link-to-an-existing-account-with-that-system-if-they-have-one-orwill-create-a-new-one-for-them--if-you-call-this-endpoint-with-a-test-jwt-we-will-simulateaccount-linking-by-redirecting-the-user-to-a-demo-permission-page-you-can-also-simulate-linking-or-unlinking-test-users-accounts-serverside-by-calling-thepost-v1userstestingusercurrenttransactable-systemsreference0simulateaccountlinkingfortestingendpoint-remember-that-not-all-systems-are-transactable-and-not-all-transactable-systems-requireaccount-linking--getting-and-setting-user-infowe-automatically-ingest-user-information-like-email-addresses-and-names-from-the-jwtauthorization-token-you-send-us--information-about-a-users-vehicle-like-their-license-plateneeds-to-be-set-through-our-api--we-require-this-in-order-for-the-user-to-transact-with-certainparking-operators-you-can-call-get-v1usersusercurrentreference0getuserinfo-to-get-all-theinformation-we-have-about-a-user-including-the-fields-we-deduce-from-their-jwt-and-those-thatyou-have-already-set-through-our-api-you-can-call-v1usersusercurrentupdate-vehiclereference0updateuservehicle-toupdate-the-vehicle-thats-associated-with-a-users-account-
  version: 1.0.0
host: api.coord.co
basePath: /v1/users
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /gps_trace:
    post:
      summary: Get toll rates corresponding to a sequence of timestamped GPS locations
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
      operationId: get_cost_for_gps_trace
      x-api-path-slug: gps-trace-post
      parameters:
      - in: query
        name: access_key
        description: The API access key for the request
      - in: body
        name: body
        description: A sequence of timestamped GPS locations in chronological order
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Gps
      - Trace