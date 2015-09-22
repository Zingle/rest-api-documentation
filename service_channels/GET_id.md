# Service Channel

    GET services/:service_id/channels/:service_channel_id
    
Returns a single [Service Channel]

## Parameters
None

## Example
### Request

    GET https://api.zingle.me/v1/services/afe7bc93-6e28-4e70-8770-defa35cdfc1b/channels/d9f91fdb-bbdb-442d-bbac-99fb76263654

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": {
      "id": "d9f91fdb-bbdb-442d-bbac-99fb76263654",
      "display_name": null,
      "value": "+17245559509",
      "formatted_value": "(724) 555-9509",
      "country": "US",
      "is_default_for_type": true,
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

[Service Channel]: /service_channels/README.md
