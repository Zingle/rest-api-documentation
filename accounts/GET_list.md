# Account List

    GET accounts
    
Returns a list of accounts the current authorized user has access to

## Parameters
 - Pagination options (see [Overview - Request Modifiers][])

## Return format
See [Account Object Format][]

## Example
**Request**

    https://api.zingle.me/v1/accounts

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
            "id": "2c89b706-47f2-431d-8e1b-4a180b448838",
            "display_name": "API Account 1",
            "term_months": 1,
            "current_term_start_date": 1433116800,
            "current_term_end_date": null,
            "created_at": 1380312314,
            "updated_at": 1438919580
        },
        {
            "id": "b550a786-e28f-4f40-8fc0-7fbac7f10429",
            "display_name": "My Second API Account",
            "term_months": 1,
            "current_term_start_date": null,
            "current_term_end_date": null,
            "created_at": 1421864342,
            "updated_at": 1439217400
        }
    ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Account Object Format]: README.md
