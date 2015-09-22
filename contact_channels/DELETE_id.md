# Delete Contact Channel

    DELETE services/:service_id/channels/:channel_id/contacts/:contact_id/channels/:channel_id
    
Deletes a Contact Channel

## Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts/89d9e8b5-b225-476c-a83e-50cdb720e3b1/channels/d9f91fdb-bbdb-442d-bbac-99fb76263653

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": "Contact Channel deleted"
    }
}
```
