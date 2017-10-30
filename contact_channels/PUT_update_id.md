# Update Contact Channel

    PUT services/:service_id/channels/:channel_id/contacts/:contact_id/channels/:channel_id
    
Updates a [Contact Channel] and returns the updated object





## Parameters
### URI Parameters
None
### JSON Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
display_name | string | N | One of HOME, BUSINESS, or MOBILE
is_default | boolean | N | If set to true, will make this channel the global default for this contact
is_default_for_type | boolean | N | If set to true, will make this channel the default for this contact for its Channel Type

## Example
### Request

    PUT https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts/89d9e8b5-b225-476c-a83e-50cdb720e3b1/channels/d9f91fdb-bbdb-442d-bbac-99fb76263653

#### Request Body 
```json
{
    "display_name": "BUSINESS"
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
      "display_name": "BUSINESS",
      "value": "+18585556565",
      "formatted_value": "(858) 555-6565",
      "country": "US",
      "is_default": false,
      "is_default_for_type": false,
      "block_inbound": false,
      "block_outbound": false,
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
