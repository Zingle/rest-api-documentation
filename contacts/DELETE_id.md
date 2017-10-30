# Delete Contact

    DELETE services/:service_id/contacts/:contact_id
    
Deletes a [Contact] for the specified Service





## Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts/f119fe3b-67e2-4b59-b605-5586616978d0

### Response
``` json
{
  "status": {
    "text": "OK",
    "status_code": 200,
    "description": "Contact deleted"
  }
}
```

[Contact]: README.md
