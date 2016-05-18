# Contact & Service List

    GET contact_services
    
Returns a list of Services and Contacts for the given search criteria.  If no channel filters are sent, this will return a list of all services the current API credentials have access to without any corresponding contact IDs.  

### User Authorization Classes 
* account
* contact

## Parameters
Field | Required | Wildcards | Description
--- | --- | --- | ---
Pagination options | N | N | (see [Overview - Request Modifiers][])
channel_value | N | N | Filter by contact channel values (must passed send channel_type_id when this is passed)
channel_type_id | N | N | Filter by channel type (must passed send channel_value when this is passed)
last_message_created_at | N | N | Filter by last message creation date

### Sortable Fields
* last_message_created_at
* created_at

## Example
### Request

    GET https://api.zingle.me/v1/contact_services?channel_type_id=89d9e8b5-b225-474c-a83e-50cdb720e3b2&channel_value=%2B18585551212

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null,
        "sort_field": "created_at",
        "sort_direction": "asc",
        "page": 1,
        "page_size": 10,
        "total_pages": 1,
        "total_records": 2
    },
    "result": [
        {
            "contact_id": "89d9e8b5-b225-476c-a83e-50cdb720e3b1",
            "service_id": "72d9e8b5-b225-476c-a83e-50cdb720e4g6",
            "account_id": "19d9e8b5-b225-476c-a83e-50cdb720f989",
            "contact_unread_message_count": 2,
            "service_display_name": "Spa",
            "account_display_name": "Los Angeles Pure Luxury Hotel",
            "last_message": {
              "id": "989d9e8b5-b225-476c-a83e-50cdb720dhu76",
              "body": "What time does the spa open?",
              "direction": "inbound",
              "created_at": 1455560636
            }
        },
        {
            "contact_id": "e3d9e8b5-b225-476c-a83e-50cdb720f741",
            "service_id": "980fe8b5-b225-476c-a83e-50cdb720fa54",
            "account_id": "19d9e8b5-b225-476c-a83e-50cdb720f989",
            "contact_unread_message_count": 0,
            "service_display_name": "Front Desk",
            "account_display_name": "Los Angeles Pure Luxury Hotel",
            "last_message": {
              "id": "75459e8b5-b225-476c-a83e-50cdb720dhl98",
              "body": "Your room is ready, Mr. Smith. Please proceed to the front desk to pick up your key.",
              "direction": "outbound",
              "created_at": 1455560436
            }
        }        
    ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
