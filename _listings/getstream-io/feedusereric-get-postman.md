{
  "info": {
    "name": "Stream API Retrieve a feed - ID filters and pagination",
    "_postman_id": "796028b9-0413-43d2-b15b-56cfb61f0903",
    "description": "Retrieves the activities within a feed with ID filtering on the activities to be returned.\n\nSee the [docs](https://getstream.io/docs_rest/#feed) for restrictions and recommendations on how to best make use of these parameters.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Feed",
      "item": [
        {
          "id": "d50e3995-6abc-4956-948c-1b1c90b9563f",
          "name": "FeedUserEricGet4",
          "request": {
            "url": "http://eu-central-api.stream-io-api.com/api/v1.0/feed/user/eric?api_key=%7B%7D&id_lt=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Stream-Auth-Type",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "User-Agent",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the activities within a feed with ID filtering on the activities to be returned.\n\nSee the [docs](https://getstream.io/docs_rest/#feed) for restrictions and recommendations on how to best make use of these parameters."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ac09446c-9c14-4d1a-a5eb-26f92e9fced5"
            }
          ]
        }
      ]
    }
  ]
}