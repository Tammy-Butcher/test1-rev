---
title: Upload Video Presentation Chapters
excerpt: >-
  This endpoint uploads a PowerPoint presentation to create chapters for a
  specified video. <p>Posting chapters replaces <em>all</em> existing chapters a
  video contains. The first slide begins at 00:00:00 with the rest evenly
  distributed throughout the duration of the video. The slide titles are the
  names of the chapter titles. If there are slides without titles, the slide
  number is the title. The endpoint requires the user have edit rights to the
  video.</p>
api:
  file: rev_v2_openapi.json
  operationId: uploadPresentationFile
hidden: false
---