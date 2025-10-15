---
title: Pagination
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
When using certain search endpoints and when several pages of results are returned, a <code>scrollId</code> parameter is returned in the first search request along with the first page of the results. 

This <code>scrollId</code>can then be passed in subsequent requests to get the next page of results. This <code>scrollId</code>parameter is forward only and you cannot get back the search results that are scrolled once.

> 🚧 Important!
>
> There is a 60 second inactivity timeout on the scroll that is renewed each time a page request is made. If not used within 60 seconds of the last call, the search query results expire. 
>
> Response payload for the search request for each page includes a <code>StatusCode</code> field. If the scroll times out, this <code>StatusCode</code> field will output 404 but the HTTP status code of the API is still 200 OK.
