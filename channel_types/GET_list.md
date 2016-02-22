# Channel Type List

    GET services/:service_id/channel-types
    
Returns a list of [Channel Types]  belonging to the specified service

## Parameters
### URI Parameters
Field | Wildcards | Description
--- | --- | ---
Pagination options | N | (see [Overview - Request Modifiers][])
### Sortable fields
* type_class
* display_name

## Example
### Request

    GET https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/channel-types

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null,
        "sort_field": "id",
        "sort_direction": "asc",
        "page": 1,
        "page_size": 10,
        "total_pages": 1,
        "total_records": 4
    },
    "result": [
        {
            "id": "0e3d71ee-9518-4b9b-b95a-dea251829887",
            "type_class": "PhoneNumber",
            "display_name": "Phone Number",
            "inbound_notification_url": null,
            "outbound_notification_url": null,
            "allow_messages": true,
            "priority": 0,
            "is_global": true
        },
        {
            "id": "0e3d71ee-9518-4b9b-b95a-dea251829887",
            "type_class": "EmailAddress",
            "display_name": "Email Address",
            "inbound_notification_url": null,
            "outbound_notification_url": null,
            "allow_messages": true,
            "priority": 1,
            "is_global": true
        },    
        {
            "id": "0e3d71ee-9518-4b9b-b95a-dea251829887",
            "type_class": "UserDefinedChannel",
            "display_name": "Chat ID",
            "inbound_notification_url": null,
            "outbound_notification_url": null,
            "allow_messages": true,
            "priority": 2,
            "is_global": false
        }
    ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Channel Types]: README.md
