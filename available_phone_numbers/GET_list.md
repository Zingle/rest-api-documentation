# Available Phone Number List

    GET available-phone-numbers
    
Returns a list of [Available Phone Number]

## Parameters
### URI Parameters
Field | Data Type | Required | Wildcards | Description
--- | --- | --- | --- | ---
country | string | Y | N | ISO 3166-1 alpha-2 country code
search | string | Y | N | A valid area code in the country
### Sortable fields
None

## Example
### Request

    https://api.zingle.me/v1/available-phone-numbers?country=US&search=619

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": [
        {
          "phone_number": "+16195556010",
          "formatted_phone_number": "(619) 555-6010",
          "country": "US"
        },
        {
          "phone_number": "+16195556099",
          "formatted_phone_number": "(619) 555-6099",
          "country": "US"
        }
    ]
}
```

[Available Phone Number]: README.md
