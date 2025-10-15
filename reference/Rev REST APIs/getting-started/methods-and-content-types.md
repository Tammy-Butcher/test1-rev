---
title: Using the API
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## Methods and Content Types

Rev APIs are RESTful. In REST, each resource is represented by a base URL like <code>/videos</code> and the HTTP methods <code>GET</code>, <code>POST</code>, <code>PUT</code> and <code>DELETE</code> are used to request data and perform actions on those resources.

For methods that accept request parameters the platform accepts either <code>application/json</code> or <code>multipart-formdata</code> content types and currently only supports returning data in <code>application/json</code> format. You \_must \_send the appropriate **Content-Type** header with each request.

## Making API Calls

All Rev APIs are accessed via HTTPS. The complete URL is based on your Rev portal URL and varies depending on the endpoint of the resource being accessed. 

For instance, you can access a user based on Rev User ID via a GET request to this URL: **https\://<span>YOUR_REV_PORTAL_URL/api/v2/users/:userId</span>**  

Make sure to replace <code>YOUR_REV_PORTAL_URL</code> with the URL to your own Rev portal.

Please make sure that you are familiar with the **authentication **and **authorization **approaches for Rev APIs.

## Expanding Objects

Some endpoints have objects that use an **Add **control for readability.  To view those parameters in this documentation, simply click the **Add **button to expand the object.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d65327d-addControl.png",
        "addControl.png",
        802
      ],
      "align": "center",
      "caption": "The Add button is used to expand and collapse some objects for easier visibility"
    }
  ]
}
[/block]