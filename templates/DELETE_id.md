# Delete Template

    DELETE services/:service_id/templates/:template_id
    
Delete a [Template][] object.

## Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/templates/13dfba6d-66d2-42e9-9290-3ea9dcf7f912

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": "Template deleted"
    }
}
```

[Template]: README.md
