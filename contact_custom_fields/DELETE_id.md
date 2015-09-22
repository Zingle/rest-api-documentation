# Contact Custom Field 

    DELETE services/:service_id/contact-custom-fields/:contact_custom_field_id
    
Deletes a [Contact Custom Field][] object

## Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/contact-custom-fields/56c70519-6c70-40e5-904e-7652e54a07b6

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": "Contact Custom Field deleted",
    } 
}
```

[Contact Custom Field]: README.md
