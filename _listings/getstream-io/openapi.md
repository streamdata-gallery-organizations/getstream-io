---
swagger: "2.0"
x-collection-name: GetStream.io
x-complete: 1
info:
  title: Stream API
  description: -how-to-use-this-collection1--install-the-collection-done2--check-the-general-prerequisites-section-below-for-basic-setup-3--review-the-request-folders-and-select-a-request-to-send------review-the-request-description-to-check-for-any-required-parameters-andor-request-specific-prerequisites-4--run-the-request--general-prerequisites--create-an-app-at-stream--set-postman-environment-variables-for-connectivity-and-authentication-stream-app-location-stream-api-key-stream-api-secret-collection-overview--get-started-requests-used-in-streams-getting-started-tutorial---rest-api-endpoints-examples-of-the-documented-api-endpointshttpsgetstream-iodocs-rest-
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
  /feed/user/eric/follows:
    get:
      summary: Retrieve followed feeds - filter
      description: Retrieve a list of the feeds followed by this feed with a filter
        applied to the feeds that are returned.
      operationId: FeedUserEricFollowsGet4
      x-api-path-slug: feeduserericfollows-get
      parameters:
      - in: query
        name: api_key
      - in: query
        name: filter
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
      - Follows
    post:
      summary: Create a following relationship
      description: |-
        The Following endpoint can be used to add following relationships from a feed to another target feed.

        # Body fields:
         - **target**: The target feed this feed should follow
      operationId: FeedUserEricFollowsPost
      x-api-path-slug: feeduserericfollows-post
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
      - Follows
  /feed/user/eric/following/user:jessica:
    delete:
      summary: Delete following relationship
      description: Unfollows a feed by deleting the following relationship from the
        feed to the target feed.
      operationId: FeedUserEricFollowingUserJessicaDelete
      x-api-path-slug: feeduserericfollowinguserjessica-delete
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
      - Eric
      - Following
      - User:jessica
  /feed/add_to_many:
    post:
      summary: Add an Activity to multiple feeds
      description: |-
        Add an Activity to multiple feeds.

        # Body fields:
         - **feeds**: The list of feeds where the activity will be stored
         - **activity**: An activity object, with at least the following mandatory fields:
           - **actor**: The actor performing the activity
           - **verb**: The verb of the activity
           - **object**: The object of the activity
      operationId: FeedAddToManyPost
      x-api-path-slug: feedadd-to-many-post
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
      - Add
      - To
      - Many
  /follow_many:
    post:
      summary: Follow multiple feeds
      description: |-
        Add an Activity to multiple feeds.

        # Body fields:
         - An array of following relationships represented with source/target feeds
      operationId: FollowManyPost
      x-api-path-slug: follow-many-post
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
      - Follow
      - Many
---