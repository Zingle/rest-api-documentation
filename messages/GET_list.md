# Message List

    GET services/:service_id/messages
    
Returns a list of [Messages] for the specified [Service]. 

### User Authorization Classes 
* account
* contact (requires x-zingle-contact-id header)

## Parameters
Field | Wildcards | Description
--- | --- | ---
Pagination options | N | (see [Overview - Request Modifiers][])
contact_channel_value | N | Filter by Contact channel value
contact_channel_id | N | Filter by Contact channel ID
contact_id | N | Filter by Contact
template_id | N | Filter by Template
communication_direction | N | Filter by communication direction
created_at | N | Filter by creation date (may use greater_than() and less_than())

### Sortable Fields
* created_at
* read_at
* communication_direction
* is_delayed
* execute_at
* executed_at
* updated_at


## Example
### Request

    GET https://api.zingle.me/v1/services/1d06e84f-8152-4de7-983d-a2d88b73734a/messages

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null,
        "sort_field": "display_name",
        "sort_direction": "asc",
        "page": 1,
        "page_size": 10,
        "total_pages": 1,
        "total_records": 2
    },
    "result": [ 
      {
        "body": "Hello there!",
        "id": "d7d64c8a-8ff1-48ea-a209-a2d240918c93",
        "template_id": null,
        "created_at": 1442249019,
        "updated_at": 1442249019,
        "read_at": 1442531686,
        "deleted_by_contact_at": null,
        "triggered_by_user_id": null,
        "triggered_by_user": {},
        "sender_type": "contact",
        "sender": {
          "id": "18d69698-5b9f-4124-9d19-d55bb23eb77a",
          "channel": {
            "id": "9cb3f0a0-7e88-431f-8941-a34787939434",
            "type_class": "PhoneNumber",
            "display_name": "Phone Number",
            "value": "+18585551214",
            "formatted_value": "(858) 555-1214"
          }
        },
        "recipient_type": "service",
        "recipient": {
          "id": "1d06e84f-8152-4de7-983d-a2d88b73734a",
          "channel": {
            "id": "23590fd3-79ee-4be2-8597-cb9bed3377da",
            "type_class": null,
            "display_name": null,
            "value": "+17605554396",
            "formatted_value": "(760) 555-4396"
          }
        },
        "communication_direction": "inbound",
        "attachments": [],
        "is_delayed": false,
        "execute_at": 0,
        "executed_at": null,
        "translated_body_language_code": null,
        "translated_body": null,
        "body_language_code": "en",
      },
      {
        "body": "Hello again!",
        "id": "e8f6d362-299c-4dda-971c-4bcd1aae90ef",
        "template_id": null,
        "created_at": 1442249051,
        "updated_at": 1442249051,
        "read_at": null,
        "deleted_by_contact_at": null,
        "triggered_by_user_id": null,
        "triggered_by_user": {},
        "sender_type": "contact",
        "sender": {
          "id": "18d69698-5b9f-4124-9d19-d55bb23eb77a",
          "channel": {
            "id": "9cb3f0a0-7e88-431f-8941-a34787939434",
            "type_class": "PhoneNumber",
            "display_name": "Phone Number",
            "value": "+18585551214",
            "formatted_value": "(858) 555-1214"
          }
        },
        "recipient_type": "service",
        "recipient": {
          "id": "1d06e84f-8152-4de7-983d-a2d88b73734a",
          "channel": {
            "id": "23590fd3-79ee-4be2-8597-cb9bed3377da",
            "type_class": null,
            "display_name": null,
            "value": "+17605554396",
            "formatted_value": "(760) 555-4396"
          }
        },
        "communication_direction": "inbound",
        "attachments": [],
        "is_delayed": false,
        "execute_at": 0,
        "executed_at": null,
        "translated_body_language_code": null,
        "translated_body": null,
        "body_language_code": "en"
      }
    ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Messages]: README.md
[Service]: /services/README.md
[Account]: /accounts/README.md
