---
swagger: "2.0"
x-collection-name: GetStream.io
x-complete: 0
info:
  title: Stream API Retrieve feed followers - offset
  description: |-
    Retrieve a paginated list of the given feed's followers with a non-default offset to specify the number of follower feeds to skip in the response.

    # Parameters
     - offset: The number of follower feeds to offset
  version: 1.0.0
host: eu-central-api.stream-io-api.com
basePath: /api/v1.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /feed/user/eric:
    get:
      summary: Retrieve a feed - ID filters and pagination
      description: |-
        Retrieves the activities within a feed with ID filtering on the activities to be returned.

        See the [docs](https://getstream.io/docs_rest/#feed) for restrictions and recommendations on how to best make use of these parameters.
      operationId: FeedUserEricGet4
      x-api-path-slug: feedusereric-get
      parameters:
      - in: query
        name: api_key
      - in: query
        name: id_lt
      - in: header
        name: Stream-Auth-Type
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Feed
      - User
      - Eric
    post:
      summary: Add multiple activities
      description: |-
        Adds a set of activities to a feed.

        # Body fields
         - **activities**: An array of activity objects, each with at least the following mandatory fields:
           - **actor**: The actor performing the activity
           - **verb**: The verb of the activity
           - **object**: The object of the activity
      operationId: FeedUserEricPost8
      x-api-path-slug: feedusereric-post
      parameters:
      - in: query
        name: api_key
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: header
        name: Stream-Auth-Type
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Feed
      - User
      - Eric
  /feed/timeline/jessica/follows:
    post:
      summary: 1. Jessica's "timeline" follows Eric's "user" feed
      description: |-
        The Following endpoint can be used to add following relationships from a feed to another target feed.

        # Body fields:
         - **target**: The target feed this feed should follow
      operationId: FeedTimelineJessicaFollowsPost
      x-api-path-slug: feedtimelinejessicafollows-post
      parameters:
      - in: query
        name: api_key
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: header
        name: Stream-Auth-Type
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Feed
      - Timeline
      - Jessica
      - Follows
  /feed/timeline/jessica:
    get:
      summary: 3. Retrieve Jessica's "timeline" feed
      description: 'TODO: Add Description'
      operationId: FeedTimelineJessicaGet
      x-api-path-slug: feedtimelinejessica-get
      parameters:
      - in: query
        name: api_key
      - in: query
        name: limit
      - in: header
        name: Stream-Auth-Type
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Feed
      - Timeline
      - Jessica
  /feed/timeline_aggregated/jule/follows:
    post:
      summary: 1. Jule's "timeline_aggregated" feed follows Eric's "user" feed
      description: Let's setup an aggregated feed for Jule which follows Eric's updates.
        By default the aggregated feed will aggregate by verb and day. You can configure
        the aggregation rules in the dashboard.
      operationId: FeedTimelineAggregatedJuleFollowsPost
      x-api-path-slug: feedtimeline-aggregatedjulefollows-post
      parameters:
      - in: query
        name: api_key
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: header
        name: Stream-Auth-Type
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Feed
      - Timeline
      - Aggregated
      - Jule
      - Follows
  /feed/timeline_aggregated/jule:
    get:
      summary: 3. Retrieve Jule's "timeline_aggregated" feed
      description: 'TODO: Add Description'
      operationId: FeedTimelineAggregatedJuleGet
      x-api-path-slug: feedtimeline-aggregatedjule-get
      parameters:
      - in: query
        name: api_key
      - in: query
        name: limit
      - in: header
        name: Stream-Auth-Type
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Feed
      - Timeline
      - Aggregated
      - Jule
  /activities:
    post:
      summary: Update activities
      description: |-
        The Activities endpoint can be used to update activity data stored by Stream API.

        # Body fields:
         - **activities**: The array of activity objects to update
      operationId: ActivitiesPost
      x-api-path-slug: activities-post
      parameters:
      - in: query
        name: api_key
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: header
        name: Stream-Auth-Type
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Activities
  /feed/user/eric/{STREAM_ACTIVITY_ID}:
    delete:
      summary: Delete activity - Activity ID
      description: Deletes an activity from a feed.
      operationId: FeedUserEricBySTREAMACTIVITYIDDelete
      x-api-path-slug: feeduserericstream-activity-id-delete
      parameters:
      - in: query
        name: api_key
      - in: header
        name: Stream-Auth-Type
      - in: path
        name: STREAM_ACTIVITY_ID
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Feed
      - User
      - Eric
      - STREAM
      - ACTIVITY
      - ID
  /feed/user/eric/{STREAM_ACTIVITY_FOREIGN_ID}:
    delete:
      summary: Delete activity - Foreign ID
      description: Deletes an activity from a feed.
      operationId: FeedUserEricBySTREAMACTIVITYFOREIGNIDDelete
      x-api-path-slug: feeduserericstream-activity-foreign-id-delete
      parameters:
      - in: query
        name: api_key
      - in: query
        name: foreign_id
      - in: header
        name: Stream-Auth-Type
      - in: path
        name: STREAM_ACTIVITY_FOREIGN_ID
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Feed
      - User
      - Eric
      - STREAM
      - ACTIVITY
      - FOREIGN
      - ID
  /feed/user/jessica/followers:
    get:
      summary: Retrieve feed followers
      description: Retrieve a paginated list of the given feed's followers.
      operationId: FeedUserJessicaFollowersGet
      x-api-path-slug: feeduserjessicafollowers-get
      parameters:
      - in: query
        name: api_key
      - in: header
        name: Stream-Auth-Type
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Feed
      - User
      - Jessica
      - Followers
  /feed/user/eric/followers:
    get:
      summary: Retrieve feed followers - offset
      description: |-
        Retrieve a paginated list of the given feed's followers with a non-default offset to specify the number of follower feeds to skip in the response.

        # Parameters
         - offset: The number of follower feeds to offset
      operationId: FeedUserEricFollowersGet2
      x-api-path-slug: feeduserericfollowers-get
      parameters:
      - in: query
        name: api_key
      - in: query
        name: offset
      - in: header
        name: Stream-Auth-Type
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Feed
      - User
      - Eric
      - Followers
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