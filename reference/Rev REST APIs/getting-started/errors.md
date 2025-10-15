---
title: Errors and Response Codes
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
The Rev API uses conventional HTTP errors and response codes to indicate the success or failure of an API request. 

A **2xx code** normally indicates a successful response. 

Codes in the **4xx code** range indicate a bad request such as an incorrect value for a <code>videoAccessControl</code> or incorrect <code>categoryId</code>.  This code can also indicate an unauthorized error if you do not have the correct permissions to perform the function you are attempting.

Codes in the **5xx code** range indicate an internal server error in processing your request.