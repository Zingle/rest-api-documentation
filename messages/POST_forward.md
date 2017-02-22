# Forward Message

    POST services/:service_id/messages/:message_id/forward
    
Forward a message to SMS, email, a Zingle printer, a Zingle service, or a connected HotSOS instance. 

### User Authorization Classes 
* account

## Parameters
### URI Parameters
None
### JSON Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
recipient_type | string | Y | The type of recipient - 'sms', 'email', 'service','printer', or 'hotsos'
recipients | array | N | Required except when recipient_type is hotsos.  Array of recipient strings. For SMS, a phone number string. For Email, an email address. For Service or Printer, an ID. 
body | string | Y | Message body
hotsos_issue | string | N | Required when recipient_type is hotsos. Name of HotSOS issue to create.
room | string | N | Required when recipient_type is hotsos. Room number to create HotSOS order for.

## Example
### Request

    POST https://api.zingle.me/v1/services/1d06e84f-8152-4de7-983d-a2d88b73734a/messages/6eccd001-eac4-44a8-841f-fa60896deeca/forward
#### Request Body
```json
{
	"recipient_type": "sms",
	"recipients": ["+18585551214"],
	"body": "This is a forwarded message"
}
```

### Response
``` json
{
    "status": {
      "text": "OK",
      "status_code": 200,
      "description": "Message forwarded"
    }
}
```
