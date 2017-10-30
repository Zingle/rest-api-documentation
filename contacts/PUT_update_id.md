# Update Contact

    PUT services/:service_id/contacts/:contact_id
    
Updates a [Contact] for the specified Service and returns the updated object





## Parameters
### URI Parameters
None
### Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
channels | array | N | Array of [Contact Channels] to set on the Contact
custom_field_values | array | N | Array of [Custom Field Values] to set on the Contact
is_starred | boolean |  N | Whether the Contact should be marked as 'starred'
is_confirmed | boolean | N | Whether the Contact's conversation should be marked as 'confirmed'
is_closed | boolean | N | Whether the Contact's conversation should be closed

## Example
### Request

    PUT https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts/f119fe3b-67e2-4b59-b605-5586616978d0


#### Request Body    
```json
{
  "is_starred": true,
  "custom_field_values": [
    {
      "custom_field_id": "56c70519-6c70-40e5-904e-7652e54a07b6",
      "value": "Rebeka"
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
        "value": "Rebeka",
        "custom_field_option_id": null,
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

[Contact]: README.md
[Custom Field Values]: /custom_field_values/README.md
[Contact Channels]: /contact_channels/README.md
