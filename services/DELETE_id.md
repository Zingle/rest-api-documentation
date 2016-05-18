# Cancel Service

    DELETE services/:service_id
    
Cancels a [Service] and releases all associated [Service Channels]

### User Authorization Classes 
* account

## Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1f

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": "Service cancelled"
    }  
}
```

[Service]: README.md
[Service Channels]: /service_channels/README.md