# Contact Service Object

Field | Data Type | Description
--- | --- | ---
contact_id | string | Unique identifier of the Contact
account_id | string | Unique identifier of the Account
service_id | string | Unique identifier of the Service
contact_unread_message_count | integer | Number of messages for this contact and service with a null read_by_contact_at
service_display_name | string | Display name of the Service the Contact belongs to
account_display_name | string | Display name of the Service's Account 
last_message | object | Object containing id, body, direction, and created_at for last message sent to or received from the contact
created_at | UNIX timestamp | Date the Contact was created
updated_at | UNIX timestamp | Date the Contact was last updated
