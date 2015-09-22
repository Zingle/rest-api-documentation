# Create Contact

    POST services/:service_id/contacts
    
Creates a new Contact for the specified Service and returns the newly-created [Contact]

## Parameters
None

## Example
### Request

    POST https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts


#### Request Body    
```json
{
  "custom_field_values": [
    {
      "custom_field_id": "56c70519-6c70-40e5-904e-7652e54a07b6",
      "value": "Rebecca"
    }
  ]
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
    "is_starred": false,
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
        "value": "Rebecca",
        "selected_custom_field_option_id": null,
        "custom_field": {
          "id": "56c70519-6c70-40e5-904e-7652e54a07b6",
          "display_name": "First Name",
          "is_global": true,
          "options": []
        }
      }
    ],
    "labels": []
  }
}
```

[Contact]: README.md
