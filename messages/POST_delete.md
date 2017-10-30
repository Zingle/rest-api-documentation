# Delete Delayed Message 

    DELETE services/:service_id/messages/:message_id
    
Deletes a message that is 'delayed' but not yet sent.





## Parameters
### URI Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/messages/819094d3-191e-4c49-b208-a9be816c9e87

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": "Messages deleted"
    }
}
```
[Messages]: README.md
