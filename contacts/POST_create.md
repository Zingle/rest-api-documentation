# Create Contact

    POST services/:service_id/contacts
    
Creates a new [Contact] for the specified Service and returns the newly-created object



* contact

## Parameters
### URI Parameters
Field | Description
--- | --- | ---
return_existing | If set to 1 and a contact already exists with the specified channel type and values, the existing contact will be updated with the new custom field values and the existing contact will be returned.  You can only use this option if the channels array has exactly one element.
### Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
channels | array | N | Array of [Contact Channels] to create when creating the contact
custom_field_values | array | N | Array of [Custom Field Values] to set on the Contact
is_starred | boolean |  N | Whether the Contact should be marked as 'starred'
is_confirmed | boolean | N | Whether the Contact's conversation should be marked as 'confirmed'
is_closed | boolean | N | Whether the Contact's conversation should be closed

## Example
### Request

    POST https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts

#### Request Body    
```json
{
  "channels": [
    {
        "channel_type_id": "23c70519-6c70-40e5-904e-7652e54a85fg",
        "value": "+18585551212"
    }
  ],
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
    "notes": null,
    "service_id": "aff7bc93-6e28-4e70-8770-defa35cdfc1b",
    "is_messageable": true,
    "is_confirmed": true,
    "is_starred": false,
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
    "channels": [
        {
            "id": "a8g70519-6c70-40e5-904e-7652e54a12t3",
            "display_name": null,
            "value": "+18585551212",
            "formatted_value": "(858) 555-1212",
            "is_default": true,
            "is_default_for_type": true,
            "block_inbound": false,
            "block_outbound": true,
            "channel_type": {
                "id": "23c70519-6c70-40e5-904e-7652e54a85fg",            
                "type_class": "PhoneNumber",
                "display_name": "Phone Number"
            }
        }
    ],
    "custom_field_values": [
      {
        "value": "Rebecca",
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
