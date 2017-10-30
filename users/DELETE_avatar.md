# Delete User's Avatar

    DELETE accounts/:account_id/users/:user_id/avatar
    
Deletes a [User]'s avatar




## Parameters
None

## Example
### Request

    DELETE https://api.zingle.me/v1/accounts/11111111-1111-1111-1111-111111111111/users/c16dd162-3712-4f5d-a157-13e781baa7f4/avatar

### Response
``` json
{
  "status": {
    "text": "OK",
    "status_code": 200,
    "description": "User avatar deleted"
  }
}
```

[User]: README.md
