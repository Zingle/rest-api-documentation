# Message Object

Field | Data Type | Description
--- | --- | ---
id | string | Unique identifier
body | string | Message body
communication_direction | string | 'inbound' or 'outbound'
body_language_code | string | ISO 639-1 detected as the language of the body of the message
translated_body | string | If the detected language of the body differs from the default language of the Service and the Service has the translation feature enabled, this field will contain the translated body
translated_body_language_code | string | If the message body was translated, this will be the ISO 639-1 language code of the language it was translated to
triggered_by_user_id | string | ID of the User that triggered the message, if any
triggered_by_user | object | User object of the user who triggered the message, if any
template_id | string | ID of the [Template][] that was used to send the message, if any
sender_type | string | 'contact' or 'service' - who sent the Message
sender | object | Correspondent object representing the sender
recipient_type | string | 'contact' or 'service' - who the Message was sent to
recipient | object |  Correspondent object representing the  recipient
attachments | array | Array of string URIs where file attachments may be downloaded
created_at | UNIX timestamp | Date the Message was created
read_at | UNIX timestamp | Date the Message was marked as read by the recipient


[Template]: /templates/README.md
