# Delete Channel Type

    DELETE services/:service_id/channel-types/:channel_type_id
    
Deletes a [Channel Type].

### User Authorization Classes 
* account

## Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/channel-types/56c70519-6c70-40e5-904e-7652e54a07b6

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": "Channel Type deleted"
    } 
}
```

[Channel Type]: README.md
