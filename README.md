# Zingle REST API

## Overview

Zingle is a multi-channel communications platform that allows the sending, receiving and automating of conversations between a Business and a Customer. Zingle is typically interacted with by Businesses via a web browser to manage these conversations with their customers. The Zingle API provides functionality to developers to act on behalf of either the Business or the Customer. The Zingle iOS SDK provides mobile application developers an easy-to-use layer on top of the Zingle API.

## Tutorial
We provide a [Postman](https://www.getpostman.com/) collection with a set of requests that introduce the basic concepts of the API.  You will need an existing Zingle account with API access to run this tutorial. The Postman collection and more information are available [here](https://github.com/Zingle/rest-api/tree/master/.postman_tutorial).

### Support
For API support, please email api.support@zingle.me.

## Authentication
Access to the API is granted by providing your username and password using HTTP basic authentication.  The username and password used, is the same username and password you use to access the Zingle web interface.

```no-highlight
GET https://api.zingle.me/v1/

{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "auth": {
        "id": "4c11f5e3-50b6-4995-b471-b8ef0015488d",
        "email": "joe@example.com",
        "first_name": "Joe",
        "last_name": "Smith",
        "title": null,
        "authorization_class": "contact"
    }
}
```

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
Each response will include a `status` object and (if successful) a `result` (`result` will be an object for single-record queries and an array for list queries).  The `status` object contains an HTTP `status_code`, `text`, `description`, `error_code` (if an error occurred - see [Error Codes]) and pagination info about the result. The `result` contains the result of a successful request.  For example, a request to the `/services/` resource might return this:

``` JSON
{
    "status": 
    {
        "text":           "OK",        
        "status_code":    200,         
        "description":    null,        
        "sort_field":     "display_name", 
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
              "id": "0e3d71ee-9518-4b9b-b9a5a-dea251829887",
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
      }
    ]
  }
```

## HTTP Response Codes
Each response will be returned with one of the following HTTP status codes:

* `200` `OK` The request was successful
* `400` `Bad Request` There was a problem with the request (security, malformed, data validation, etc.)
* `401` `Unauthorized` The supplied API credentials are invalid
* `403` `Forbidden` The credentials provided do not have permission to access the requested resource
* `404` `Not found` An attempt was made to access a resource that does not exist in the API
* `405` `Method not allowed` The resource being accessed doesn't support the method specified (GET, POST, etc.).
* `500` `Server Error` An error on the server occurred

## Request Modifiers
Request modifiers may be included in the request URI query string. The following modifiers are available throughout the API.  Other resource-specific modifiers are covered under the specific resource documentation sections.
* `page` The page number in the result set to return (default 1)
* `page_size` The number of records to return per page (default 10, max 1000)
* `sort_field` field to sort the results by
* `sort_direction` asc (default) or desc
* `sort_fields` Specify multiple fields to sort by seperated by commas.  Optionally append with a space and a direction e.g. "event_id asc"


## Record Filtering
In addition to the request modifiers, record filters may also be specified in the query string.  Exactly which fields may be filtered and sorted on for each resource are covered in the resource sections. A simple filter for services in California would look like this:

```no-highlight
https://api.zingle.me/v1/services?state=CA
```

Wildcards are also supported for some fields by using an asterisk in the filter. The following would return any services with display anmes containing 'foo':

```no-highlight
https://api.zingle.me/v1/services?display_name=*foo*
```

Some values, such as dates, support range selection by using 'greater_than' and 'less_than' functions.  All messages sent from January 1, 2015 at 8:00AM to February 1, 2015 at 8:00AM could be retrieved with the following query:

```no-highlight
https://api.zingle.me/v1/services/f762cdf9-6b0c-4563-a774-3e9d86f908f9/messages?communication_direction=inbound&created_at=greater_than(1420099200000),less_than(1422777600000)
```

#### Note that all dates are in the form of Unix timestamps (seconds since January 1, 1970) and returned in GMT - you will have to account for time zone adjustment depending on your client's location.

## Resources
For a description of the available resources see the [Resource Overview](resource_overview.md).

### General
- **[<code>GET</code> Time Zones list](/time_zones/GET_list.md)**
- **[<code>GET</code> Available Phone Numbers list](/available_phone_numbers/GET_list.md)**

### [Accounts][]
- **[<code>GET</code> Accounts list](/accounts/GET_list.md)**
- **[<code>GET</code> Account](/accounts/GET_id.md)**
- **[<code>GET</code> Account Plans list](/plans/GET_list.md)**
- **[<code>GET</code> Account Plan](/plans/GET_id.md)**

### [Services][]
- **[<code>GET</code> Services list](/services/GET_list.md)**
- **[<code>GET</code> Service](/services/GET_id.md)**
- **[<code>POST</code> Create Service](/services/POST_create.md)**
- **[<code>PUT</code> Update Service](/services/PUT_update_id.md)**
- **[<code>DELETE</code> Cancel Service](/services/DELETE_id.md)**
- **[<code>POST</code> Set Service Setting](/service_settings/POST_create.md)**


### [Channel Types][]
- **[<code>GET</code> Channel Type List](/channel_types/GET_list.md)**
- **[<code>GET</code> Channel Type](/channel_types/GET_id.md)**
- **[<code>POST</code> Create Channel Type](/channel_types/POST_create.md)**
- **[<code>PUT</code> Update Channel Type](/channel_types/PUT_update_id.md)**
- **[<code>DELETE</code> Delete Channel Type](/channel_types/DELETE_id.md)**

### [Service Channels][]
- **[<code>GET</code> Service Channel](/service_channels/GET_id.md)**
- **[<code>POST</code> Create Service Channel](/service_channels/POST_create.md)**
- **[<code>PUT</code> Update Service Channel](/service_channels/PUT_update_id.md)**
- **[<code>DELETE</code> Delete Service Channel](/service_channels/DELETE_id.md)**

### [Contacts][]
- **[<code>GET</code> Contact list](/contacts/GET_list.md)**
- **[<code>GET</code> Contact](/contacts/GET_id.md)**
- **[<code>POST</code> Create Contact](/contacts/POST_create.md)**
- **[<code>PUT</code> Update Contact](/contacts/PUT_update_id.md)**
- **[<code>DELETE</code> Delete Contact](/contacts/DELETE_id.md)**
- **[<code>POST</code> Set Contact Custom Field Value](/custom_field_values/POST_create_id.md)** 
- **[<code>POST</code> Trigger automation for Contact](/contacts/POST_trigger_automation_id.md)** 
- **[<code>POST</code> Attach Label to Contact](/contacts/POST_attach_label_id.md)** 
- **[<code>DELETE</code> Detach Label from Contact](/contacts/DELETE_detach_label_id.md)** 

### [Contact Channels][]
- **[<code>GET</code> Contact Channel](/contact_channels/GET_id.md)**
- **[<code>POST</code> Create Contact Channel](/contact_channels/POST_create.md)**
- **[<code>PUT</code> Update Contact Channel](/contact_channels/PUT_update_id.md)**
- **[<code>DELETE</code> Delete Contact Channel](/contact_channels/DELETE_id.md)**

### [Messages][]
- **[<code>GET</code> Message List](/messages/GET_list.md)**
- **[<code>GET</code> Message](/messages/GET_id.md)**
- **[<code>POST</code> Send Message](/messages/POST_create.md)**
- **[<code>POST</code> Set Message 'Read' Status](/messages/POST_read_id.md)**

### [Contact Custom Fields][]
- **[<code>GET</code> Contact Field list](/contact_custom_fields/GET_list.md)**
- **[<code>GET</code> Contact Field](/contact_custom_fields/GET_id.md)**
- **[<code>POST</code> Create Contact Field](/contact_custom_fields/POST_create.md)**
- **[<code>PUT</code> Update Contact Field](/contact_custom_fields/PUT_update_id.md)**
- **[<code>DELETE</code> Delete Contact Field](/contact_custom_fields/DELETE_id.md)** 

### [Labels][]
- **[<code>GET</code> Label list](/labels/GET_list.md)**
- **[<code>GET</code> Label](/labels/GET_id.md)**
- **[<code>POST</code> Create Label](/labels/POST_create.md)**
- **[<code>PUT</code> Update Label](/labels/PUT_update_id.md)**
- **[<code>DELETE</code> Delete Label](/labels/DELETE_id.md)**

### [Templates][]
- **[<code>GET</code> Template list](/templates/GET_list.md)**
- **[<code>GET</code> Template](/templates/GET_id.md)**
- **[<code>POST</code> Create Template](/templates/POST_create.md)**
- **[<code>PUT</code> Update Template](/templates/PUT_update_id.md)**
- **[<code>DELETE</code> Delete Template](/templates/DELETE_id.md)** 

### [Automations][]
- **[<code>GET</code> Automation list](/automations/GET_list.md)**
- **[<code>GET</code> Automation](/automations/GET_id.md)**
- **[<code>PUT</code> Update Automation](/automations/PUT_update_id.md)**

[Accounts]: /accounts/
[Services]: /services/
[Channel Types]: /channel-types
[Service Channels]: /service_channels
[Contacts]: /contacts
[Contact Channels]: /contact_channels
[Messages]: /messages
[Contact Custom Fields]: /contact_custom_fields
[Labels]: /labels
[Templates]: /templates
[Automations]: /automations
[Error Codes]: /error_codes.md
