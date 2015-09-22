# Available Phone Number List

    GET available-phone-numbers
    
Returns a list of [Available Phone Number Objects][]

## Parameters
### URI Parameters
Field | Data Type | Required | Wildcards | Description
country | string | Y | N | ISO 3166-1 alpha-2 country code
search | string | N | Y | If specified, phone numbers matching this string will be searched. 

## Example
### Request

    https://api.zingle.me/v1/available-phone-numbers?country=US

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
          "phone_number": "+18025556010",
          "formatted_phone_number": "(802) 555-6010",
          "country": "US"
        },
        {
          "phone_number": "+16315556099",
          "formatted_phone_number": "(631) 555-6099",
          "country": "US"
        }
    ]
}
```

[Available Phone Number Objects]: README.md
