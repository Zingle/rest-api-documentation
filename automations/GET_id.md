# Automation 

    GET services/:service_id/automations/:automation_id
    
Returns a single [Automation][] object

## Parameters
None

## Example
**Request**

    GET https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/automations/3d4f772f-d2c4-4dc1-98d0-6f23ba072758

**Return**
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": {
      "id": "3d4f772f-d2c4-4dc1-98d0-6f23ba072758",
      "display_name": "5-Minute Escalation",
      "is_global": true,
      "type": "Escalation",
      "status": "active"
    }
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Automation]: README.md
