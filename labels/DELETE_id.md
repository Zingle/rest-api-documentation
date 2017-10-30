# Delete Contact Label

    DELETE services/:service_id/contact-labels/:label_id
    
Delete a [Label].




## Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/contact-labels/13dfba6d-66d2-42e9-9290-2ea9dcf7f91d

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": "Label deleted"
    }
}
```

[Label]: README.md
