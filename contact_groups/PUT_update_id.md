# Update Contact Group

    PUT services/:service_id/contact-groups/:contact_group_id
    
Updates a [Contact Group]

### User Authorization Classes 
* account

## Parameters
Field | Required | Wildcards | Description
--- | --- | --- | ---
display_name | Y | N | The created Contact Group's display name
condition_boolean_operator | Y | N | The boolean operator between conditions
background_color | N | N | The background color of the displayed Contact Group identifier
text_color | N | N | The color of the text of the displayed Contact Group identifier
conditions | Y | N | The conditions from which the contact group is created
 

## Example
### Request

    PUT https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/contact-groups/e122da7a-8a2a-4a59-a344-fb0e25aae01e
#### Request Body
```json
{
  "display_name": "Smiths",
  "condition_boolean_operator": "AND",
  "conditions": [
    {
      "comparison_method_code": "string_contains",
      "comparison_source": "{CONTACT.LAST_NAME}",
      "comparison_value": "smith"
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
      "description": null,
  },
  "result": {
    "id": "e122da7a-8a2a-4a59-a344-fb0e25aae01e",
    "display_name": "Smiths",
    "condition_boolean_operator": "AND",
    "background_color": null,
    "text_color": null,
    "conditions": [
      {
        "comparison_method_code": "string_contains",
        "comparison_source": "{CONTACT.LAST_NAME}",
        "comparison_value": "smith"
      }
    ]
  }
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Contact Group]: README.md