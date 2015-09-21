# Contact Object

Field | Data Type | Description
--- | --- | ---
id | string | Unique identifier
is_confirmed | boolean | Whether the conversation associated with this Contact is currently marked as 'Confirmed'
is_starred | boolean | Whether the conversation associated with this Contact is currently marked as 'Starred'
last_message | object | Object containing id, body, and created_at for last message sent to or received from the contact
channels | array | Array of [Contact Channel Objects][]
custom_field_values | array | Array of [Custom Field Value Objects][]
created_at | UNIX timestamp | Date the Account was created
updated_at | UNIX timestamp | Date the Account was last updated



[Contact Channel Objects]: /contact_channels//README.md
[Custom Field Value Objects][]: /custom_field_values/README.md
