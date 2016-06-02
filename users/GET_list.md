# User List

    GET users
    
Returns a list of [Users] associated with any service the current user is authorized for

### User Authorization Classes 
* account

## Parameters
### URI Parameters
Field | Wildcards | Description
service_id | N | Filter users by service_id

Pagination options | N | (see [Overview - Request Modifiers][])
### Sortable fields
* first_name
* last_name
* email_address

## Example
### Request

    GET https://api.zingle.me/v1/users

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null,
        "sort_field": "last_name",
        "sort_direction": "asc",
        "page": 1,
        "page_size": 10,
        "total_pages": 1,
        "total_records": 2
    },
    "result": [
        {
          "id": "3d4f772f-d2c4-4dc1-98d0-6f23ba072758",
          "username": "bsmith@example.com",
          "email": "bsmith@example.com",
          "first_name": "Bob",
          "last_name": "Smith",
          "title": "Front Desk Supervisor",
          "service_ids": ["3d4f772f-d2c4-4dc1-98d0-6f23ba072554"]
        },
        {
          "id": "3d4f772f-d2c4-4dc1-98d0-6f23ba07a6678",
          "username": "cdoe",
          "email": null,
          "first_name": "Cindy",
          "last_name": "Doe",
          "title": "Front Desk Staff",
          "service_ids": ["3d4f772f-d2c4-4dc1-98d0-6f23ba072554"]
        }
    ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Users]: README.md
