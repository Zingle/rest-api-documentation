# Detach Label from a Contact

    DELETE services/:service_id/contacts/:contact_id/labels/:label_id
    
Detaches a [Label] from a [Contact]. Returns the updated Contact.

### User Authorization Classes 
* account
* contact (requires x-zingle-contact-id header)

## Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts/f119fe3b-67e2-4b59-b605-5586616978d0/labels/4492b6a7-bac4-471a-8e54-ddcdda502013

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
    "notes": null,
    "service_id": "aff7bc93-6e28-4e70-8770-defa35cdfc1b",
    "is_messageable": true,
    "is_confirmed": true,
    "is_starred": true,
    "is_closed": false,
    "avatar_uri": null,
    "optin_status": "opted-in",
    "created_at": 1442877113,
    "updated_at": 1442877113,
    "locked_by_source": null,
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

[Contact]: README.md
[Label]: /labels/README.md
