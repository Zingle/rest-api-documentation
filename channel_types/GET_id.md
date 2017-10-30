# Channel Type

    GET services/:service_id/channel-types/:channel_type_id
    
Returns a single [Channel Type].

## Parameters
None

## Example
### Request

    GET https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/channel-types/0e3d71ee-9518-4b9b-b95a-dea251829887

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null,
    },
    "result": {
        "id": "0e3d71ee-9518-4b9b-b95a-dea251829887",
        "type_class": "PhoneNumber",
        "display_name": "Phone Number",
        "inbound_notification_url": null,
        "outbound_notification_url": null,
        "allow_communications": true,
        "priority": 0,
        "is_global": true
    }    
}
```

[Channel Type]: README.md
