# Contact Object

Field | Data Type | Description
--- | --- | ---
id | string | Unique identifier
service_id | string | Unique identifier of the Contact's Service 
is_messageable | boolean | Whether the contact has a valid channel that is not blocked for outbound sending
is_confirmed | boolean | Whether the conversation associated with this Contact is currently marked as 'Confirmed'
is_starred | boolean | Whether the conversation associated with this Contact is currently marked as 'Starred'
is_closed | boolean | Whether the conversation associated with this Contact is currently closed
locked_by_source | string | If the contact was created or updated by an external system, which system will be indicated in this field. Locked contacts can not have their first name, last name, title, phone numbers, nor email addresses edited.
last_message | object | Object containing id, body, and created_at for last message sent to or received from the contact
channels | array | Array of [Contact Channels]
custom_field_values | array | Array of [Custom Field Values]
labels | array | Array of [Labels]
created_at | UNIX timestamp | Date the Account was created
updated_at | UNIX timestamp | Date the Account was last updated



[Contact Channels]: /contact_channels//README.md
[Custom Field Values]: /custom_field_values/README.md
[Labels]: /labels/README.md
