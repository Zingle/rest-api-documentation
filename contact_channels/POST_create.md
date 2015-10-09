# Create Contact Channel

    POST services/:service_id/contacts/:contact_id/channels
    
Creates a new [Contact Channel] and returns the newly-created object.

## Parameters
### URI Parameters
None
### JSON Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
channel_type_id | string | Y | [Channel Type] to add
value | string | Y | Channel value 
display_name | string | N | 
country | string | Y | Required for phone numbers. ISO 3166-1 alpha-2 country code. Not saved for any other channel type.
is_default | boolean | N | If set to true, will make this channel the global default for this contact
is_default_for_type | boolean | N | If set to true, will make this channel the default for this contact for its Channel Type

## Example
### Request

    POST https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts/89d9e8b5-b225-476c-a83e-50cdb720e3b1/channels

#### Request Body 
```json
{
    "channel_type_id": "0e3d71ee-9518-4b9b-b95a-dea25182988",
    "value": "+18585556565",
    "country": "US"
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
      "display_name": null,
      "value": "+18585556565",
      "formatted_value": "(858) 555-6565",
      "country": "US",
      "is_default": false,
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

[Contact Channel]: README.md
[Contact Type]: /channel_types/README.md
