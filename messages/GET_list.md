# Message List

    GET services/:service_id/messages
    
Returns a list of [Messages] for the specified [Service]

## Parameters
Field | Wildcards | Description
--- | --- | ---
Pagination options | N | (see [Overview - Request Modifiers][])
contact_id | N | Filter by Contact
template_id | N | Filter by Template
communication_direction | N | Filter by communication direction
created_at | N | Filter by creation date (may use greater_than() and less_than())


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
        "total_records": 3
    },
    "result": [ 
      {
        "body": "Hello there!",
        "id": "d7d64c8a-8ff1-48ea-a209-a2d240918c93",
        "created_at": 1442249019,
        "read_at": 1442531686,
        "sender_type": "contact",
        "attachments": [],
        "sender": {
          "id": "18d69698-5b9f-4124-9d19-d55bb23eb77a",
          "channel": {
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
            "type_class": null,
            "display_name": null,
            "value": "+17605554396",
            "formatted_value": "(760) 555-4396"
          }
        },
        "communication_direction": "inbound",
        "body_language_code": "en",
        "triggered_by_user_id": null,
        "translated_body": null,
        "template_id": null,
        "translated_body_language_code": null
      },
      {
        "body": "Hello again!",
        "id": "e8f6d362-299c-4dda-971c-4bcd1aae90ef",
        "created_at": 1442249051,
        "read_at": null,
        "attachments": [],
        "sender_type": "contact",
        "sender": {
          "id": "18d69698-5b9f-4124-9d19-d55bb23eb77a",
          "channel": {
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
            "type_class": null,
            "display_name": null,
            "value": "+17605554396",
            "formatted_value": "(760) 555-4396"
          }
        },
        "communication_direction": "inbound",
        "body_language_code": "en",
        "triggered_by_user_id": null,
        "translated_body": null,
        "template_id": null,
        "translated_body_language_code": null
      }
    ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Messages]: README.md
[Service]: /services/README.md
