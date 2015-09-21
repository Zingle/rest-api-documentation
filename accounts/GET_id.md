# Account

    GET accounts/:account_id
    
Returns a single [Account Object]

## Parameters
None

## Example
**Request**

    https://api.zingle.me/v1/accounts/2d89b706-47f2-471d-8e1b-4a180b448838

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
    "result": {
            "id": "2d89b706-47f2-471d-8e1b-4a180b448838",
            "display_name": "API Account 1",
            "term_months": 1,
            "current_term_start_date": 1433116800,
            "current_term_end_date": null,
            "created_at": 1380312314,
            "updated_at": 1438919580
    }
}
```

[Account Object]: README.md
