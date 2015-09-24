# Create Contact Custom Field 

    POST services/:service_id/contact-custom-fields
    
Creates a [Contact Custom Field]

## Parameters
## Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
display_name | string | Y | 
options | array | N | Array of [Field Options]

## Example
### Request

    POST https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/contact-custom-fields

#### Request Body
```json 
{
  "display_name": "Favorite Flower",
  "options": [
    {
        "display_name": "Tulips",
        "value": "tulip",
        "sort_order": 0
    },
    {
        "display_name": "White Roses",
        "value": "roses_white",
        "sort_order": 1
    },
    {
        "display_name": "Red Roses",
        "value": "roses_red",
        "sort_order": 2
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
        "description": null
    },
    "result": {
        "id": "9fcbf2a4-a450-42c6-b0eb-40149b6a2cfc",
        "display_name": "Favorite Flower",
        "data_type": "single_select_options",
        "is_global": false,
        "options": [
          {
            "id": "38444cd6-5b9d-4628-b851-7c66c6fe1ffd",
            "display_name": "Tulips",
            "value": "tulip",
            "sort_order": 38444
          },
          {
            "id": "74a490ca-1f50-4b0c-8e4c-05f187276356",
            "display_name": "White Roses",
            "value": "roses_white",
            "sort_order": 74
          },
          {
            "id": "c367b4ab-8518-4aa0-8d2c-6fe2e6614f17",
            "display_name": "Red Roses",
            "value": "roses_red",
            "sort_order": 0
          }
        ]
    }   
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Contact Custom Field]: README.md
[Field Options]: /field_options/README.md
