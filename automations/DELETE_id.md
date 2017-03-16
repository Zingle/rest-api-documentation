# Delete Automation

    DELETE services/:service_id/automations/:automation_id
    
Deletes an [Automation]

### User Authorization Classes 
* account
* contact (requires x-zingle-contact-id header)

## Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/automations/99d9e0b8-b222-476d-a83e-50cdb720e3b1

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": "Automation deleted"
    }
}
```

[Automation]: README.md
