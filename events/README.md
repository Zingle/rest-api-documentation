# Event Object

Field | Data Type | Description
--- | --- | ---
id | string | Unique identifier
contact_id | string | ID of the contact the event is linked to
event_type | string | The type of event. 
created_at | UNIX timestamp | Date the Message was created
triggered_by_user | object | User object of the user who triggered the event
automation | object | The automation the event occurred in, if any
message | object | The message object, for 'message' event types


