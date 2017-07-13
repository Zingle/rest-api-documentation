# Contact Group

    GET services/:service_id/contact-group/:contact_group_id
    
Returns a single [Contact Group].

### User Authorization Classes 
* account

## Parameters
None

## Example
### Request

    GET https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/contact-group/e122da7a-8a2a-4a59-a344-fb0e25aae01e

### Response
``` json
{
  "status": {
      "text": "OK",
      "status_code": 200,
      "description": null
  },
  "result": {
    "id": "e122da7a-8a2a-4a59-a344-fb0e25aae01e",
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
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Contact Group]: README.md
