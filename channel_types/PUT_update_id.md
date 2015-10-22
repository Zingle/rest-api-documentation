# Update Channel Type

    PUT services/:service_id/channel-types/:channel_type_id
    
Updates a [Channel Type]. Returns the updated object 

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

    PUT https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/channel-types/0e3d71ee-9518-4b9b-b95a-dea251829687

#### Request Body
```json 
{
    "inbound_notification_url": "https://www.myexample.com/notifiers/inbound-chat-notice",
    "outbound_notification_url": "https://www.myexample.com/notifiers/outbound-chat-notice"     
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
        "inbound_notification_url": "https://www.myexample.com/notifiers/inbound-chat-notice",
        "outbound_notification_url": "https://www.myexample.com/notifiers/outbound-chat-notice",
        "allow_communications": true,
        "priority": 0,
        "is_global": false
    }   
}
```

[Channel Type]: README.md
