# Stop a running Automation on a  Contact

    POST services/:service_id/contacts/:contact_id/stop-automation
    
Stop a running [Automation] on a Contact. 

### User Authorization Classes 
* account
* contact (requires x-zingle-contact-id header)

## Parameters
None

## Example
### Request

    POST https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts/f119fe3b-67e2-4b59-b605-5586616978d0/stop-automation

### Response
``` json
{
  "status": {
    "text": "OK",
    "status_code": 200,
    "description": "Automation stopped"
  }
}
```

[Automation]: /automations/README.md
