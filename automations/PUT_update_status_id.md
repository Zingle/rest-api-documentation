# Update Automation 

    PUT services/:service_id/automations/:automation_id
    
Update the status of a single [Automation]. Returns the updated object.

### User Authorization Classes 
* account

## Parameters
### URI Parameters
None
### Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
status | string | Y | "active" or "inactive"

## Example
### Request

    PUT https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/automations/0f0a9170-4e49-47ee-9e18-71d2a093df43
#### Request Body
```json
{
    "status": "inactive"
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
    "id": 971,
    "uuid": "0f0a9170-4e49-47ee-9e18-71d2a093df43",
    "display_name": "My Zing",
    "status": "inactive",
    "triggers": [
      {
        "id": "d99a12f1-1b6f-4f91-bb5a-81a0b9299010",
        "type": "keyword",
        "properties": {
          "comparison_method_code": "string_contains",
          "comparison_value": "wifi password",
          "delay": 0
        }
      }
    ],
    "actions": [
      {
        "id": "8f1a217b-6569-4921-ab11-979d1c322160",
        "type": "label_apply",
        "order": "1",
        "condition_outcome": "default",
        "properties": {
          "label_id": "24"
        },
        "conditions": []
      },
      {
        "id": "3579d8fc-8f27-453f-9870-a84600f9c3e9",
        "type": "reply",
        "order": "2",
        "condition_outcome": "conditions_pass",
        "properties": {
          "body": "",
          "delay_minutes": "0"
        },
        "conditions": [
          {
            "id": null,
            "property": "{CONTACT.LABELS}",
            "comparison_method_code": "string_equals",
            "compare_data_to": "57",
            "sort_order": "1"
          },
          {
            "id": null,
            "property": "{CONTACT.CUSTOM_FIELD.100}",
            "comparison_method_code": "number_equals",
            "compare_data_to": "4",
            "sort_order": "2"
          }
        ]
      },
      {
        "id": "0967eb38-2cea-4d65-9317-f4c43eec388b",
        "type": "contact_delete",
        "order": "3",
        "condition_outcome": "default",
        "properties": [],
        "conditions": []
      }
    ],
    "timeout_actions": [],
    "timeout_minutes": 15
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Automation]: README.md
