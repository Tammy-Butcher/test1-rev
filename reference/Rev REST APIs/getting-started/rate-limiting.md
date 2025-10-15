---
title: Rate Limiting
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Rate limiting of the Rev public APIs applies to your Rev account. If an API method allows for 100 requests per rate limit window (minute), then it allows 100 requests per window across all the API calls for that HTTP Method.

## 1 Minute Window

Rate limits are divided into 1 minute intervals i.e. the defined rate limits are applicable in a window of 1 minute.

The window begins when an API call is received and it starts reducing the number of available API calls by 1 per request until it reaches the rate limit or the minute window is elapsed at which point Rev resets the bucket of allowed requests.

## Http Response Codes

When an application exceeds the rate limit for a given standard API endpoint, the API will return a HTTP **429 Too Many Requests** response code.

## Standard GET and POST Request Limits

|                | Rate Limit Per Minute | HTTP Methods             |
| :------------- | :-------------------- | :----------------------- |
| POST endpoints | 3600                  | POST, PUT, DELETE, PATCH |
| GET endpoints  | 24000                 | GET                      |
| HEAD endpoints | No Limit              | HEAD                     |
| OPTIONS        | No Limit              | OPTIONS                  |

### Applying Rate Limits

Consider the following scenario:

- There are 100 users making rev API calls. If in a particular minute, every user made 240 calls in first 30 seconds for total of (240\*100 = 24,000), they will reach the rate limit on the GETs (based on 24,000 GETs per minute). Rev will then return HTTP 429 error code for further requests for the next 30 seconds until rate limit is reset and more API calls can be processed.
- If a single user submits 24,000 API requests in 5 seconds, then no more API calls will be allowed for the next 55 seconds.
- Rate limits are not on a per-user basis, rather they are cumulative for all users. Therefore, if you’re using OAuth authentication to make API queries for multiple users at once then you may need to use a smaller limit in your code. Alternately, if you’re using a system-wide API user (or small number) for service automation then you may consider detecting 429 HTTP Responses, and retrying impacted requests after a sufficient delay.

## Rate Limits Per Endpoint

There are certain endpoints that have separate limits on rate limiting than the base limits specified above. Those are noted in the table below.

<!-- block:parameters -->
<div>
  <table>
    <thead>
      <tr>
        <th>Endpoint</th>
        <th>Rate Limit (Calls per Minute)</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><a href="ref:getvideosdetails">Get Video Details/Metadata</a></td>
        <td>2000</td>
      </tr>
      <tr>
        <td><a href="ref:searchvideo">Search Videos</a></td>
        <td>120</td>
      </tr>
      <tr>
        <td><a href="ref:audit">Audit Endpoints</a> (all Audit endpoints)</td>
        <td>60</td>
      </tr>
      <tr>
        <td><a href="ref:uploadvideo-1">Upload Video</a><br/><a href="ref:updatevideo">Update Video Metadata</a><br/><a href="ref:postvideoreport">Get Video Report</a><br/><a href="ref:deletevideo">Delete Video</a><br/><a href="ref:editvideopatch">(Patch) Partially Update Video Metadata</a></td>
        <td>30</td>
      </tr>
      <tr>
        <td><a href="ref:loginreport">Get Users By Login Date</a></td>
        <td>10</td>
      </tr>
      <tr>
        <td><a href="ref:getrealtimeattendeessearchrequest">Get Webcast Attendees Realtime</a></td>
        <td>2</td>
      </tr>
    </tbody>
  </table>
</div>
<!-- /block:parameters -->