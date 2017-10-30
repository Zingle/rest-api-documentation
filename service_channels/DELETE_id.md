# Delete Service Channel

    DELETE services/:service_id/channels/:channel_id
    
Deletes a [Service Channel]




## Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/channels/d9f91fdb-bbdb-442d-bbac-99fb76263653
    
### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": "Service channel deleted"
    }
}
```

[Service Channel]: README.md
