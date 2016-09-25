# Update Contact Custom Field Value

    POST services/:service_id/contacts/:contact_id/custom-field-values/:contact_field_id
    
Updates the value of a [Custom Field Value][] and returns the updated [Contact][].

For custom fields with options, the request body must contain a `custom_field_option_id`.  For all other data types, the field should contain a `value`.

### User Authorization Classes 
* account
* contact (requires x-zingle-contact-id header)

## Parameters
None

## Example
### Request

    POST https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1f/contacts/89d9e8b5-b225-476c-a83e-50cdb720e3b1/custom-field-values/56c70519-6c70-40e5-904e-7652e54a07b6

#### Request Body    
```json
{
    "value": "Cindy"
}
```

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
  "result": {
    "id": "f119fe3b-67e2-4b59-b605-5586616978d0",
    "is_confirmed": true,
    "is_starred": true,
    "created_at": 1442877113,
    "updated_at": 1442877113,
    "last_message": {
      "id": null,
      "body": null,
      "created_at": null
    },
    "channels": [],
    "custom_field_values": [
      {
        "value": "Cindy",
        "selected_custom_field_option_id": null,
        "custom_field": {
          "id": "56c70519-6c70-40e5-904e-7652e54a07b6",
          "display_name": "First Name",
          "code": "first_name",
          "replacement_variable": "FIRST NAME",
          "is_global": true,
          "options": []
        }
      }
    ],
    "labels": []
  }
}
```

[Custom Field Value]: README.md
[Contact]: /contacts/README.md
