# Update Contact Custom Field 

    PUT services/:service_id/contact-custom-fields/:contact_custom_field_id
    
Updates a [Contact Custom Field]. Returns the updated object 

### User Authorization Classes 
* account

## Parameters
## Body Parameters
**NOTE:** If options are specified, all existing options will be deleted and replaced with the newly-specified options.

Field | Data Type | Required | Description
--- | --- | --- | ---
display_name | string | Y | 
options | array | N | Array of [Field Options]

## Example
### Request

    PUT https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/contact-custom-fields/9fcbf2a4-a450-42c6-b0eb-40149b6a2cfc

#### Request Body
```json 
{
  "display_name": "Mom's Favorite Flower",
  "code": "moms_favorite_flower",
  "options": [
    {
        "display_name": "Tulips",
        "value": "tulip",
        "sort_order": 0
    },
    {
        "display_name": "Yellow Roses",
        "value": "roses_yellow",
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
        "display_name": "Mom's Favorite Flower",
        "data_type": "single_select_options",
        "replacement_variable": "MOMS FAVORITE FLOWER",
        "is_global": false,
        "options": [
            {
                "id": "38444cd6-5b9d-4628-b851-7c66c6fe1ffd",
                "display_name": "Tulips",
                "value": "tulip",
                "sort_order": 38444
            },
            {
                "id": "38444c89-5b9d-4628-b851-7c66c6fe1ec1",
                "display_name": "Yellow Roses",
                "value": "roses_yellow",
                "sort_order": 1
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
