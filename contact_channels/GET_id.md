# Contact Channel

    GET services/:service_id/contacts/:contact_id/channels/:contact_channel_id
    
Returns a single [Contact Channel]





## Parameters
None

## Example
### Request

    GET https://api.zingle.me/v1/services/afe7bc93-6e28-4e70-8770-defa35cdfc1b/89d9e8b5-b225-476c-a83e-50cdb720e3b1/channels/1bc63907-b3df-47c4-9a7c-11ad9ab35085

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": {
    "id": "1bc63907-b3df-47c4-9a7c-11ad9ab35085",
    "value": "+18582355555",
    "formatted_value": "(858) 235-5555",
    "display_name": "MOBILE",
    "country": "US",    
    "is_default": false,
    "is_default_for_type": false,
    "block_inbound": false,
    "block_outbound": false,
    "is_messageable": true,
    "channel_type": {
        "type_class": "PhoneNumber",
        "display_name": "Phone Number",
        "allow_messages": true
    }
}
```

[Contact Channel]: README.md
