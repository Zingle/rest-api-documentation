# Update Template

    PUT services/:service_id/templates/:template_id
    
Update a [Template]. Returns the updated object.

### User Authorization Classes 
* account

## Parameters
### URI Parameters
None
### Body Parameters
Field | Description
--- | ---
display_name | 
templateTypeCode | 
body |  
subject | 

## Example
### Request

    PUT https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/templates/13dfba6d-66d2-42e9-9290-3ea9dcf7f912
#### Request Body
```json 
{
    "body": "Welcome to the Zingle Hotel, {TITLE} {FIRST_NAME}.  We are sure you will enjoy your first stay with us.",
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
        "body": "Welcome to the Zingle Hotel, {TITLE} {FIRST_NAME}.  We are sure you will enjoy your first stay with us.",
        "is_global": false
    }
}
```

[Template]: README.md
