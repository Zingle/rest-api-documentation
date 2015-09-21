# Zingle REST API
## Overview

Zingle is a multi-channel communications platform that allows the sending, receiving and automating of conversations between a Business and a Customer. Zingle is typically interacted with by Businesses via a web browser to manage these conversations with their customers. The Zingle API provides functionality to developers to act on behalf of either the Business or the Customer. The Zingle iOS SDK provides mobile application developers an easy-to-use layer on top of the Zingle API.

## REST API

The Zingle REST API allows account holders to perform the most common functions they'd normally perform in their account dashboard using a web browser.  Using the API you can perform activities such as provisioning new service, cancelling existing service, managing contacts, changing service settings, sending and reading messages, and more.

## Authentication
Access to the API is granted by providing your username and password.

## API Versioning
The first part of the URI path specifies the API version you wish to access in the format `v{version_number}`. 

For example, version 1 of the API (most current) is accessible via:

```no-highlight
https://api.zingle.me/v1/
```

## HTTP requests
All API requests are made by sending a secure HTTPS request using one of the following methods, depending on the action being taken:

* `POST` Create a resource
* `PUT` Update a resource
* `GET` Get a resource or list of resources
* `DELETE` Delete a resource

For PUT and POST requests the body of your request may include a JSON payload, and the URI being requested may include a query string specifying additional filters or commands, all of which are outlined in the following sections.

## HTTP Responses
Each response will include a `status` object and `result` array.  The `status` object contains an HTTP status code, message, description, error message (if an error occurred) and info about the result. The `result` contains the result of a successful request.  For example, a request to the `/services/` resource might return this:

``` JSON
{
    "status": 
    {
        "text":           "OK"         
        "status_code":    200,         
        "description":    null,        
        "sort_field":     "last_name", 
        "sort_direction": "asc",       
        "page":           1,           
        "page_size":      10,          
        "total_pages":    1,           
        "total_records":  8,           
    },
    "result": 
    [
      {
        "id": "aff7bc93-6e28-4e70-8770-defa35cdfc1f",
        "display_name": "My test API service",
        "time_zone": "America/Los_Angeles",
        "created_at": 1429034365,
        "updated_at": 1439228868,
        "account": {
            "id": "2c89b706-47f2-471d-8e1b-4a180b448838",
            "display_name": "Developer Account",
            "term_months": 1,
            "current_term_start_date": 1433116800,
            "current_term_end_date": null,
            "created_at": 1380312314,
            "updated_at": 1438919580
        },
        "plan": {
            "id": "a0eb6d49-caa8-4bd2-ae15-acb529a2ca98",
            "code": "zingle_basic",
            "term_months": 1,
            "monthly_or_unit_price": 0,
            "setup_price": 0,
            "display_name": "Zingle Basic",
            "is_printer_plan": false
        },
        "channels": [
          {
              "id": "d9f91fdb-bbdb-442d-bbac-99fc76263654",
              "display_name": null,
              "value": "+17245551212",
              "formatted_value": "(724) 555-1212",
              "country": "US",
              "is_default_for_type": true,
              "channel_type": {
                  "id": "0e3d71ee-9518-4b9b-b95a-2ea251829887",
                  "type_class": "PhoneNumber",
                  "display_name": "Phone Number",
                  "inbound_notification_url": null,
                  "outbound_notification_url": null,
                  "allow_communications": true
              }
          }
        ],
        "channel_types": [
          {
              "id": "0e3d71ee-9518-4b9b-b95a-dea251829887",
              "type_class": "PhoneNumber",
              "display_name": "Phone Number",
              "inbound_notification_url": null,
              "outbound_notification_url": null,
              "allow_communications": true
          }
        ],
        "service_address": {
            "address": "123 Zingle Blvd.",
            "city": "San Diego",
            "state": "CA",
            "country": "US",
            "postal_code": "92129"
        },
        "customFieldValues": []
      },
      {
        "id": "17804413-2851-4f96-9c21-83ea65dcbeba",
        "display_name": "My other test API service",
        "time_zone": "America/Los_Angeles",
        "created_at": 1429033270,
        "updated_at": 1439228868,
        "account": {
            "id": "2c89b706-43f2-471d-8e1b-4a180b448838",
            "display_name": "Developer Account",
            "term_months": 1,
            "current_term_start_date": 1433116800,
            "current_term_end_date": null,
            "created_at": 1380312314,
            "updated_at": 1438919580
        },
        "plan": {
            "id": "a0eb6d49-caa8-4dd2-ae15-acb529a2ca98",
            "code": "zingle_basic",
            "term_months": 1,
            "monthly_or_unit_price": 0,
            "setup_price": 0,
            "display_name": "Zingle Basic",
            "is_printer_plan": false
        },
        "channels": [
          {
              "id": "1e5961c7-0e93-469a-8283-030fa18e1043",
              "display_name": null,
              "value": "+14025558184",
              "formatted_value": "(402) 555-8184",
              "country": "US",
              "is_default_for_type": true,
              "channel_type": {
                  "id": "0e3d71ee-9518-4b9b-c95a-dea251829887",
                  "type_class": "PhoneNumber",
                  "display_name": "Phone Number",
                  "inbound_notification_url": null,
                  "outbound_notification_url": null,
                  "allow_communications": true
              }
          }
        ],
        "channel_types": [
          {
              "id": "0e4d71ee-9518-4b9b-b95a-dea251829887",
              "type_class": "PhoneNumber",
              "display_name": "Phone Number",
              "inbound_notification_url": null,
              "outbound_notification_url": null,
              "allow_communications": true
          }
          {
              "id": "60c83850-5c7b-4400-a01a-d0153084e916",
              "type_class": "EmailAddress",
              "display_name": "Email Address",
              "inbound_notification_url": null,
              "outbound_notification_url": null,
              "allow_communications": true
          }
        ],
        "service_address": {
            "address": "456 Winston St.",
            "city": "San Diego",
            "state": "CA",
            "country": "US",
            "postal_code": "92129"
        },
        "customFieldValues": []
      }
    ]
  }
```

