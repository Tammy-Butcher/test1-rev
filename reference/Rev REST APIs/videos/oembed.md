---
title: Get Video oEmbed
excerpt: >-
  Gets oEmbed JSON data for a given video for video embedding. This is typically
  used for integrations into other social systems with activity feeds so users
  can watch video inline of an activity feed. The Rev Shared URL is also an
  acceptable format as noted in the example(s) below.<p>This API does not
  require an authorization header.</p>
api:
  file: rev-rest-apis.json
  operationId: oembed
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
**Example Url Query Params **

Url example(s):
[block:code]
{
  "codes": [
    {
      "code": "https://myRevURL.vbrick.com/#/videos/5e0625da-d2a0-45d7-a221-deb49b9623ab",
      "language": "http",
      "name": "url"
    }
  ]
}
[/block]

[block:code]
{
  "codes": [
    {
      "code": "https%3A%2F%2FmyRevURL.vbrick.com%2F%23%2Fvideos%2F5e0625da-d2a0-45d7-a221-deb49b9623ab",
      "language": "http",
      "name": "encoded url"
    }
  ]
}
[/block]
Shared and encoded url example(s):
[block:code]
{
  "codes": [
    {
      "code": "https://myRevURL.vbrick.com/sharevideo/5e0625da-d2a0-45d7-a221-deb49b9623ab",
      "language": "http",
      "name": "shared url"
    }
  ]
}
[/block]

[block:code]
{
  "codes": [
    {
      "code": "https%3A%2F%2FmyRevURL.vbrick.com%2Fsharevideo%2F5e0625da-d2a0-45d7-a221-deb49b9623ab",
      "language": "http",
      "name": "encoded shared url"
    }
  ]
}
[/block]