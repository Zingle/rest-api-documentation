# Event

    GET services/:service_id/events/:event_id
    
Returns a single [Event]

### User Authorization Classes 
* account
* contact (requires x-zingle-contact-id header)

## Parameters
None

## Example
### Request

    GET https://api.zingle.me/v1/services/1d06e84f-8152-4de7-983d-a2d88b73734a/events/d7d64c8a-8ff1-48ea-a209-a2d240918c93

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": {
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
}
```
[Event]: README.md
