# Create Template

    POST services/:service_id/templates
    
Create a [Template]. Returns the newly-created object.

### User Authorization Classes 
* account

## Parameters
### URI Parameters
None
### Body Parameters
Field | Required | Description
--- | --- | ---
display_name | Y |
templateTypeCode | Y |
body | Y | 
subject | N |

## Example
### Request

    POST https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/templates
#### Request Body
```json 
{
    "display_name": "Welcome first-time guest",
    "body": "Welcome to the Zingle Hotel, {TITLE} {FIRST_NAME}.  We hope you enjoy your first stay with us.",
    "templateTypeCode": "general"
}
```

### Return
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": {
        "id": "13dfba6d-66d2-42e9-9290-3ea9dcf7f912",
        "templateTypeCode": "general",
        "display_name": "Welcome first-time guest",
        "subject": null,
        "body": "Welcome to the Zingle Hotel, {TITLE} {FIRST_NAME}.  We hope you enjoy your first stay with us.",
        "is_global": false
    }
}
```

[Template]: README.md
