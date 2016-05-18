# Account

    GET accounts/:account_id
    
Returns a single [Account]

### Required Authorization Class: account

## Parameters
None

## Example
### Request

    https://api.zingle.me/v1/accounts/2d89b706-47f2-471d-8e1b-4a180b448838

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
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

[Account]: README.md
