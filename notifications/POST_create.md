# Subscribe to push notifications

    POST notifications
    
Subscribe to push notifications for a contact or user

### User Authorization Classes 
* account
* contact (requires x-zingle-contact-id header)

## Parameters
### URI Parameters
None
### Body Parameters
Field | Required | Description
--- | --- | ---
device_identifier | Y | Unique identifier of the device that is subscribing
operating_system | Y | One of 'ios', 'android',  or 'windows'
service_ids | N | Array of service IDs to subscribe to notifications for. Not required when subscribing a Contact to notifications
push_environment | N | One of 'dev' or 'production'. Optionally specified which push certificate will be used to send notifications

## Example
### Request

    POST https://api.zingle.me/v1/notifications
#### Request Body
```json 
{
    "device_identifier": "as897d98as7d89a7d89asd897",
    "operating_system": "ios"
}
```
### Return
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    }
}
```
