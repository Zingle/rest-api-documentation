# Delete Contact Group

    DELETE services/:service_id/contact-groups
    
Deletes a [Contact Group]

### User Authorization Classes 
* account

## Parameters
None
 

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/contact-groups/e122da7a-8a2a-4a59-a344-fb0e25aae01e

### Response
``` json
{
  "status": {
    "text": "OK",
    "status_code": 200,
    "description": "Contact group deleted"
  }
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Contact Group]: README.md
