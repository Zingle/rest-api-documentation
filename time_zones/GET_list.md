# Time Zone List

    GET accounts
    
Returns an array of Time Zones that can be used when provisioning or configuring a service

### User Authorization Classes 
* account

## Parameters
None

## Example
### Request

    https://api.zingle.me/v1/time-zones

### Sortable Fields
None

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null,
    },
    "result": [
        "America/Anchorage",
        "America/Argentina/San_Juan",
        "America/Chicago",
        "America/Denver",
        "America/Los_Angeles",
        "America/New_York",
        "America/Phoenix"
    ]
}
```
