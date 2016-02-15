# Contact Object

Field | Data Type | Description
--- | --- | ---
id | string | Unique identifier
service_id | string | Unique identifier of the Contact's Service 
is_confirmed | boolean | Whether the conversation associated with this Contact is currently marked as 'Confirmed'
is_starred | boolean | Whether the conversation associated with this Contact is currently marked as 'Starred'
last_message | object | Object containing id, body, and created_at for last message sent to or received from the contact
channels | array | Array of [Contact Channels]
custom_field_values | array | Array of [Custom Field Values]
labels | array | Array of [Labels]
created_at | UNIX timestamp | Date the Account was created
updated_at | UNIX timestamp | Date the Account was last updated



[Contact Channels]: /contact_channels//README.md
[Custom Field Values]: /custom_field_values/README.md
[Labels]: /labels/README.md
