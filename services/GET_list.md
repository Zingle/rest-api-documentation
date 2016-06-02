# Service List

    GET services
    
Returns a list of [Services] the current user (as specified by API credentials) has access to

### User Authorization Classes 
* account
* contact

## Parameters
### URI Parameters
Field | Wildcards | Description
--- | --- | ---
Pagination options | N | (see [Overview - Request Modifiers][])
account_id | N | only return Services from this Account
channel_value | Y | Filter by service channel values
display_name | Y | Filter by Service display name
address | Y | Filter by Service street address
city | N | Filter by Service city
state | N | Filter by Service state
country | N | Filter by Service country
postal_code | N | Filter by Service postal_code

### Sortable Fields
* display_name
* created_at
* updated_at
* city
* state
* country
* postal_code

## Example
### Request

    GET https://api.zingle.me/v1/services

### Response
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
        "total_records": 1
    },
    "result": [
      {
        "id": "aff7bc93-6e28-4e70-8770-defa35cdfc1f",
        "display_name": "My test API service",
        "business_name": "My test API service",
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
        "contact_labels": [],
        "contact_custom_fields": [],        
        "service_address": {
            "address": "123 Zingle Blvd.",
            "city": "San Diego",
            "state": "CA",
            "country": "US",
            "postal_code": "92129"
        },
        "settings": []
      }
    ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Services]: README.md
