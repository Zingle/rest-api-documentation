# Automation List

    GET services/:service_id/automations
    
Returns a list of [Automations] belonging to the specified [Service]

### User Authorization Classes 
* account

## Parameters
### URI Parameters
Field | Wildcards | Description
--- | --- | ---
Pagination options | N | (see [Overview - Request Modifiers][])
### Sortable fields
* display_name
* type
* created_at

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
      "sort_field": "display_name",
      "sort_direction": "asc",
      "page": 1,
      "page_size": 10,
      "total_pages": 1,
      "total_records": 2
  },
  "result": [
    {
      "id": "9153b558-c6f1-4254-a35f-af47b4bae7dc",
      "display_name": "My Zing",
      "type": "Custom Automation",
      "status": "inactive",
      "is_global": false,
      "created_at": {
        "date": "2017-05-17 23:56:56.000000",
        "timezone_type": 3,
        "timezone": "UTC"
      },
      "triggers": [
        {
          "id": "d89c6e3d-5525-4528-88ff-885cbfacbef2",
          "type_code": "first_message"
        },
        {
          "id": "91fe3cea-5923-48b7-ba02-6cc79fdd3b71",
          "type_code": "keyword"
        }
      ],
      "steps": [
        {
          "id": "d59d3124-01af-4243-9a8f-4f495f185106",
          "type_code": "reply",
          "display_name": null,
          "sort_order": "1"
        }
      ]
    },
    {
      "id": "51565714-c55c-4ccc-afa3-c36415e9ba1a",
      "display_name": "My Second Zing",
      "type": "Custom Automation",
      "status": "inactive",
      "is_global": false,
      "created_at": {
        "date": "2017-05-20 22:11:09.000000",
        "timezone_type": 3,
        "timezone": "UTC"
      },
      "triggers": [
        {
          "id": "02a244c5-ddb8-4df6-b3cc-b42f5cf5566f",
          "type_code": "keyword"
        }
      ],
      "steps": [
        {
          "id": "dad5a90b-ee38-4977-a66a-023e8d7d82d3",
          "type_code": "label_apply",
          "display_name": null,
          "sort_order": "1"
        },
        {
          "id": "b4b823b6-210e-407e-801c-8c5ede005e97",
          "type_code": "reply",
          "display_name": null,
          "sort_order": "2"
        }
      ]
    }
  ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Automations]: README.md
[Service]: /services/README.md
