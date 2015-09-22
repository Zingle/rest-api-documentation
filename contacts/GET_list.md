# Contact List

    GET services/:service_id/contacts
    
Returns a list of [Contacts] belonging to the specified service

## Parameters
Field | Wildcards | Description
--- | --- | ---
Pagination options | N | (see [Overview - Request Modifiers][])
channel_value | Y | Filter by service channel values
label_id | N | Filter by Label ID
is_confirmed | N | Filter by confirmed status (1 = confirmed, 0 = not confirmed)
is_starred | N | Filter by starred status (1 = starred, 0 = not starred)


## Example
### Request

    GET https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/contacts

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null,
        "sort_field": "id",
        "sort_direction": "asc",
        "page": 1,
        "page_size": 10,
        "total_pages": 1,
        "total_records": 2
    },
    "result": [
    {
        "id": "89d9e8b5-b225-476c-a83e-50cdb720e3b1",
        "is_confirmed": true,
        "is_starred": false,
        "created_at": 1442352326,
        "updated_at": 1442621196,
        "last_message": {
          "id": null,
          "body": null,
          "created_at": null
        },
        "channels": [
          {
            "id": "1bc63907-b3df-47c4-9a7c-11ad9ab35085",
            "display_name": "Woohoo!",
            "value": "+18582355555",
            "formatted_value": "(858) 235-5555",
            "country": "US",
            "is_default": false,
            "is_default_for_type": false,
            "channel_type": {
              "id": "0e3d71ee-9518-4b9b-b95a-dea251829887",
              "type_class": "PhoneNumber",
              "display_name": "Phone Number",
              "inbound_notification_url": null,
              "outbound_notification_url": null,
              "allow_communications": true
            }
          },
          {
            "id": "cca65a79-cf8e-44e0-8003-b422819db801",
            "display_name": "Home",
            "value": "+18585555523",
            "formatted_value": "(858) 555-5523",
            "country": "US",
            "is_default": false,
            "is_default_for_type": false,
            "channel_type": {
              "id": "0e3d71ee-9518-4b9b-b95a-dea251829887",
              "type_class": "PhoneNumber",
              "display_name": "Phone Number",
              "inbound_notification_url": null,
              "outbound_notification_url": null,
              "allow_communications": true
            }
          }
        ],
        "custom_field_values": [
          {
            "value": "William",
            "selected_custom_field_option_id": null,
            "custom_field": {
              "id": "56c70519-6c70-40e5-904e-7652e54a07b6",
              "display_name": "First Name",
              "is_global": true,
              "options": []
            }
          },
          {
            "value": "Tell",
            "selected_custom_field_option_id": null,
            "custom_field": {
              "id": "29fdae7d-c5d7-4cd6-b2e4-cd52603ff577",
              "display_name": "Last Name",
              "is_global": true,
              "options": []
            }
          },
          {
            "value": "Mr.",
            "selected_custom_field_option_id": "266cbe3c-dd2f-45c2-8473-d84a8e6fada6",
            "custom_field": {
              "id": "808cd25e-ca27-4fdb-a10c-d87032108f38",
              "display_name": "Title",
              "is_global": true,
              "options": [
                {
                  "id": "6c39cca3-a27c-4a8b-9383-53262651d0af",
                  "display_name": "",
                  "value": "",
                  "sort_order": 1
                },
                {
                  "id": "266cbe3c-dd2f-45c2-8473-d84a8e6fada6",
                  "display_name": "Mr.",
                  "value": "Mr.",
                  "sort_order": 2
                },
                {
                  "id": "4f0fe1ce-dff6-47e6-8737-1212d603b430",
                  "display_name": "Mrs.",
                  "value": "Mrs.",
                  "sort_order": 3
                },
                {
                  "id": "5af67d3f-f31d-4f32-a560-c6a36e734b21",
                  "display_name": "Ms.",
                  "value": "Ms.",
                  "sort_order": 4
                },
                {
                  "id": "5782d3ca-9db8-4549-a5e5-9e0abd3b7366",
                  "display_name": "Dr",
                  "value": "Dr",
                  "sort_order": 5
                },
                {
                  "id": "f941f1ff-1c99-40b8-841b-b46bc5e1fd90",
                  "display_name": "Prof.",
                  "value": "Prof.",
                  "sort_order": 6
                },
                {
                  "id": "97b482f2-93a8-4eb9-8458-f922f2d4026a",
                  "display_name": "Dir.",
                  "value": "Dir.",
                  "sort_order": 7
                },
                {
                  "id": "cd15f583-a4de-46d8-b9af-17f674263472",
                  "display_name": "Rev.",
                  "value": "Rev.",
                  "sort_order": 8
                },
                {
                  "id": "5b298689-faae-4a40-8703-735b1057e892",
                  "display_name": "Capt.",
                  "value": "Capt.",
                  "sort_order": 9
                }
              ]
            }
          },
          {
            "value": "Yes",
            "selected_custom_field_option_id": null,
            "custom_field": {
              "id": "533a2ea5-ccae-4662-9a09-215aa0156a04",
              "display_name": "Verified",
              "is_global": true,
              "options": []
            }
          }
        ],
        "labels": []
      }      
    ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Contacts]: README.md
