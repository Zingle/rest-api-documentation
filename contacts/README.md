# Contact Object

Field | Data Type | Description
--- | --- | ---
id | string | Unique identifier
first_name | string | First name
last_name | string | Last name
title | string | Salutation/title
notes | string | Internal note about the contact
service_id | string | Unique identifier of the Contact's Service
assigned_to_team_id | string | Unique identifier of the Contact's assigned User
assigned_to_user_id | string | Unique identifier of the Contact's assigned Team 
is_messageable | boolean | Whether the contact has a valid channel that is not blocked for outbound sending
is_confirmed | boolean | Whether the conversation associated with this Contact is currently marked as 'Confirmed'
is_starred | boolean | Whether the conversation associated with this Contact is currently marked as 'Starred'
is_closed | boolean | Whether the conversation associated with this Contact is currently closed
avatar_uri | string | URI of the contact's avatar
optin_status | string | The current opt-in status of the contact.  Will be null if the service does not have set opt-in behavior
unconfirmed_at | UNIX timestamp | Date the Contact's conversation was last marked unconfirmed/unread
created_at | UNIX timestamp | Date the Contact was created
updated_at | UNIX timestamp | Date the Contact was last updated
locked_by_source | string | If the contact was created or updated by an external system, which system will be indicated in this field. Locked contacts can not have their first name, last name, title, phone numbers, nor email addresses edited.
last_message | object | Object containing id, body, and created_at for last message sent to or received from the contact
channels | array | Array of [Contact Channels]
custom_field_values | array | Array of [Custom Field Values]
labels | array | Array of [Labels]



[Contact Channels]: /contact_channels//README.md
[Custom Field Values]: /custom_field_values/README.md
[Labels]: /labels/README.md
