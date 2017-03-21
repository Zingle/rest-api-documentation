# Delete Contact's Avatar

    DELETE services/:service_id/contacts/:contact_id/avatar
    
Deletes a [Contact]'s avatar for the specified Service

### User Authorization Classes 
* account
* contact (requires x-zingle-contact-id header)

## Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts/f119fe3b-67e2-4b59-b605-5586616978d0/avatar

### Response
``` json
{
  "status": {
    "text": "OK",
    "status_code": 200,
    "description": "Contact avatar deleted"
  }
}
```

[Contact]: README.md
