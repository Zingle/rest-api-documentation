# Available Phone Number List

    GET avilable-phone-numbers
    
Returns a list of [Available Phone Number Objects][]

## Parameters
 - **country (required)**: Two-character country code to search
 - **search**: Search string. If specified, phone numbers matching this string will be searched.  You may use wildcards(*) when searching.

## Example
**Request**

    https://api.zingle.me/v1/available-phone-numbers?country=US

**Return**
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
        "total_records": 3
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

[Available Phone Number Objects]: /README.md
