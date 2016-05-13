# Delete Message 

    POST services/:service_id/messages/deleted_by_contact
    
Marks one or more [Messages] as deleted by a contact. This will delete the messages from the contact's perspective.  From the service's perspective there is no change. 

## Parameters
### URI Parameters
None
### JSON Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
message_ids | array of strings | Y | Specify the message_ids to mark as 'read by contact'

## Example
### Request

    POST https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/messages/deleted_by_contact
### Request Body 
```json
{
  "message_ids": ["819094d3-191e-4c49-b208-a9be816c9e87","739094d3-191e-4c49-b208-a9be816c39b0"]
}
```
### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": "Messages deleted"
    }
}
```
[Messages]: README.md
