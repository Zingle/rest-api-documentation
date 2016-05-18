# Event List

    GET services/:service_id/events
    
Returns a list of [Events] for the specified [Service]. 

### User Authorization Classes 
* account
* contact

## Parameters
Field | Wildcards | Description
--- | --- | ---
Pagination options | N | (see [Overview - Request Modifiers][])
contact_id | N | Filter by Contact
event_type | N | Filter by event type
contact_id | N | Filter by Contact
triggered_by_user_id | N | Filter by triggering user
automation_id | N | Filter by associated automation
created_at | N | Filter by creation date (may use greater_than() and less_than())
template_id | N | Filter by Template (only applies to message events)
communication_direction | N | Filter by communication direction (only applies to message events)
contact_channel_id | N | Filter by contact channel (only applies to message events)

### Sortable Fields
* created_at
* contact_id
* event_type
* read_at
* communication_direction
* triggered_by_user_id,
* automation_id


## Example
### Request

    GET https://api.zingle.me/v1/services/1d06e84f-8152-4de7-983d-a2d88b73734a/events

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
        "id": "d7d64c8a-8ff1-48ea-a209-a2d240918c93",
        "contact_id": "89j64c8a-8ff1-48ea-a209-a2d240918d77",
        "event_type": "workflow_started",
        "body": null,
        "created_at": 1442249019,
        "triggered_by_user": {},
        "automation": {
          "id": "33d64c8a-8ff1-48ea-a209-a2d240918e44",
          "display_name": "Default Survey",
          "type": "survey"
        },
        "message": {}      
      }
    ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Events]: README.md
[Service]: /services/README.md
[Account]: /accounts/README.md
