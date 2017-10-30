# Contact Label List

    GET services/:service_id/contact-labels
    
Returns a list of [Labels][] belonging to the specified [Service].




## Parameters
### URI Parameters
Field | Wildcards | Description
--- | --- | ---
Pagination options | N | (see [Overview - Request Modifiers][])
display_name | Y | Filter by display name
is_global | N | deprecated

### Sortable Fields 
* display_name

## Example
### Request

    GET https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/contact-labels

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
        "total_records": 3
    },
    "result": [
        {
          "id": "13dfba6d-66d2-42e9-9290-2ea9dcf7f91d",
          "display_name": "VIP",
          "background_color": "#93623a",
          "text_color": "#ffffff",
          "is_global": false,
          "is_automatic": false
        },
        {
          "id": "0b431e20-ead7-4fb1-8ede-59e4554d031c",
          "display_name": "Hosts",
          "background_color": "#000000",
          "text_color": "#ffffff",
          "is_global": false,
          "is_automatic": false
        },
        {
          "id": "d3701285-a000-4aea-ad59-2be6c48ad855",
          "display_name": "Checked In",
          "background_color": "#73423a",
          "text_color": "#ffffff",
          "is_global": true,
          "is_automatic": true
        } 
    ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Label]: README.md
[Service]: /services/README.md
