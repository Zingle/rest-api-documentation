# Mark Message Read

    POST services/:service_id/messages/:message_id/read
    POST services/:service_id/messages/read
    
Marks one or more [Messages] as read. If a single message is updated, that message it returned.  If more than one message is updated, a 200 response is returned but no message data is returned.

If the call is made under the account user authorization class and the URL services/:service_id/messages/read is used, the body of the message must contain message_ids.

If the call is made under the contact user authorization class and the URL services/:service_id/messages/read is used, the body of the message may optionally contain message_ids. If message_ids is not included in the body, all of the contacts unread messages will be marked as read.

### User Authorization Classes 
* account
* contact (requires x-zingle-contact-id header)

## Parameters
### URI Parameters
None
### JSON Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
message_ids | array| N | Array of message IDs to mark as read
read_at | UNIX timestamp| N | Specify the read_at timestamp.  If ommitted, the current time will be used

## Example
### Request

    POST https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/messages/739094d3-191e-4c49-b208-a9be816c39b0/read
### Request Body 
```json
{
  "read_at": 1442881911
}
```
### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": {
    "body": "3\nThank you! Your order has been confirmed",
    "id": "739094d3-191e-4c49-b208-a9be816c39b0",
    "template_id": null,
    "created_at": 1442881911,
    "updated_at": 1442881911,
    "read_at": 1442881911,
    "deleted_by_contact_at": null,
    "triggered_by_user_id": null,
    "triggered_by_user": {},
    "sender_type": "service",
    "sender": {
      "id": "1d06e84f-8152-4de7-983d-a2d88b73734a",
      "channel": {
        "id": "9cb3f0a0-7e88-431f-8941-a34787939434"
        "type_class": "PhoneNumber",
        "display_name": null,
        "value": "+17602784396",
        "formatted_value": "(760) 278-4396"
      }
    },
    "recipient_type": "contact",
    "recipient": {
      "id": "18d69698-5b9f-4124-9d19-d55bb23eb77a",
      "channel": {
        "type_class": "PhoneNumber",
        "display_name": "Phone Number",
        "value": "+18582311214",
        "formatted_value": "(858) 231-1214"
      }
    },
    "attachments": [
      "https://6407d4d3a30bb891aafe-345656863e41d74beb2a8fef19bcbe4a.ssl.cf1.rackcdn.com/attachment_5713.gif"
    ],
    "communication_direction": "outbound",
    "attachments": [],
    "is_delayed": false,
    "execute_at": 0,
    "executed_at": null,
    "translated_body_language_code": null,
    "translated_body": null,
    "body_language_code": null
  }
}
```
[Message]: README.md
