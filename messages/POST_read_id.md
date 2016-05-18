# Mark Message Read

    POST services/:service_id/messages/:message_id/read
    
Marks a [Message] as read by the service. Returns the update Message.

## Parameters
### URI Parameters
None
### JSON Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
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
    "created_at": 1442881911,
    "read_at": 1442881911,
    "read_by_contact_at": 1442881911,
    "sender_type": "service",
    "sender": {
      "id": "1d06e84f-8152-4de7-983d-a2d88b73734a",
      "channel": {
        "type_class": null,
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
    "body_language_code": null,
    "triggered_by_user_id": null,
    "triggered_by_user": {},
    "translated_body": null,
    "template_id": null,
    "translated_body_language_code": null
  }
}
```
[Message]: README.md
