---
title: Get Video Thumbnail Configuration
excerpt: >-
  The <a href=/reference/downloadthumbnailsheet>Get Video Thumbnail Sheet</a> is
  returned as a grid view when using this endpoint. Each thumbnail is indexed
  from left to right, then top to bottom.
api:
  file: rev-rest-apis.json
  operationId: getVideoThumbnailConfig
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
To calculate the index of a thumbnail, use the following equation:

```Text code
frameIndex = floor(scrubTime / spf)
```

Where:

* **frameIndex**: Index of the desired thumbnail (starting from 0) as it appears in the thumbnail sheet.
* **scrubTime**: The time in seconds of the desired frameIndex.
* **spf**: Seconds per Frame. 

This is returned in the thumbnail config.

Once the **frameIndex** is found, it can be used to find the **X** and **Y** coordinates that the thumbnail is located at within the grid, as well as the **scaling value** like so:

```javascript code
row = floor(frameIndex / verticalTiles)
column = frameIndex % verticalTiles
frameWidth = sheetWidth / horizontalTiles
frameHeight = sheetHeight / verticalTiles
scale = hostHeight / frameHeight
xOffset = column * frameWidth
yOffset = row * frameHeight
```

Where:

* **horizontalTiles**: Number of tiles in the rows of the thumbnail sheet grid (found in the config)
* **verticalTiles**: Number of tiles in the columns of the thumbnail sheet grid (found in the config)
* **sheetWidth**: Total width (in pixels) of the thumbnail sheet (found in the config)
* **sheetHeight**: Total height (in pixels) of the thumbnail sheet grid (found in the config)
* **hostHeight**: Height (in pixels) of the element that will contain the desired thumbnail.

Finally, the style for the **background** can be computed using:

```Text code
url(${thumbnailSheetsUri}) -${xOffset * scale}px -${yOffset * scale}px / ${sheetWidth * scale}px ${sheetHeight * scale}px`
```
