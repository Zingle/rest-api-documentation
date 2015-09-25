# Automation List

    GET services/:service_id/automations
    
Returns a list of [Automations] belonging to the specified [Service]

## Parameters
### URI Parameters
Field | Wildcards | Description
--- | --- | ---
Pagination options | N | (see [Overview - Request Modifiers][])
### Sortable fields
* display_name
* type

## Example
### Request

    GET https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/automations

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
          "id": "3d4f772f-d2c4-4dc1-98d0-6f23ba072758",
          "display_name": "5-Minute Escalation",
          "is_global": true,
          "type": "Escalation",
          "status": "active"
        },
        {
          "id": "46ab325e-6360-4d7b-aedc-67b90aa64e5e",
          "display_name": "10-Minute Escalation",
          "is_global": false,
          "type": "Escalation",
          "status": "inactive"
        } 
    ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Automations]: README.md
[Service]: /services/README.md