# Trigger Automation on a  Contact

    POST services/:service_id/contacts/:contact_id/automations/:automation_id
    
Trigger an [Automation] on a Contact. 





## Parameters
None

## Example
### Request

    POST https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts/f119fe3b-67e2-4b59-b605-5586616978d0/automations/3d4f772f-d2c4-4dc1-98d0-6f23ba072758

### Response
``` json
{
  "status": {
    "text": "OK",
    "status_code": 200,
    "description": "Automation started"
  }
}
```

[Automation]: /automations/README.md
