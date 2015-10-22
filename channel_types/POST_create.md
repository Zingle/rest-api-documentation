# Create Channel Type

    POST services/:service_id/channel-types
    
Creates a [Channel Type]

## Parameters
## Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
display_name | string | Y | 
inbound_notification_url | string | N | URL to call whenever an inbound message is created using this Channel Type
outbound_notification_url | string | N | URL to call whenever an outbound message is created using this Channel Type
allow_communications | boolean | N | Whether this Channel Type allows communications. Defaults to true.
priority | integer | N | The default priority of this channel type (when sending group messages)

## Example
### Request

    POST https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/channel-types

#### Request Body
```json 
{
    "display_name": "Customer Chat ID",
    "inbound_notification_url": "https://www.myexample.com/notifiers/inbound-chat",
    "outbound_notification_url": "https://www.myexample.com/notifiers/outbound-chat"     
}   
```

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": {
        "id": "0e3d71ee-9518-4b9b-b95a-dea251829687",
        "type_class": "UserDefinedChannel",
        "display_name": "Customer Chat ID",
        "inbound_notification_url": "https://www.myexample.com/notifiers/inbound-chat",
        "outbound_notification_url": "https://www.myexample.com/notifiers/outbound-chat",
        "allow_communications": true,
        "priority": 0,
        "is_global": false
    }   
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Channel Type]: README.md
