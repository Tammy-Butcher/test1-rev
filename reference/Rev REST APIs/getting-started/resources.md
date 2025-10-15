---
title: Resources and Code
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
The Rev API uses the OpenAPI specification.  If you are unfamiliar with this, visit <a href="https://oai.github.io/Documentation/specification.html" target="_blank">The OpenAPI Initiative</a> for more information and details on how to use it. 

> 📘 Note
>
> View the [Rev OpenAPI specification](https://github.com/vbrick/sample-code/blob/main/openapi.json) on Github!

## GitHub Sample Code Snippets

We have provided some additional <a href="https://github.com/vbrick/sample-code" target="_blank">sample code</a> on GitHub and described each snippet below.

### Postman

A Postman collection that demonstrates logging in via Username / User API key as well as accessing some common API endpoints.

### nodejs

* **rev-client** - a Typescript wrapper around the Rev API
* **minimal-sample.js** - a minimal no-depenancy example of authenticating with Rev and then making an API request

### .Net

To try out oAuth using this application, replace the <code>TBD</code> parameters at the top of the <code>Program.cs</code> file with appropriate values from your Rev instance as following:

* **myRevServerURL**: Rev URL
* **myapiKey**: Name API key defined in Rev for use with oAuth
* **secret**: Value of “secret” specified in Rev for myapiKey
* **redirecturi**: Redirect URI specified in Rev for myapiKey
* **myUsername**: Username of the person who will log into Rev
* **myPassword**: Password of the person who will log into Rev
