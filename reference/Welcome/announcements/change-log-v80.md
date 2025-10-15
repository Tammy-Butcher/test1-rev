---
title: Change Log (v8.0)
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
> 🚧 Important!
> 
> Per our [Rev v7.40 deprecation announcement](https://revdocs.vbrick.com/v7.40/reference/announcements), the **Rev v1 API** no longer functions as of this release. 
> 
> If you have not already done so, please begin using the Rev v2 API _immediately_. If you need assistance, contact [Vbrick Support](mailto:support@vbrick.com).

## :star2: **New**

### Capture Video Recording Support

Authorized users are now able to create [screen share and record videos](doc:screen-share-and-record) directly from the browser without the need to log-in to Rev's UI by passing a Vbrick access token through the [Capture Video](ref:capturevideo) URL.

## :wrench: **Updated/Fixed**

### Channel Hierarchy Support

The [Update Category](ref:editcategory) endpoint now provides an optional **parentCategoryId** parameter that allows you to manage channel hierarchy when used by an Account or Media admin. If the parentCategoryId is a different category, it creates a child category. If a blank string is passed, it is moved as a top-level category. If no value is passed, the value is not updated. Note that if you specify a category Id, it needs to exist in Rev.