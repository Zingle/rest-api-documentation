# Create Contact Label

    POST services/:service_id/contact-labels/
    
Create a [Label]. Returns the newly-created object.

### User Authorization Classes 
* account

## Parameters
### URI Parameters
None
### Body Parameters
Field | Required | Description
--- | --- | ---
display_name | Y |
background_color | Y | 
text_color | Y |

## Example
### Request

    POST https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/contact-labels
#### Request Body
```json 
{
    "display_name": "Foo Conference Attendees",
    "background_color": "#93623a",
    "text_color": "#ffffff"
}
```
### Return
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": {
      "id": "13dfba6d-66d2-42e9-9290-2ea9dcf7f91e",
      "display_name": "Foo Conference Attendees",
      "background_color": "#93623a",
      "text_color": "#ffffff",
      "is_global": false
    }
}
```

[Label]: README.md
