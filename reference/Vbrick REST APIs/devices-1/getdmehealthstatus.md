---
title: Get DME Health Status
excerpt: >-
  This endpoint retrieves the last reported, complete health status of a DME.
  Each DME communicates a health status based on a frequency determined by
  Vbrick. Currently, this is every 60 seconds. Customers implementing
  longitudinal comparisons should periodically call this endpoint.
api:
  file: rev_v2_openapi.json
  operationId: getDmeHealthStatus
hidden: false
---