---
title: Reveknew - API Documentation

language_tabs: # must be one of https://git.io/vQNgJ
  - Example Value | Model
  

  


toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>


search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the  Reveknew-API
---

# Introduction

# customer-resource

## Create a customer record under a business account

```json
[
  {
    "customerNum" : "string",
    "email" : "string",
    "firstName" : "string",
    "id" : "string",
    "lastName" : "string",
    "phoneNo" : "string"
  }
]
```

This endpoint creates a customer record under a business account

### HTTP Request

POST  /enterprise/v1/customers/{businessId}

### Query Parameters

Parameter | Description
---------  | -----------
businessId *required| businessId
string                        |
(path)                        |
                                  |
customer*required   | customer
(body)                       |

### Responses

Code         |                   Description
-----------  |  ----------------------------------------------------------------------------
200 | Customer record created successfully 
      | Example  /Model
      | {
      |  "body" : {},
      | "statusCode" : "100 CONTINUE" ,
      | "statusCodeValue" : 0
      | }
201 | Created
       |
400 | Invalid data supplied for creation of customer 
       |
401 | Unauthorized
       |
403 | Operation not permitted for this business
        |
404 | Invalid businessId supplied      



## Update a Customer record under a business account

```json
[
  {
    "customerNum" : "string",
    "email" : "string",
    "firstName" : "string",
    "id" : "string",
    "lastName" : "string",
    "phoneNo" : "string"
  }
]
```

This endpoint updates a customer record under a business account

### HTTP Request

PUT  /enterprise/v1/customers/{businessId}

### Query Parameters

Parameter | Description
---------  | -----------
businessId *required| businessId
string                        |
(path)                        |
                                  |
customer*required   | customer
(body)                       |

### Responses

Code         |                   Description
-----------  |  ----------------------------------------------------------------------------
200 | Customer record updated successfully 
      | Example  /Model
      | {
      |  "body" : {},
      | "statusCode" : "100 CONTINUE" ,
      | "statusCodeValue" : 0
      | }
201 | Created
       |
400 | Invalid data supplied for update of customer record
       |
401 | Unauthorized
       |
403 | Operation not permitted for this business
        |
404 | Invalid businessId supplied    

## Find customer record by its id
This endpoint finds  customer record by its id 

### HTTP Request

GET /enterprise/v1/customers/{businessId}/id/{customerId}

### Query Parameters

Parameter | Description
---------  | -----------
businessId *required| businessId
string                        |
(path)                        |
                                  |
customer*required   | customer
(body)                       |

### Responses

Code         |                   Description
-----------  |  ----------------------------------------------------------------------------
200 | Customer record found successfully 
      | Example  /Model
      | {
      |  "body" : {},
      | "statusCode" : "100 CONTINUE" ,
      | "statusCodeValue" : 0
      | }
       |
401 | Unauthorized
       |
403 | Operation not permitted for this business
        |
404 | Invalid businessId supplied    