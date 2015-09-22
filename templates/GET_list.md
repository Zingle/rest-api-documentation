# Template List

    GET services/:service_id/templates
    
Returns a list [Template][] objects scoped to the selected service

## Parameters
None

## Example
### Request

    GET https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/templates

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null,
        "sort_field": null,
        "sort_direction": "asc",
        "page": 1,
        "page_size": 10,
        "total_pages": 1,
        "total_records": 3       
    },
    "result": [
        {
            "id": "13dfba6d-66d2-42e9-9290-2ea9dcf7f91d",
            "type": "welcome",
            "display_name": "VIP Welcome",
            "subject": null,
            "body": "Welcome back to the Zingle Hotel, {TITLE} {LAST_NAME}. We are very excited to have you back. Let us know if you need anything during your stay.",
            "is_global": false
        },
        {
            "id": "13dfba6d-66d2-42e9-9290-2ea9dcf7e91d",
            "type": "general",
            "display_name": "You're welcome",
            "subject": null,
            "body": "It's our pleasure, {TITLE} {LAST_NAME}.",
            "is_global": false
        },
        {
            "id": "13dfba6d-66d2-42e9-9290-2ed3dcf7f91d",
            "type": "general",
            "display_name": "Apology Escalation",
            "subject": null,
            "body": "We are very sorry, {TITLE} {LAST_NAME}. A manager will be in touch with you very shortly.",
            "is_global": false
        }                
    ]
}
```

[Template]: README.md
