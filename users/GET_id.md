# User

    GET accounts/:account_id/users/:user_id
    
Returns a single [User].

### User Authorization Classes 
* account

## Parameters
None

## Example
### Request

    GET https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/users/7c9j2933s-d8n3-8xn3-30m4-9d33bv613579

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": {
      "id": "7c9j2933s-d8n3-8xn3-30m4-9d33bv613579",
      "username": "wtell@zingle.me",
      "title": null,
      "email": "wtell@zingle.me",
      "status": "active",
      "first_name": "William",
      "last_name": "Tell",
      "phone_number": null,
      "avatar_uri": "https://6407d4d3a30bb891aafe-345656863e41d74beb2a8fef19bcbe4a.ssl.cf1.rackcdn.com/727113a8-03cd-414f-b251-4c4f83431611.png",
      "account_uuids": [
        "a43gf496-1035-6d1y-k761-13v561red3q8"
      ],
      "service_uuids": [
        "fae3ef6d-a253-42f9-9fc1-a9765ab59694"
      ]
    }
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[User]: README.md
