---
name: GetStream.io
x-slug: getstream-io
description: Scalable & Fast API for building social networks, activity feeds, news
  feeds and activity streams.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
x-kinRank: "6"
x-alexaRank: "127527"
tags: GetStream.io
created: "2018-08-30"
modified: "2018-08-30"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/apis.md
specificationVersion: "0.14"
apis:
- name: Stream API - Retrieve a feed - ID filters and pagination
  x-api-slug: feedusereric-get
  description: |-
    Retrieves the activities within a feed with ID filtering on the activities to be returned.

    See the [docs](https://getstream.io/docs_rest/#feed) for restrictions and recommendations on how to best make use of these parameters.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feedusereric-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feedusereric-get-openapi.md
- name: Stream API - Add multiple activities
  x-api-slug: feedusereric-post
  description: |-
    Adds a set of activities to a feed.

    # Body fields
     - **activities**: An array of activity objects, each with at least the following mandatory fields:
       - **actor**: The actor performing the activity
       - **verb**: The verb of the activity
       - **object**: The object of the activity
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feedusereric-post-openapi.md
- name: Stream API - 1. Jessica's "timeline" follows Eric's "user" feed
  x-api-slug: feedtimelinejessicafollows-post
  description: |-
    The Following endpoint can be used to add following relationships from a feed to another target feed.

    # Body fields:
     - **target**: The target feed this feed should follow
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feedtimelinejessicafollows-post-openapi.md
- name: Stream API - 3. Retrieve Jessica's "timeline" feed
  x-api-slug: feedtimelinejessica-get
  description: 'TODO: Add Description'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feedtimelinejessica-get-openapi.md
- name: Stream API - 1. Jule's "timeline_aggregated" feed follows Eric's "user" feed
  x-api-slug: feedtimeline-aggregatedjulefollows-post
  description: Let's setup an aggregated feed for Jule which follows Eric's updates.
    By default the aggregated feed will aggregate by verb and day. You can configure
    the aggregation rules in the dashboard.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feedtimeline-aggregatedjulefollows-post-openapi.md
- name: Stream API - 3. Retrieve Jule's "timeline_aggregated" feed
  x-api-slug: feedtimeline-aggregatedjule-get
  description: 'TODO: Add Description'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feedtimeline-aggregatedjule-get-openapi.md
- name: Stream API - Update activities
  x-api-slug: activities-post
  description: |-
    The Activities endpoint can be used to update activity data stored by Stream API.

    # Body fields:
     - **activities**: The array of activity objects to update
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/activities-post-openapi.md
- name: Stream API - Delete activity - Activity ID
  x-api-slug: feeduserericstream-activity-id-delete
  description: Deletes an activity from a feed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feeduserericstream-activity-id-delete-openapi.md
- name: Stream API - Delete activity - Foreign ID
  x-api-slug: feeduserericstream-activity-foreign-id-delete
  description: Deletes an activity from a feed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feeduserericstream-activity-foreign-id-delete-openapi.md
- name: Stream API - Retrieve feed followers
  x-api-slug: feeduserjessicafollowers-get
  description: Retrieve a paginated list of the given feed's followers.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feeduserjessicafollowers-get-openapi.md
- name: Stream API - Retrieve feed followers - offset
  x-api-slug: feeduserericfollowers-get
  description: |-
    Retrieve a paginated list of the given feed's followers with a non-default offset to specify the number of follower feeds to skip in the response.

    # Parameters
     - offset: The number of follower feeds to offset
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feeduserericfollowers-get-openapi.md
- name: Stream API - Retrieve followed feeds - filter
  x-api-slug: feeduserericfollows-get
  description: Retrieve a list of the feeds followed by this feed with a filter applied
    to the feeds that are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feeduserericfollows-get-openapi.md
- name: Stream API - Create a following relationship
  x-api-slug: feeduserericfollows-post
  description: |-
    The Following endpoint can be used to add following relationships from a feed to another target feed.

    # Body fields:
     - **target**: The target feed this feed should follow
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feeduserericfollows-post-openapi.md
- name: Stream API - Delete following relationship
  x-api-slug: feeduserericfollowinguserjessica-delete
  description: Unfollows a feed by deleting the following relationship from the feed
    to the target feed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feeduserericfollowinguserjessica-delete-openapi.md
- name: Stream API - Add an Activity to multiple feeds
  x-api-slug: feedadd-to-many-post
  description: |-
    Add an Activity to multiple feeds.

    # Body fields:
     - **feeds**: The list of feeds where the activity will be stored
     - **activity**: An activity object, with at least the following mandatory fields:
       - **actor**: The actor performing the activity
       - **verb**: The verb of the activity
       - **object**: The object of the activity
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/feedadd-to-many-post-openapi.md
- name: Stream API - Follow multiple feeds
  x-api-slug: follow-many-post
  description: |-
    Add an Activity to multiple feeds.

    # Body fields:
     - An array of following relationships represented with source/target feeds
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26600-getstream-io.jpg
  humanURL: https://getstream.io
  baseURL: https://eu-central-api.stream-io-api.com//api/v1.0
  tags: Mobile, SaaS, Real Time, Feeds, General Data, Service API, Relative StreamRank,
    Streams, Webhook Implementations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/getstream-io/master/_listings/getstream-io/follow-many-post-openapi.md
x-common:
- type: x-blog
  url: https://getstream.io/blog/
- type: x-blog-rss
  url: https://getstream.io/blog/feed/
- type: x-github
  url: https://github.com/GetStream
- type: x-api-gallery
  url: http://geneea.api.gallery.streamdata.io
- type: x-api-stack
  url: http://getstream.io.stack.network
- type: x-crunchbase
  url: https://crunchbase.com/organization/getstream-io
- type: x-documentation
  url: https://getstream.io/docs_rest/
- type: x-email
  url: sales@getstream.io
- type: x-email
  url: support@getstream.io
- type: x-pricing
  url: https://getstream.io/pricing/
- type: x-status
  url: http://status.getstream.io/
- type: x-twitter
  url: https://twitter.com/getstream_io
- type: x-webhook
  url: https://getstream.io/docs/#realtime-webhooks
- type: x-website
  url: https://getstream.io
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---