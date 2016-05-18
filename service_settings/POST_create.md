# Update Service Setting

    POST services/:service_id/settings/:settings_field_id
    
Updates the value of a [Service Setting] and returns the updates [Service] object

### User Authorization Classes 
* account

## Parameters
### URI Parameters
None
### Body Parameters
Field | Required | Description
--- | --- | ---
value | Y | Required when setting a value for a [Settings Field] without options
settings_field_option_id | Y | Required when setting a value for a [Settings Field] with options

## Example
### Request

    POST https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1f/settings/ec760ab1-2679-4621-b4cf-003fa6d3ca4b

#### Request Body    
```json
{
    "value": "Thanks for your message! We will get back to you soon"
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
        "id": "aff7bc93-6e28-4e70-8770-defa35cdfc1f",
        "display_name": "Zingle Cafe",
        "time_zone": "America/Los_Angeles",
        "created_at": 1429034365,
        "updated_at": 1439228868,
        "account": {
            "id": "2c89b706-47f2-471d-8e1b-4a180b448838",
            "display_name": "Developer Account",
            "term_months": 1,
            "current_term_start_date": 1433116800,
            "current_term_end_date": null,
            "created_at": 1380312314,
            "updated_at": 1438919580
        },
        "plan": {
            "id": "a0eb6d49-caa8-4bd2-ae15-acb529a2ca98",
            "code": "zingle_basic",
            "term_months": 1,
            "monthly_or_unit_price": 0,
            "setup_price": 0,
            "display_name": "Zingle Basic",
            "is_printer_plan": false
        },
        "channels": [
          {
              "id": "d9f91fdb-bbdb-442d-bbac-99fc76263654",
              "display_name": null,
              "value": "+17245551212",
              "formatted_value": "(724) 555-1212",
              "country": "US",
              "is_default_for_type": true,
              "channel_type": {
                  "id": "0e3d71ee-9518-4b9b-b95a-2ea251829887",
                  "type_class": "PhoneNumber",
                  "display_name": "Phone Number",
                  "inbound_notification_url": null,
                  "outbound_notification_url": null,
                  "allow_communications": true
              }
          }
        ],
        "channel_types": [
          {
              "id": "0e3d71ee-9518-4b9b-b95a-dea251829887",
              "type_class": "PhoneNumber",
              "display_name": "Phone Number",
              "inbound_notification_url": null,
              "outbound_notification_url": null,
              "allow_communications": true
          }
        ],
        "service_address": {
            "address": "123 Zingle Blvd.",
            "city": "San Diego",
            "state": "CA",
            "country": "US",
            "postal_code": "92129"
        },
        "settings": [
          {
              "value": "Thanks for your message! We will get back to you soon",
              "selected_settings_field_option_id": null,
              "settings_field": {
                  "id": "ec760ab1-2679-4621-b4cf-003fa6d3ca4b",
                  "data_type": "string",
                  "display_name": "Autoresponder Body",
                  "options": []
              }
          }          
        ]
      }    
}
```

[Service Setting]: README.md
[Settings Field]: /settings_fields/README.md
[Service]: /services/README.md
