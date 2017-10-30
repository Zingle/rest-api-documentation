# Contact Group List

    GET services/:service_id/contact-groups
    
Returns a list of [Contact Groups] for the given service




## Parameters
Field | Required | Wildcards | Description
--- | --- | --- | ---
Pagination options | N | N | (see [Overview - Request Modifiers][])
 

## Example
### Request

    GET https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/contact-groups

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
        },
        {
          "id": "8ab199e6-a259-4e97-b3bd-90335ec8ef71",
          "display_name": "June New People",
          "condition_boolean_operator": "AND",
          "conditions": [
            {
              "comparison_method_code": "date_is_or_after",
              "comparison_source": "{CONTACT.CREATED_AT}",
              "comparison_value": "2017-06-01"
            },
            {
              "comparison_method_code": "date_is_or_before",
              "comparison_source": "{CONTACT.CREATED_AT}",
              "comparison_value": "2017-06-30"
            }            
          ]
        }          
    ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Contact Groups]: README.md
