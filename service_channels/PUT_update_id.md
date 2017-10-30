# Update Service Channel

    PUT services/:service_id/channels/:channel_id
    
Updates a [Service Channel] and returns the updated object







## Parameters
### URI Parameters
None
### JSON Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
display_name | string | N | 
is_default_for_type | boolean | N | If set to true, will make this channel the default for this service for its Channel Type. You can not manually set this value to false.

## Example
### Request

    PUT https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/channels/d9f91fdb-bbdb-442d-bbac-99fb76263653

#### Request Body 
```json
{
    "display_name": "My spare phone number"
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
      "id": "d9f91fdb-bbdb-442d-bbac-99fb76263653",
      "display_name": "My spare phone number",
      "value": "+18585556565",
      "formatted_value": "(858) 555-6565",
      "country": "US",
      "is_default_for_type": false,
      "channel_type": {
        "id": "0e3d71ee-9518-4b9b-b95a-dea251829887",
        "type_class": "PhoneNumber",
        "display_name": "Phone Number",
        "inbound_notification_url": null,
        "outbound_notification_url": null,
        "allow_communications": true
      }
    }
}
```

[Service Channel]: README.md
