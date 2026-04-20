---
title: Update Video Details/Metadata
excerpt: >-
  This endpoint is used to set or modify all metadata fields for a specific
  video. Note that if you are only changing one field (categories for example)
  <em>all</em> other metadata fields must also be submitted with this API call.
  Otherwise, those values that are not set are reset to defaults or nullified
  entirely.<p>To edit specific fields instead of all fields, use the [Patch
  Video Details/Metadata](/reference/editvideopatch) endpoint instead.</p>
api:
  file: rev_v2_openapi.json
  operationId: updateVideo
hidden: false
---