## HTTP Response Codes
Each response will be returned under one of the following HTTP response codes:

* `200` `OK` The request was successful
* `400` `Bad Request` There was a problem with the request (security, malformed, etc.)
* `403` `Forbidden` The credentials provided do not have permission to access the requested resource
* `404` `Not found` An attempt was made to access a resource that does not exist in the API
* `405` `Method not allowed` The resource being accessed doesn't support the method specified (GET, POST, etc.).
* `500` `Server Error` An error on the server occurred

## Request Modifiers
Request modifiers may be included in the request URI query string. The following modifiers are available throughout the API.  Other resource-specific modifiers are covered under the resource documentation that follows.
* `page` The page number in the result set to return (default 1)
* `page_size` The number of records to return per page (default 10, max 1000)
* `sort_field` field to sort the results by
* `sort_direction` asc (default) or desc


## Record Filtering
In addition to the request modifiers, record filters may also be specified in the query string.  Exactly which fields may be filtered and sorted on for each resource are covered in the sections below. A simple filter for services in California would look like this:

```no-highlight
https://api.zingle.me/v1/services?state=CA
```

Wildcards are also supported for some fields by using an asterisk in the filter. The following would return any services with phone numbers containing '619':

```no-highlight
https://api.zingle.me/v1/services?phone_number=*619*
```

Some values support range selection, such as dates, by using 'greater_than' and 'less_than' functions.  All messages sent from January 1, 2015 at 8:00AM to February 1, 2015 at 8:00AM could be retrieved with the following query:

```no-highlight
https://api.zingle.me/v1/service/1/messages?communication_direction=inbound&created_at=greater_than(1420099200000),less_than(1422777600000)
```

#### Note that all dates are in the form of Unix timestamps with milliseconds (milliseconds since January 1, 1970) and returned in GMT - you will have to account for time zone adjustment depending on your client's location.
