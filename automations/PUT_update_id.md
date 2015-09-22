# Update Automation 

    PUT services/:service_id/automations/:automation_id
    
Update the status of a single [Automation][] object. Returns the updated [Automation][] object.

## Parameters
### URI Parameters
None
### Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
status | string | Y | "active" or "inactive"

## Example
### Request

    PUT https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/automations/3d4f772f-d2c4-4dc1-98d0-6f23ba072758
#### Request Body
```json
{
    "status": "inactive"
}
```

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
      "status": "inactive"
    }
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Automation]: README.md
