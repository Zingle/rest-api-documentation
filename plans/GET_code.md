# Plan

    GET accounts/:account_id/plans/:plan_code
    
Returns a single [Plan]

### User Authorization Classes 
* account

## Parameters
None

## Example
### Request

    https://api.zingle.me/v1/accounts/2d89b706-47f2-471d-8e1b-4a180b448838/plans/zingle_basic

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": {
          "code": "zingle_basic",
          "monthly_or_unit_price": 55,
          "term_months": 1,
          "setup_price": 0,
          "display_name": "Zingle Basic",
          "is_printer_plan": false
    }
}
```

[Plan]: README.md
