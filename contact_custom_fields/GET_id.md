# Contact Custom Field 

    GET services/:service_id/contact-custom-fields/:contact_custom_field_id
    
Returns a single [Contact Custom Field].

### User Authorization Classes 
* account

## Parameters
None

## Example
### Request

    GET https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/contact-custom-fields/56c70519-6c70-40e5-904e-7652e54a07b6

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null,
    },
    "result": {
      "id": "56c70519-6c70-40e5-904e-7652e54a07b6",
      "display_name": "First Name",
      "data_type": "string",
      "replacement_variable": "FIRST NAME",
      "is_global": true,
      "options": []
    }    
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Contact Custom Field]: README.md
