# Assign a Contact

    POST services/:service_id/contacts/:contact_id/assign
    
Assign [Contact] to a User or Team. Returns the updated Contact. A user or team may be specified, but not both

## Parameters
### URI Parameters
None
### Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
userId | string | N | The ID of the user to assign the contact to
teamId | string | N | The ID of the team to assign the contact to

## Example
### Request

    POST https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts/f119fe3b-67e2-4b59-b605-5586616978d0/assign

#### Request Body    
```json
{
  "userId": "5912ac4d-280a-4d4e-a632-961b40718293"
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
    "assigned_to_team_id": null,
    "assigned_to_user_id": "5912ac4d-280a-4d4e-a632-961b40718293",
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
          "code": "first_name",
          "replacement_variable": "FIRST NAME",
          "is_global": true,
          "options": []
        }
      }
    ],
    "labels": [
      {
        "id": "4492b6a7-bac4-471a-8e54-ddcdda502013",
        "display_name": "VIP",
        "background_color": "#e84527",
        "text_color": "#ffffff",
        "is_automatic": false,
        "is_global": false        
      }
    ]
  }
}
```
[Contact]: README.md
