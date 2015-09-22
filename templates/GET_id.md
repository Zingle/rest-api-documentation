# Template

    GET services/:service_id/templates/:template_id
    
Returns a single [Template].

## Parameters
None

## Example
### Request

    GET https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/templates/13dfba6d-66d2-42e9-9290-2ea9dcf7f91d

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": {
        "id": "13dfba6d-66d2-42e9-9290-2ea9dcf7f91d",
        "type": "welcome",
        "display_name": "VIP Welcome",
        "subject": null,
        "body": "Welcome back to the Zingle Hotel, {TITLE} {LAST_NAME}. We are very excited to have you back. Let us know if you need anything during your stay.",
        "is_global": false
    }
}
```

[Template]: README.md
